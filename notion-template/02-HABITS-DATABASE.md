# Habits Database Structure

## Overview
Track habits in a forgiving, dopamine-friendly way. This database focuses on building consistency without guilt when you miss days.

---

## Database Properties

### 1. Habit Name (Title)
- **Type**: Title
- **Example**: "Take morning meds", "10-minute walk", "Drink water"
- **Tip**: Use emoji in the name for visual appeal (💊 Meds, 🚶 Walk, 💧 Water)

### 2. Category (Select)
- **Type**: Select
- **Options**:
  - 🏃 **Health & Wellness** - Purple
  - 🧠 **ADHD Management** - Blue
  - 💼 **Productivity** - Coral
  - 🎨 **Creative** - Pink
  - 🤝 **Social** - Yellow
  - 🏠 **Home Care** - Green
  - 💰 **Financial** - Teal

### 3. Frequency (Select)
- **Type**: Select
- **Options**:
  - Daily
  - 3-5x per week
  - Weekly
  - Bi-weekly
  - Monthly
  - As needed

### 4. Current Streak (Number)
- **Type**: Number
- **Description**: Days in a row completed
- **Display**: Show with fire emoji in views (🔥 7)

### 5. Longest Streak (Number)
- **Type**: Number
- **Description**: Personal best
- **Motivation**: Beat your own record

### 6. Last Completed (Date)
- **Type**: Date
- **Auto-update**: Manual (check when done)

### 7. Next Target Date (Formula)
- **Type**: Formula
- **Formula**: Based on frequency, calculate next target
- **Description**: When to do this next

### 8. Why This Matters (Text)
- **Type**: Text
- **Description**: Your personal reason for this habit
- **Example**: "Helps me focus", "Reduces anxiety", "Makes me feel proud"

### 9. Implementation Intention (Text)
- **Type**: Text
- **Format**: "After [TRIGGER], I will [HABIT]"
- **Example**: "After I pour my coffee, I will take my meds"
- **Why**: Research shows this increases habit success

### 10. Total Completions (Number)
- **Type**: Number
- **Description**: Lifetime count
- **Motivation**: Every completion counts!

### 11. Difficulty (Select)
- **Type**: Select
- **Options**:
  - 😊 Easy (low friction)
  - 😐 Medium (some effort)
  - 😤 Challenging (requires push)

### 12. Time Required (Select)
- **Type**: Select
- **Options**:
  - < 5 min
  - 5-15 min
  - 15-30 min
  - 30-60 min
  - 60+ min

### 13. Best Time (Select)
- **Type**: Select
- **Options**:
  - Morning
  - Midday
  - Afternoon
  - Evening
  - Before bed
  - Anytime

### 14. Reminder Set (Checkbox)
- **Type**: Checkbox
- **Description**: Do you have a phone/calendar reminder?

### 15. Habit Stack Partner (Relation)
- **Type**: Relation to Habits database (self-relation)
- **Description**: Pair with another habit (habit stacking)
- **Example**: "Stretch" linked to "Morning coffee"

### 16. Notes (Text)
- **Type**: Text
- **Use for**: Tracking obstacles, celebrations, adjustments

### 17. Status (Select)
- **Type**: Select
- **Options**:
  - ✅ Active
  - ⏸️ Paused
  - 🗓️ Seasonal
  - ✨ Completed Goal (graduated!)
  - 🔄 Adjusting

### 18. Created Date (Created time)
- **Type**: Created time
- **Automatic**: Yes

### 19. Days Active (Formula)
- **Type**: Formula
- **Formula**: `dateBetween(now(), prop("Created Date"), "days")`

---

## Database Views

### View 1: Active Habits (Gallery)
**Purpose**: Daily dashboard view

**Filter**:
- Status is "Active"

**Sort**: Category, then Habit Name

**Layout**: Gallery with large cards

**Properties Shown**:
- Habit Name (with emoji)
- Current Streak 🔥
- Last Completed
- Frequency
- Checkbox to mark complete

**Card Display**: 
- Cover: Emoji or color by category
- Large text for streak number

---

### View 2: Habit Tracker Calendar (Calendar)
**Purpose**: Visual pattern tracking

**Filter**: Status is "Active"

**Date Property**: Last Completed

**Color**: By Category

**Properties Shown**:
- Habit Name
- Streak

---

### View 3: By Category (Board)
**Purpose**: Organize by life area

**Filter**: Status is "Active"

**Board Columns**: Category

**Sort**: Current Streak (High to Low)

**Properties Shown**:
- Habit Name
- Current Streak
- Frequency
- Last Completed

---

### View 4: Morning Routine (List)
**Purpose**: What to do when you wake up

**Filter**:
- Status is "Active"
- Best Time is "Morning" or "Before bed"

**Sort**: Custom order (your routine sequence)

**Properties Shown**:
- Habit Name
- Time Required
- Checkbox

**Use**: Pull into daily dashboard

---

### View 5: Quick & Easy (List)
**Purpose**: Momentum builders

**Filter**:
- Status is "Active"
- Difficulty is "Easy"
- Time Required is "< 5 min" or "5-15 min"

**Sort**: Time Required

**Properties Shown**:
- Habit Name
- Time Required
- Why This Matters

---

### View 6: Needs Attention (List)
**Purpose**: Habits you're struggling with

**Filter**:
- Status is "Active"
- Last Completed is more than 7 days ago

**Sort**: Last Completed (Oldest first)

**Properties Shown**:
- Habit Name
- Last Completed
- Why This Matters
- Notes (obstacles)

