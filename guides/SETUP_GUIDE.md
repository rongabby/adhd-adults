# ADHD Flow OS - Setup Guide

## Welcome! 🧠✨

This guide will walk you through setting up your complete ADHD Flow OS in Notion. Take your time—you don't need to do everything in one sitting!

---

## Before You Begin

### What You'll Need
- ✅ Notion account (free or paid)
- ✅ 2-4 hours for initial setup (can be split over multiple days)
- ✅ These implementation files from the repository
- ✅ Optional: Coffee/tea and your favorite music

### Important Mindset
- **Start simple**: You can always add complexity later
- **Something > Perfect**: A working 80% system beats a perfect 0% system
- **Make it yours**: Customize everything to fit YOUR brain
- **Progress over perfection**: Always

---

## Setup Timeline

### Quick Start (30 minutes)
Get the essentials running today:
- Main dashboard page
- Tasks database
- Daily check-in spot

### Full Setup (2-4 hours)
Build the complete system:
- All databases
- All views
- Integrations
- Customizations

### Choose Your Approach
- **Option A**: Quick start today, expand later
- **Option B**: One section per day over a week
- **Option C**: Deep dive in one focused session

---

## Phase 1: Foundation (30-60 minutes)

### Step 1: Create Your Workspace

1. **Open Notion**
2. **Create a new page**: Click "+ New Page" in sidebar
3. **Name it**: "ADHD Flow OS" (or whatever resonates with you!)
4. **Add icon**: Click "Add icon" → Choose 🧠 or ✨
5. **Add cover**: Click "Add cover" → Pick a calming gradient or solid color
   - Recommended: Lavender, mint, or soft blue
6. **Set page width**: Click "•••" menu → Page width → Full width

**🎯 Checkpoint**: You should have a blank page with icon and cover

---

### Step 2: Build Core Databases

Let's create the engines that power everything:

#### A. Tasks Database

1. **Type** `/database` and select "Database - Full page"
2. **Create new database** named "Tasks"
3. **Add properties** (click "+" in property bar):

```
✅ Name (Title) - already there
📊 Status (Select):
   - 📥 Inbox
   - 📋 To Do
   - 🔄 In Progress
   - ✅ Done
   - ⏸️ On Hold

🎯 Priority (Select):
   - 🔴 High
   - 🟡 Medium
   - 🟢 Low

⚡ Energy Required (Select):
   - ⚡ Low
   - ⚡⚡ Medium
   - ⚡⚡⚡ High

📅 Due Date (Date)
🏷️ Tags (Multi-select) - add your common tags
📝 Notes (Text)
```

4. **Save database** (it auto-saves, but double-check)

**🎯 Checkpoint**: You should see a database with all these properties

---

#### B. Habits Database

1. **Create another database** named "Habits"
2. **Add properties**:

```
✅ Habit Name (Title) - already there
📁 Category (Select):
   - 🏃 Health & Wellness
   - 🧠 ADHD Management
   - 💼 Productivity
   - 🎨 Creative

🔁 Frequency (Select):
   - Daily
   - 3-5x per week
   - Weekly

🔥 Current Streak (Number)
📅 Last Completed (Date)
💭 Why This Matters (Text)
```

**🎯 Checkpoint**: Habits database created with properties

---

#### C. Mood Tracker Database

1. **Create another database** named "Mood Tracker"
2. **Add properties**:

```
📅 Date (Date)
😊 Mood (Select):
   - 😄 Excellent
   - 😊 Good
   - 😐 Okay
   - 😔 Low
   - 😢 Very Low

⚡ Energy Level (Select):
   - ⚡⚡⚡⚡⚡ 5
   - ⚡⚡⚡⚡ 4
   - ⚡⚡⚡ 3
   - ⚡⚡ 2
   - ⚡ 1

😴 Sleep Hours (Number)
💊 Meds Taken (Checkbox)
🏆 Wins Today (Text)
📝 Notes (Text)
```

**🎯 Checkpoint**: Mood Tracker database ready

---

#### D. Quick Capture / Inbox Database

1. **Create another database** named "Brain Dump"
2. **Keep it simple**:

```
💭 Thought/Idea (Title)
📁 Type (Select):
   - 📝 Note
   - 💡 Idea
   - 🔗 Link
   - ✅ Task

📅 Captured Date (Created time) - automatic
☑️ Processed (Checkbox)
```

