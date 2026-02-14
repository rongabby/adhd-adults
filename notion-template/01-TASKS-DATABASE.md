# Tasks Database Structure

## Overview
The Tasks Database is the core engine of ADHD Flow OS. It's designed to help you capture, organize, and complete tasks in a way that works with your ADHD brain.

---

## Database Properties

### 1. Name (Title)
- **Type**: Title
- **Description**: The task description
- **Example**: "Write project proposal", "Call dentist", "Buy groceries"

### 2. Status (Select)
- **Type**: Select
- **Options**:
  - 📥 **Inbox** (default for new tasks) - Gray
  - 📋 **To Do** - Blue
  - 🔄 **In Progress** - Orange
  - ✅ **Done** - Green
  - ⏸️ **On Hold** - Yellow
  - ❌ **Cancelled** - Red

### 3. Priority (Select)
- **Type**: Select
- **Options**:
  - 🔴 **High** - Red background
  - 🟡 **Medium** - Yellow background
  - 🟢 **Low** - Green background
  - ⚪ **Someday/Maybe** - Gray

### 4. Energy Required (Select)
- **Type**: Select
- **Description**: Match tasks to your current energy level
- **Options**:
  - ⚡ **Low Energy** - Quick, easy tasks (5-15 min)
  - ⚡⚡ **Medium Energy** - Moderate effort (30-60 min)
  - ⚡⚡⚡ **High Energy** - Deep focus needed (1-3 hours)

### 5. Due Date (Date)
- **Type**: Date
- **Include Time**: Optional
- **Description**: When this task needs to be done
- **Can be empty**: Yes (not everything needs a deadline)

### 6. Scheduled For (Date)
- **Type**: Date
- **Description**: When you plan to work on this
- **Different from Due Date**: You might schedule a task before it's due

