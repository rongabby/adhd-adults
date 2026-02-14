# ADHD Flow OS - Notion Dashboard Structure

## Design Principles

### ADHD-Specific Optimizations
- **Forgiving design**: No guilt-inducing "streak breakers" – use progress bars that reset gently
- **Visual hierarchy**: Huge headings (H1/H2), icons, dividers, callouts for key info
- **Mobile-first**: Everything works well on phone (big buttons, collapsible sections)
- **Customization ease**: Instructions page at root with "How to tweak colors/icons" guide

### Visual Design System
- **Large emojis/icons** for instant visual recognition
- **Color-coded sections**:
  - Green = energy/health
  - Blue = tasks
  - Purple = reflection
  - Coral/Orange = energy actions
  - Teal = calm tasks
- **Buttons everywhere** for one-click actions
- **Synced blocks** for repeating elements
- **Embedded AI prompt buttons** that open ChatGPT/Claude with pre-filled text

## Homepage / Main Dashboard Layout

### Top Banner / Header (Synced across pages)
```
🧠✨ ADHD Flow OS
Dopamine-friendly | Forgiving | Visual | AI-Powered Coach
```

#### Quick Stats Row (synced databases)
- Today's Energy Level (slider 1-10 emoji scale)
- Current Focus Mission (single property pull from today's page)
- Wins Today (counter or gallery of checked items)

#### Navigation Buttons (big, colorful call-to-action buttons)
- 📅 Today (links to daily page)
- 🏆 Weekly Overview
- ⚡ Quick Capture / Brain Dump
- 🔥 Hyperfocus Zone
- ❤️ Wellness & Mood
- 💡 Second Brain / Notes
- 💰 Finances Hub
- 🏠 Life Areas (collapsible sub-menu)

### Main Body - Three Column Layout

#### Left Column: Today at a Glance
**Daily Focus Mission**
- One big editable property: "What matters most today?"

**Top 3 Priorities**
- Linked view from Tasks database
- Filtered to "Today" + high priority

**Due Today / Overdue**
- Board or list view
- Color-coded urgency: red overdue, yellow today

**Energy & Body Check-In** (toggle)
- Mood emoji picker
- Energy slider
- Medication/Meals reminder checklist

**Quick Wins Tracker**
- Small gallery or checkbox list
- Reward dopamine hits

#### Center Column: Action Center
**Brain Dump Inbox**
- Simple database or text block
- Button: "Dump thoughts here → Process later"

**Task Quick-Add Buttons**
- "New Errand"
- "New Work Task"
- "Idea"
- Auto-tags & dates

**Habit Streak Dashboard**
- Progress bars or emoji chains for 3-5 core habits
- Examples: water, move, meds

**Timer / Pomodoro Embed**
- Simple Notion timer or link to browser extension

**AI Coach Buttons** (big buttons with labels)
- "Help me start this task"
- "Break this down"
- "Motivate me right now"
- Each copies a tailored prompt

#### Right Column: Gentle Reminders & Rewards
**Distraction Parking Lot**
- "Squirrel!" button dumps random thoughts here

**Rewards Shop**
- Simple table: earn points from tasks
- "Redeem" for fun activities

**Affirmations / Dopamine Quotes**
- Rotating synced block or gallery

**Quick Links**
- Icons to external tools: GoblinTools, Focus@Will, Calm, etc.

### Bottom Section (collapsible)
- Toggle: Weekly/Monthly Planning
- Toggle: Life Areas Hub (icons linking to sub-pages)
- Toggle: Reflection & Journal Archive

## Key Sub-Pages / Linked Databases

### 1. Daily Page (auto-created or duplicated template)
- Date header with weather widget
- Morning Routine Checklist (customizable toggles)
- Full Tasks Board (Kanban: To Do → Doing → Done)
- Evening Wind-Down (gratitude, wins, tomorrow's top 3)
- Embedded daily journal prompt + AI reflection button

### 2. Tasks Master Database (core engine)

#### Properties
- Name
- Priority (High/Med/Low with colors)
- Energy Required (low/medium/high)
- Due Date
- Status
- Tags (work/home/errand)
- Project relation

#### Views
- Today only (list or board)
- This Week
- Overdue
- By Energy Level (great for matching task to current state)
- Hyperfocus Queue (long tasks for deep work)

### 3. Habits Database

#### Properties
- Name
- Streak
- Frequency
- Notes

#### Views
- Calendar view + streak visuals
- Linked mini-view on homepage

### 4. Wellness / Mood Tracker Database

#### Properties
- Date
- Mood emoji
- Energy slider
- Sleep hours
- Triggers
- Medication taken Y/N

#### Features
- Trend chart (Notion charts if available) or gallery for patterns
- AI button: "Analyze my mood patterns this month"

### 5. Second Brain / Knowledge Vault

Based on simplified PARA method:
- Projects
- Areas
- Resources
- Archives

Features:
- Quick capture button on every page
- Search bar prominent

### 6. Hyperfocus Zone (dedicated page)
- Big timer
- Current deep-work task (pulled from database)
- "Protect Me" checklist (close tabs, phone away, etc.)
- Transition ritual prompts

### 7. Quarterly Reset / Life Review (seasonal page)
- Values check-in
- Big wins archive
- Next 90 days planning

## Color Palette & Visual Style

### Colors
- Soft pastel background (light mint or lavender gradient)
- Accent buttons in coral/orange for energy
- Teal/green for calm tasks
- Purple for AI features

### Typography
- Large H1/H2 headings (bold, 28-40px)
- Plenty of white space
- Rounded callouts/boards

### Icons/Emojis
- Oversized everywhere (🧠⚡❤️🔥) for instant visual scanning

### Mobile View
- Stacks vertically
- Buttons stay big/tappable

### Dopamine Elements
- Progress bars fill with color
- Confetti emojis on completion
- Gentle animations (via Notion's native features)
- No harsh reds/guilt language

## Implementation Notes

This structure keeps the initial view under 1-2 scrolls (crucial for ADHD), while allowing expansion without overwhelm. The design is inspired by successful ADHD templates from Gridfiti, Producing Paradise, and Mynd, using similar "simple dashboard → deep databases" patterns.