**🎯 Checkpoint**: All 4 core databases created!

---

### Step 3: Create Your Dashboard Homepage

Now let's build the main page that ties everything together.

1. **Go back to your main "ADHD Flow OS" page**
2. **Add a header callout**:
   - Type `/callout`
   - Icon: 🧠✨
   - Background: Light purple or blue
   - Text: "ADHD Flow OS - Dopamine-friendly | Forgiving | AI-Powered"

3. **Add navigation buttons** (type `/button` or use callout blocks):

```
Row 1:
📅 TODAY  |  🏆 WEEKLY  |  ⚡ QUICK CAPTURE

Row 2:
🔥 HYPERFOCUS  |  ❤️ WELLNESS  |  📊 ALL TASKS
```

4. **Create three columns** (type `/column`)

**Left Column: Today at a Glance**
- Add heading "🎯 Today's Mission"
- Add text block for daily focus
- Add linked database → Choose Tasks
- Filter: Due Date = Today
- View: List, limit to 5 items

**Center Column: Action Center**
- Add heading "🧠 Brain Dump"
- Add linked database → Choose Brain Dump
- Add heading "⚡ Quick Actions"
- Add buttons for task creation

**Right Column: Support & Rewards**
- Add heading "🐿️ Distraction Parking Lot"
- Add toggle list for random thoughts
- Add heading "🎁 Dopamine Menu"
- Add text list of quick rewards

**🎯 Checkpoint**: Dashboard structure is visible and functional

---

## Phase 2: Database Views (30-45 minutes)

Now let's create different ways to view your data.

### Tasks Database Views

1. **Open your Tasks database** (full page)
2. **Create views** (click "+ Add a view" at top)

**View 1: Today Only**
- View type: List
- Filter: Due Date = Today AND Status ≠ Done
- Sort: Priority (High → Low)
- Name it: "📅 Today"

**View 2: This Week**
- View type: Board
- Group by: Status
- Filter: Due Date = This Week
- Name it: "📆 This Week"

**View 3: By Energy**
- View type: Board
- Group by: Energy Required
- Filter: Status = To Do
- Name it: "⚡ By Energy"

**View 4: All Tasks**
- View type: Table
- No filters
- Show all properties
- Name it: "📊 All Tasks"

**🎯 Checkpoint**: At least 4 views created in Tasks database

---

### Habits Database Views

1. **Open your Habits database**
2. **Create views**:

**View 1: Active Habits**
- View type: Gallery
- Filter: None (or Status = Active if you added that property)
- Sort: Category
- Cards show: Name, Current Streak, Last Completed

**View 2: Habit Calendar**
- View type: Calendar
- Date property: Last Completed
- Name it: "📅 Habit Calendar"

**🎯 Checkpoint**: Habit views created

---

### Mood Tracker Views

1. **Open your Mood Tracker database**
2. **Create views**:

**View 1: This Week**
- View type: Timeline or List
- Filter: Date = This Week
- Sort: Date (newest first)

**View 2: Monthly Calendar**
- View type: Calendar
- Date property: Date
- Color: By Mood

**🎯 Checkpoint**: Mood tracking views ready

---

## Phase 3: Daily Pages & Templates (20-30 minutes)

### Create a Daily Page Template

1. **In your dashboard**, add a section "📅 Daily Pages"
2. **Create a new database** called "Daily Pages"
3. **Properties**:
   - Date (Date)
   - Morning Mood (Select)
   - Evening Reflection (Text)

4. **Create page template**:

```
[Date at top]

## Morning ☀️
☐ Took meds
☐ Ate breakfast
☐ Checked today's priorities

🎯 Today's Mission:
[What matters most today?]

## Tasks for Today
[Linked view from Tasks database, filtered to today]

## Brain Dump
[Quick capture area]

## Evening 🌙
✨ Wins today:
-
-
-

📝 What I learned:

💭 Tomorrow's top 3:
1.
2.
3.
```

**🎯 Checkpoint**: Daily template created

---

## Phase 4: AI Integration (15-20 minutes)

### Add AI Prompt Buttons

1. **Create a database** called "AI Prompt Library"
2. **Properties**:
   - Prompt Name (Title)
   - Category (Select)
   - Full Prompt (Text)
   - When to Use (Text)

