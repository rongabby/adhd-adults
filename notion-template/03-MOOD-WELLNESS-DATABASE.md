# Mood & Wellness Tracker Database Structure

## Overview
Track your emotional, physical, and mental wellness patterns to understand what supports your ADHD brain best.

---

## Database Properties

### 1. Date (Date)
- **Type**: Date
- **Default**: Today
- **Description**: When did you log this entry

### 2. Mood (Select)
- **Type**: Select
- **Options**:
  - 😄 **Excellent** - Green
  - 😊 **Good** - Light green
  - 😐 **Okay/Neutral** - Yellow
  - 😔 **Low** - Orange
  - 😢 **Very Low** - Red
  - 😤 **Frustrated/Angry** - Dark red
  - 😰 **Anxious** - Purple

### 3. Energy Level (Select or Number)
- **Type**: Select
- **Options**:
  - ⚡⚡⚡⚡⚡ **5 - High Energy**
  - ⚡⚡⚡⚡ **4 - Good Energy**
  - ⚡⚡⚡ **3 - Moderate**
  - ⚡⚡ **2 - Low**
  - ⚡ **1 - Depleted**

### 4. Focus/Concentration (Select)
- **Type**: Select
- **Options**:
  - 🎯🎯🎯 **Sharp**
  - 🎯🎯 **Decent**
  - 🎯 **Scattered**
  - 🌀 **Brain Fog**

### 5. Sleep Quality (Select)
- **Type**: Select
- **Options**:
  - 😴😴😴 **Great Sleep**
  - 😴😴 **Decent Sleep**
  - 😴 **Poor Sleep**
  - 😵 **Terrible Sleep**

### 6. Sleep Hours (Number)
- **Type**: Number
- **Description**: Actual hours slept

### 7. ADHD Meds Taken (Checkbox)
- **Type**: Checkbox
- **Label**: "Took ADHD medication as prescribed"

### 8. Other Meds/Supplements (Text)
- **Type**: Text
- **Description**: Any other medications or supplements taken

### 9. Meals Eaten (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 🍳 Breakfast
  - 🥗 Lunch
  - 🍽️ Dinner
  - 🍎 Snacks
  - ❌ Skipped meals

### 10. Hydration (Select)
- **Type**: Select
- **Options**:
  - 💧💧💧 **Well hydrated** (8+ glasses)
  - 💧💧 **Adequate** (4-7 glasses)
  - 💧 **Not enough** (1-3 glasses)
  - 🏜️ **Dehydrated** (none)

### 11. Exercise/Movement (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 🏃 Cardio
  - 💪 Strength
  - 🧘 Yoga/Stretch
  - 🚶 Walk
  - 🏠 General movement
  - ❌ No exercise today

### 12. Time Outside (Select)
- **Type**: Select
- **Options**:
  - ☀️ 60+ minutes
  - 🌤️ 30-60 minutes
  - ⛅ 10-30 minutes
  - 🏠 None (indoor day)

### 13. Social Interaction (Select)
- **Type**: Select
- **Options**:
  - 👥👥👥 **Lots of social time**
  - 👥👥 **Moderate social**
  - 👥 **Minimal social**
  - 🏠 **Alone all day**

### 14. Stressors/Triggers (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 💼 Work stress
  - 💰 Money worries
  - 👨‍👩‍👧 Relationship issues
  - 📰 World news
  - 😴 Poor sleep
  - ⏰ Time pressure/Deadlines
  - 🔊 Sensory overload
  - 🥺 RSD episode
  - ⚠️ Other (note in text)

### 15. Wins/Highlights (Text)
- **Type**: Text
- **Description**: What went well today? Any accomplishments?
- **Template**: Even tiny wins count!

### 16. Challenges/Struggles (Text)
- **Type**: Text
- **Description**: What was hard today?
- **No judgment zone**

### 17. Sensory Input (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 🎵 Listened to music
  - 🎧 Used noise-cancelling
  - 🧸 Fidget toys
  - 🛀 Bath/shower
  - 🕯️ Aromatherapy
  - 🧥 Weighted blanket
  - ☕ Caffeine
  - 🍫 Comfort food