### 7. Project (Relation)
- **Type**: Relation to Projects database
- **Description**: Link tasks to larger projects
- **Can be empty**: Yes (one-off tasks don't need a project)

### 8. Tags (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 💼 Work
  - 🏠 Personal
  - 🏃 Errands
  - 📞 Calls/Emails
  - 💡 Creative
  - 📝 Admin
  - 🎨 Fun
  - 🚨 Urgent
  - 🔁 Recurring
  - 🧠 Requires Focus
  - 👥 Waiting on Others

### 9. Context (Select)
- **Type**: Select
- **Description**: Where/how to do this task
- **Options**:
  - 🏢 Office
  - 🏠 Home
  - 💻 Computer
  - 📱 Phone
  - 🚗 Out & About
  - 🧘 Anywhere/Flexible

### 10. Time Estimate (Select)
- **Type**: Select
- **Options**:
  - 5 minutes
  - 15 minutes
  - 30 minutes
  - 1 hour
  - 2-3 hours
  - Half day
  - Full day
  - Multiple days

### 11. Notes (Text)
- **Type**: Text (Long)
- **Description**: Details, links, thoughts about the task
- **Use for**: Breaking down steps, copying relevant info, paste links

### 12. Subtasks Checklist (Text or Template)
- **Type**: Text with checklist
- **Template**:
```
☐ Step 1
☐ Step 2
☐ Step 3
```

### 13. Motivation / Why (Text)
- **Type**: Text
- **Description**: Why this matters - helps with task initiation
- **Example**: "This will help me feel less stressed", "Client is waiting", "Will make me feel proud"

### 14. Dopamine Reward (Text)
- **Type**: Text
- **Description**: What you'll do/get after completing this
- **Example**: "Coffee break", "15 min social media", "Victory dance"

### 15. Created Date (Created time)
- **Type**: Created time
- **Automatic**: Yes
- **Description**: When task was added

### 16. Completed Date (Formula or Date)
- **Type**: Date
- **Description**: When you checked it done
- **Use**: For tracking patterns

### 17. Days in System (Formula)
- **Type**: Formula
- **Formula**: `dateBetween(now(), prop("Created Date"), "days")`
- **Description**: How long has this been sitting? (helps identify stuck tasks)

### 18. Is Overdue (Formula)
- **Type**: Formula
- **Formula**: `if(prop("Status") != "Done" and prop("Due Date") < now(), "⚠️ OVERDUE", "")`
- **Description**: Visual flag for overdue tasks

---

## Database Views

### View 1: Today (List)
**Purpose**: Focus on what's due or scheduled today

**Filters**:
- Status is not "Done"
- Status is not "Cancelled"
- Due Date is Today OR Scheduled For is Today

**Sort**:
1. Priority (High → Low)
2. Energy Required (Low → High)

**Properties Shown**:
- Name
- Priority
- Energy Required
- Time Estimate
- Context
- Checkbox

**Group By**: Priority

---

### View 2: This Week (Board)
**Purpose**: Weekly planning view

**Filters**:
- Status is not "Done"
- Status is not "Cancelled"
- Due Date is within next 7 days OR Scheduled For is within next 7 days

**Board Columns**: Status (To Do | In Progress | Done)

**Sort**: Priority, then Due Date

**Properties Shown**:
- Name
- Due Date
- Tags
- Energy Required

---

### View 3: By Energy Level (Board)
**Purpose**: Match tasks to your current energy

**Filters**:
- Status is "To Do" or "In Progress"

**Board Columns**: Energy Required (Low | Medium | High)

**Sort**: Priority

**Properties Shown**:
- Name
- Time Estimate
- Due Date
- Context

---

### View 4: Overdue (List)
**Purpose**: Address stuck tasks

**Filters**:
- Status is not "Done"
- Status is not "Cancelled"
- Due Date is before Today

**Sort**: Due Date (Oldest first)

**Properties Shown**:
- Name
- Due Date
- Days in System
- Priority
- Why this is stuck (Notes)

**Color**: All items show in red

---

### View 5: Hyperfocus Queue (List)
**Purpose**: Tasks that need deep work

**Filters**:
- Status is "To Do" or "In Progress"
- Energy Required is "High"
- Tags contains "Requires Focus"

**Sort**: Priority

**Properties Shown**:
- Name
- Time Estimate
- Due Date
- Motivation / Why
- Notes

---

### View 6: Quick Wins (List)
**Purpose**: Build momentum with easy tasks

**Filters**:
- Status is "To Do"
- Time Estimate is "5 minutes" OR "15 minutes"
- Energy Required is "Low"

**Sort**: Priority

**Properties Shown**:
- Name
- Time Estimate
- Context
- Dopamine Reward

---

### View 7: Waiting On Others (List)
**Purpose**: Track tasks you're blocked on

**Filters**:
- Tags contains "Waiting on Others"
- Status is "On Hold"

**Sort**: Due Date

**Properties Shown**:
- Name
- Notes (who/what you're waiting for)
- Due Date
- Follow-up date

---

### View 8: Inbox to Process (List)
**Purpose**: Triage new captures

**Filters**:
- Status is "Inbox"

**Sort**: Created Date (Newest first)

**Properties Shown**:
- Name
- Created Date
- All properties (to fill in during processing)

---

### View 9: All Tasks (Table)
**Purpose**: Master list with all details

**Filters**: None (or hide Done older than 30 days)

**Sort**: Created Date (Newest first)

**Properties Shown**: All

**Group By**: Status

---

### View 10: Completed This Month (Gallery)
**Purpose**: Celebrate wins!

**Filters**:
- Status is "Done"
- Completed Date is within last 30 days

**Sort**: Completed Date (Newest first)

**Properties Shown**:
- Name
- Completed Date
- Dopamine Reward
- Project

**Display**: Large cards with checkmark emoji

---

## Task Templates

### Template 1: Simple Task
```
Name: [Task name]
Status: To Do
Priority: Medium
Energy Required: Medium
Tags: [Relevant tag]
Time Estimate: 30 minutes
```

### Template 2: Project Task
```
Name: [Task name]
Status: To Do
Priority: [Set priority]
Energy Required: [Assess]
Project: [Link to project]
Tags: [Relevant tags]
Time Estimate: [Estimate]
Subtasks:
☐ [Step 1]
☐ [Step 2]
☐ [Step 3]
Motivation / Why: [Why this matters]
```

### Template 3: Quick Capture
```
Name: [Quick thought]
Status: Inbox
[Everything else blank - process later]
```

### Template 4: Recurring Task
```
Name: [Task name] - [Date]
Status: To Do
Tags: Recurring
Scheduled For: [Date]
Context: [Where to do]
Time Estimate: [How long]
Notes: [Copy from previous instance]
```

---

## Quick Add Buttons

### Button 1: Work Task
- Sets Tags: Work
- Sets Status: To Do
- Opens in side peek

### Button 2: Errand
- Sets Tags: Errands
- Sets Context: Out & About
- Sets Status: To Do

### Button 3: Quick Win
- Sets Energy Required: Low
- Sets Time Estimate: 15 minutes
- Sets Status: To Do

### Button 4: Deep Work
- Sets Energy Required: High
- Sets Tags: Requires Focus
- Sets Time Estimate: 2-3 hours
- Sets Status: To Do

---

## Integration with AI Prompts

### Task Initiation Button
```
🚀 Help Me Start This Task

Copy this to AI:
"I'm stuck starting this task: [TASK NAME]. 
My energy level is [X/10]. 
Can you break this into tiny steps and give me just the first 2-minute action?"
```

### Task Breakdown Button
```
📝 Break This Down

Copy this to AI:
"I need to [TASK NAME]. This feels overwhelming. 
Can you break this into 5-10 manageable steps, each taking 15 minutes or less? 
Start with the easiest first step."
```

---

## ADHD-Friendly Features

### Visual Cues
- **Color-coded priorities**: Red/Yellow/Green for instant recognition
- **Energy icons**: Lightning bolts show at a glance
- **Status emojis**: Symbols make scanning easier
- **Progress tracking**: See what's done without guilt about what's not

### Forgiveness Built-In
- **No streak trackers on tasks**: Avoiding guilt
- **"Someday/Maybe" option**: Permission to deprioritize
- **Can cancel tasks**: It's okay to let things go
- **No harsh language**: "On Hold" not "Failed"

### Dopamine Optimization
- **Celebration view**: See completed tasks gallery
- **Rewards field**: Built-in motivation
- **Quick Wins view**: Easy momentum builders
- **Visual progress**: Satisfying to see status change

### Executive Function Support
- **Time estimates**: Help with planning
- **Context field**: Batch similar tasks
- **Energy matching**: Do tasks when you have the right fuel
- **Motivation field**: Remember why it matters

---

## Customization Tips

### Add Custom Tags
Common additions:
- Specific project names
- Client names
- Seasonal tasks
- Life areas (health, finances, etc.)

### Adjust Energy Levels
Modify based on YOUR energy patterns:
- Some people do 4 levels instead of 3
- Add "Hyperfocus" as special high-energy state
- Create "Depleted" for tasks to do when exhausted

### Create Custom Views
Examples:
- By project
- By life area
- By context (all phone calls together)
- By due week
- By who assigned it

---

## Maintenance Tips

### Daily
- ✅ Check Today view
- ✅ Move tasks between statuses
- ✅ Add new captures to Inbox

### Weekly
- 🗂️ Process Inbox (triage new tasks)
- 🧹 Review Overdue (reschedule or cancel)
- 🎯 Schedule next week's priorities
- 🎉 Look at Completed view (celebrate!)

### Monthly
- 📊 Archive completed tasks older than 30 days
- 🗑️ Delete cancelled tasks
- 📈 Review patterns (what took longer than expected?)
- 🎨 Adjust views/properties as needed

---

**Remember**: This system serves you, not the other way around. Start with the basics and customize as you learn what works for your brain! 🧠✨