3. **Add your first prompts** from the AI prompt files:
   - Copy prompts from `/ai-prompts/` folder
   - Create one entry per prompt
   - Categorize them

4. **Add quick-access buttons to dashboard**:

```
✨ AI COACH QUICK ACCESS

[Button: 🚀 Help Me Start]
[Button: 💪 Motivate Me]
[Button: 📝 Break It Down]
[Button: 📚 Browse All Prompts]
```

**🎯 Checkpoint**: AI prompts accessible from dashboard

---

## Phase 5: Customization (30-45 minutes)

### Make It Yours!

1. **Colors**: Adjust callout backgrounds, database covers
2. **Icons**: Change emojis to ones you love
3. **Layout**: Rearrange sections to fit your flow
4. **Views**: Show/hide properties based on what you use
5. **Buttons**: Add custom quick-add buttons for common tasks

### Add Sample Data

Create a few sample entries to test:
- 3-5 tasks with different priorities
- 2-3 habits you want to track
- A mood entry from today
- A few brain dump items

**🎯 Checkpoint**: System feels personalized and has test data

---

## Phase 6: Mobile Setup (10-15 minutes)

### Optimize for Phone

1. **Download Notion mobile app**
2. **Test your dashboard on phone**:
   - Can you see main sections?
   - Are buttons tappable?
   - Is text readable?
3. **Adjustments**:
   - Use toggles to collapse sections
   - Pin most-used databases to favorites
   - Add home screen widget for quick capture

**🎯 Checkpoint**: Mobile experience is smooth

---

## Phase 7: Workflow Testing (15-20 minutes)

### Test Your Setup

Walk through these scenarios:

1. **Morning routine**:
   - Open dashboard
   - Check Today's tasks
   - Add daily mood entry
   - Log habit completion

2. **During day**:
   - Quick brain dump
   - Add new task
   - Update task status
   - Check energy level for task matching

3. **Evening routine**:
   - Review completed tasks
   - Log wins
   - Plan tomorrow's top 3
   - Update habit streaks

**🎯 Checkpoint**: All workflows work smoothly

---

## Troubleshooting

### Common Issues

**Problem**: Database views are empty
**Solution**: Add sample data or check filters aren't too restrictive

**Problem**: Links between databases aren't working
**Solution**: Recreate relations, ensure databases are in same workspace

**Problem**: Dashboard is overwhelming
**Solution**: Use toggle blocks to hide sections, simplify to essentials

**Problem**: Can't find things
**Solution**: Use search (Cmd/Ctrl + P), add to favorites

**Problem**: Mobile view is cluttered
**Solution**: Create mobile-specific view with just essentials

---

## Next Steps

### Week 1: Getting Comfortable
- Use the system daily
- Add real tasks and data
- Adjust what feels clunky
- Start the 30-Day Challenge

### Week 2-4: Expansion
- Add more databases (Second Brain, Projects, etc.)
- Create additional views
- Integrate workbooks
- Fine-tune to your needs

### Month 2+: Maintenance
- Weekly review routine
- Monthly cleanup
- Quarterly deep review
- Continuous small improvements

---

## Getting Help

### Resources
- **Notion Help Center**: Official guides and videos
- **ADHD Flow OS Community**: [Your community link]
- **Video Tutorials**: [Link to your videos]
- **Email Support**: [Your support email]

### Common Questions
See `FAQ.md` in the repository for detailed answers.

---

## Celebration Time! 🎉

You did it! You have a functional ADHD management system built specifically for how your brain works.

**Remember**:
- It doesn't have to be perfect to be useful
- You'll keep adjusting and improving
- The system serves you—not the other way around
- You're building life-changing habits

**Now go use your beautiful new system!** 🧠✨

---

## Quick Reference: What to Do Daily

### Every Morning (5 minutes)
1. ☑️ Open dashboard
2. ☑️ Check Today's tasks
3. ☑️ Set daily mission
4. ☑️ Quick mood check

### Throughout Day
- Capture thoughts to Brain Dump
- Update task statuses
- Use AI prompts when stuck

### Every Evening (5 minutes)
1. ☑️ Log wins
2. ☑️ Update habits
3. ☑️ Mood check
4. ☑️ Tomorrow's top 3

---

**Need more help? Check BUILD_INSTRUCTIONS.md for detailed implementation guidance!**