### 18. Coping Strategies Used (Multi-select)
- **Type**: Multi-select
- **Options**:
  - 📝 Journaling
  - 🧘 Meditation/Breathing
  - 💬 Talked to someone
  - 🚶 Went for a walk
  - 🎨 Creative outlet
  - 📱 Used AI prompt
  - 📺 Distraction/Entertainment
  - 😴 Nap/Rest

### 19. Productivity Level (Select)
- **Type**: Select
- **Options**:
  - 🚀 **High** - Got lots done
  - ✅ **Moderate** - Some things done
  - 🐢 **Low** - Barely anything
  - 🛌 **Rest Day** - Intentional rest

### 20. RSD Episodes (Checkbox)
- **Type**: Checkbox
- **Label**: "Experienced rejection sensitivity today"
- **Note field**: What triggered it?

### 21. Hyperfocus Occurred (Checkbox)
- **Type**: Checkbox
- **Label**: "Had a hyperfocus session"
- **Note field**: On what? For how long?

### 22. Overall Day Rating (Select)
- **Type**: Select
- **Options**:
  - ⭐⭐⭐⭐⭐ **5 - Excellent Day**
  - ⭐⭐⭐⭐ **4 - Good Day**
  - ⭐⭐⭐ **3 - Okay Day**
  - ⭐⭐ **2 - Rough Day**
  - ⭐ **1 - Very Hard Day**

### 23. Notes/Journal (Text)
- **Type**: Text (Long)
- **Description**: Free-form reflection space

### 24. Gratitude (Text)
- **Type**: Text
- **Description**: One thing you're grateful for today (optional)

---

## Database Views

### View 1: Today's Check-In (Form)
**Purpose**: Quick daily logging

**Display**: All essential fields in a simple form

**Properties Shown**:
- Date (auto-filled)
- Mood
- Energy Level
- Meds Taken
- Meals Eaten
- Sleep Hours/Quality
- Quick wins
- Overall day rating

---

### View 2: This Week (Timeline)
**Purpose**: See patterns at a glance

**Filter**: Date is within last 7 days

**Sort**: Date (newest first)

**Layout**: Timeline or List

**Properties Shown**:
- Date
- Mood emoji
- Energy level
- Sleep quality
- Meds taken
- Overall rating

**Color code**: By mood

---

### View 3: Mood Calendar (Calendar)
**Purpose**: Visual monthly view

**Date Property**: Date

**Color**: By Overall Day Rating

**Properties Shown**:
- Mood
- Energy
- Sleep hours
- Brief highlights

---

### View 4: Pattern Analysis (Table)
**Purpose**: Identify correlations

**Filter**: Last 30 days

**Sort**: Date

**Properties Shown**: All

**Group By**: Mood or Energy Level

**Use**: Export to analyze patterns

---

### View 5: Good Days (Gallery)
**Purpose**: Remind yourself what works

**Filter**:
- Overall Day Rating is 4 or 5
- Date is within last 30 days

**Sort**: Date (newest first)

**Properties Shown**:
- Date
- Mood
- Energy
- What made it good (highlights)
- Sleep, exercise, social

**Display**: Celebrate patterns!

---

### View 6: Rough Days (List)
**Purpose**: Learn from challenges

**Filter**:
- Overall Day Rating is 1 or 2
- Date is within last 30 days

**Sort**: Date (newest first)

**Properties Shown**:
- Date
- Mood
- Stressors/Triggers
- Challenges
- What helped (if anything)

**Use**: Identify warning signs

---

### View 7: Sleep Tracker (Chart)
**Purpose**: Track sleep patterns

**Filter**: Last 30 days

**Properties**: Sleep Hours, Sleep Quality

**Display**: Chart or graph (if available)

---

### View 8: Medication Adherence (List)
**Purpose**: Track med consistency

**Filter**: Last 14 days