**Action**: Review and adjust

---

### View 7: Paused & Seasonal (Table)
**Purpose**: Habits on hold

**Filter**:
- Status is "Paused" or "Seasonal"

**Sort**: Category

**Properties Shown**: All

**Use**: Revisit during quarterly review

---

### View 8: Hall of Fame (Gallery)
**Purpose**: Celebrate success!

**Filter**: All habits

**Sort**: Longest Streak (High to Low)

**Properties Shown**:
- Habit Name
- Longest Streak 🏆
- Total Completions
- Days Active
- Category

**Display**: Celebration view with big numbers

---

## Habit Templates

### Template 1: Daily Habit
```
Habit Name: [Name with emoji]
Category: [Select]
Frequency: Daily
Why This Matters: [Your reason]
Implementation Intention: After [trigger], I will [habit]
Difficulty: [Easy/Medium/Challenging]
Time Required: [Select]
Best Time: [Morning/Evening/etc]
Status: Active
Reminder Set: ☐
```

### Template 2: Weekly Habit
```
Habit Name: [Name]
Category: [Select]
Frequency: Weekly
Why This Matters: [Your reason]
Best Time: [Day and time]
Time Required: [Select]
Status: Active
Notes: [When/where you'll do this]
```

### Template 3: Habit Stack
```
Habit Name: [New habit]
Category: [Select]
Frequency: Daily
Implementation Intention: After [existing habit], I will [this habit]
Habit Stack Partner: [Link to existing habit]
Difficulty: Easy (piggybacking makes it easier!)
Status: Active
```

---

## Quick Actions

### Button 1: Mark Done Today
- Opens habit entry
- Updates Last Completed to today
- Increments Current Streak (if appropriate)
- Increments Total Completions

### Button 2: Break Happened (No Guilt!)
- Resets Current Streak to 0
- Keeps Longest Streak and Total Completions
- Adds note: "Break is okay! Starting fresh."

### Button 3: New Daily Habit
- Opens template
- Pre-fills Frequency: Daily
- Pre-fills Status: Active

---

## Habit Stacking Guide

### What is Habit Stacking?
Link new habits to existing ones using "After [THIS], I will [THAT]" formula.

### Examples
- After I **pour my coffee**, I will **take my meds**
- After I **brush my teeth**, I will **do 10 pushups**
- After I **sit at my desk**, I will **write for 5 minutes**
- After I **close my laptop**, I will **stretch for 2 minutes**

### Why It Works for ADHD
- Reduces decision fatigue
- Uses existing triggers
- Creates automatic routine
- Lower activation energy

---

## Forgiving Features

### No Guilt Tracking
- **Breaking a streak is okay**: Numbers reset, but progress remains
- **Paused is valid**: Life happens, pause without shame
- **"Adjusting" status**: Experimenting is part of the process
- **Total completions matter more**: Consistency over perfection

### Flexible Frequency
- **Not everything is daily**: Some habits are 3-5x/week
- **"As needed" option**: For irregular but important habits
- **Seasonal habits**: Garden in summer, cozy habits in winter

### Progress Focus
- **Days active**: Shows commitment even with breaks
- **Total completions**: Every single time counts
- **Longest streak**: You did it before, you can again
- **Category balance**: Not about perfecting all areas at once

---

## Integration with Daily Dashboard

### Pull These Views
1. **Active Habits Gallery** - See all at once
2. **Morning Routine List** - Start the day
3. **Quick & Easy** - Momentum when low energy

### Add These Blocks
```
🔥 Habit Streaks Today

[Linked view showing 3-5 primary habits]

☐ [Habit 1] - Current: 🔥 7
☐ [Habit 2] - Current: 🔥 3
☐ [Habit 3] - Current: 🔥 14
```

---

## Celebration Rituals

### Daily
- Check off completed habit
- Watch streak number go up
- Feel the dopamine!

### Weekly
- Review Hall of Fame
- Note improvements
- Adjust struggling habits

### Monthly
- Total up completions
- Celebrate longest streaks
- Graduate completed goals
- Add new habits (one at a time!)

---

## ADHD-Specific Tips

### Start Small
- **1-3 habits maximum** to start
- Choose easiest ones first
- Build confidence before adding more

### Make It Visible
- Pin Active Habits view to dashboard
- Use phone widget if available
- Physical checklist as backup

### Reduce Friction
- Prep materials night before
- Keep supplies visible and accessible
- Choose location carefully

### Stack, Don't Add
- Attach new habits to existing routines
- Use triggers you already do
- Piggyback on strong habits

### Forgive and Adjust
- Missing days happens
- Some habits don't stick - that's data
- Seasonal motivation is real
- Pause and restart is valid

---

## Customization Ideas

### Add Custom Properties
- **Energy Required**: High/Medium/Low (like tasks)
- **Weather Dependent**: For outdoor habits
- **Social Component**: Solo vs with others
- **Cost per Completion**: For financial habits
- **Body Part**: For exercise habits

### Create Custom Views
- **By Time of Day**: Morning, Midday, Evening
- **By Energy Level**: Match to your state
- **By Location**: Home, Gym, Office, Outdoors
- **Stacked Chains**: Habits grouped by trigger

### Link to Other Databases
- **Projects**: Habits supporting specific goals
- **Mood Tracker**: See habit-mood correlations
- **Tasks**: Recurring tasks as habits
- **Wins Journal**: Celebrate completions

---

**Remember**: Habit tracking is about progress, not perfection. Your brain works differently, and that's okay. Build a system that encourages you, not one that shames you. 🌟