**Properties Shown**:
- Date
- ADHD Meds Taken (checkbox)
- Mood
- Energy
- Focus/Concentration

**Highlight**: Days when meds were missed

---

## Quick Entry Templates

### Template 1: Morning Check-In
```
Date: [Today]
Mood: [How do you feel waking up?]
Energy Level: [Starting energy]
Sleep Hours: [Last night]
Sleep Quality: [How was it?]
Meds Taken: ☐
```

### Template 2: Evening Reflection
```
Date: [Today]
Overall Day Rating: [1-5 stars]
Wins/Highlights: [What went well?]
Challenges: [What was hard?]
Gratitude: [One thing you're grateful for]
Tomorrow's Intention: [One focus for tomorrow]
```

### Template 3: Energy Dip Check-In
```
Time: [Current time]
Energy Level: [Current state]
Mood: [How feeling now]
Last meal: [When did you eat?]
Last water: [When did you hydrate?]
Need: [What might help?]
```

---

## Integration with Dashboard

### Pull Into Daily Dashboard
- **Today's Check-In button** - Opens form
- **Yesterday's entry** - Quick reference
- **Current energy level** - Live indicator

### Link to Other Databases
- **Tasks**: Energy-matched task suggestions
- **Habits**: Habit completion affects mood
- **Daily Pages**: Embed today's mood entry

---

## AI Analysis Prompts

### Button 1: "Analyze My Patterns"
```
Here's my mood/energy data from the past [TIMEFRAME]:
[Export and paste data]

Please help me identify:
- Patterns in my good vs bad days
- What correlates with high/low energy
- Sleep impact on mood and focus
- Medication consistency effects
- Best times of day for different tasks
```

### Button 2: "What's Affecting Me?"
```
I'm feeling [MOOD] today and I'm not sure why.

My data for the past few days:
[Paste recent entries]

Can you help me identify:
- Possible triggers
- Changes from my good days
- What might be missing
- Suggestions to feel better
```

---

## Wellness Patterns to Watch

### Positive Correlations to Track
- Sleep hours → Energy level
- Meds taken → Focus quality
- Exercise → Mood
- Social time → Energy (for your type)
- Time outside → Overall rating

### Warning Signs
- Consecutive poor sleep days
- Multiple skipped meals
- High stress + low coping strategies
- Downward mood trend
- Decreased med adherence

---

## ADHD-Specific Insights

### What to Track Extra
- **Hyperfocus**: When it happens, what triggers it
- **RSD episodes**: Frequency and triggers
- **Medication effects**: Onset, duration, crash
- **Stimulation needs**: Under vs over stimulated
- **Executive function**: Good vs bad days

### What Matters for ADHD
- **Consistency over perfection**: Track most days, not all
- **No guilt logging**: Just data, no judgment
- **Short entries valid**: Something > nothing
- **Patterns > individual days**: Look at trends

---

## Privacy & Sharing

### Keep Private
- Medical information
- Medication details
- Personal struggles
- Mental health data

### Safe to Share
- General patterns (if you want)
- Tips that work for you
- Anonymous data for support groups
- With healthcare providers (your choice)

---

## Maintenance

### Daily
- Quick check-in (2 minutes)
- Note mood + energy at minimum

### Weekly
- Review the week's pattern
- Note any significant changes
- Adjust strategies based on data

### Monthly
- Look at overall trends
- Celebrate improvements
- Identify areas needing support
- Share relevant data with doctor if needed

---

## Customization Ideas

### Add Your Own Properties
- **Menstrual cycle tracking** (affects ADHD symptoms)
- **Weather/barometric pressure** (affects some people)
- **Screen time** (correlation with sleep/mood)
- **Creative output** (energy for different work)
- **Pain levels** (chronic conditions)

### Create Custom Views
- **By day of week** - See weekly patterns
- **By season** - Seasonal affective disorder
- **By project phases** - Work stress correlation
- **Medication changes** - Track adjustment periods

---

**Remember**: This data is for YOU. Track what's useful, skip what's not. The goal is insight and self-compassion, not perfect logging. 💜
