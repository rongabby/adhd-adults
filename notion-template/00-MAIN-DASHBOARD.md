# ADHD Flow OS - Main Dashboard Structure

## Overview
This file describes the complete structure of the ADHD Flow OS main dashboard page in Notion. Use this as a blueprint to build your template.

---

## Page Properties
- **Icon**: 🧠✨
- **Cover**: Gradient background (soft lavender to mint green)
- **Cover Position**: Center

---

## 1. Header Section (Full Width)

### Callout Block - Brand Header
```
🧠✨ ADHD Flow OS
Dopamine-friendly | Forgiving | Visual | AI-Powered Coach

Built for neurospicy brains that need visual cues, gentle reminders, and AI support.
```
- **Background Color**: Light purple (#E6E6FA)
- **Text Size**: Large
- **Style**: Callout with icon

---

## 2. Quick Stats Bar (Synced Block)

Create a synced block named: "Quick Stats Header"

**Three-Column Layout**:

### Column 1: Today's Energy
```
⚡ Energy Level: [1-10 slider or select]
Link to: Today's Mood Tracker Entry
```

### Column 2: Current Focus
```
🎯 Today's Mission:
[Editable text property]
"What matters most today?"
```

### Column 3: Today's Wins
```
🏆 Wins Today: [Counter]
[Linked database view showing completed tasks]
```

---

## 3. Navigation Hub (Full Width)

### Row 1: Primary Actions
Create colorful button/callout blocks:

```
📅 TODAY          🏆 WEEKLY OVERVIEW     ⚡ QUICK CAPTURE
↓                 ↓                       ↓
Daily Page        Weekly Review Page      Brain Dump Database
```
- **Color**: Sky Blue (#87CEEB)

### Row 2: Core Features
```
🔥 HYPERFOCUS ZONE    ❤️ WELLNESS & MOOD     💡 SECOND BRAIN
↓                     ↓                       ↓
Hyperfocus Page       Mood Tracker            Knowledge Vault
```
- **Color**: Coral (#FF6B6B) | Pink (#FFB6C1) | Purple (#A78BFA)

### Row 3: Life Management
```
💰 FINANCES HUB       🏠 LIFE AREAS          📊 ALL TASKS
↓                     ↓                       ↓
Financial Hub         Life Areas Hub          Tasks Database
```
- **Color**: Yellow (#FFE66D) | Green (#98FB98) | Teal (#4ECDC4)

---

## 4. Main Dashboard Body (Three-Column Layout)

### Left Column (30% width): TODAY AT A GLANCE

#### Daily Focus Mission
```
🎯 Today's Mission
[Large editable text field]

What's the ONE thing that would make today feel successful?
```

#### Top Priorities for Today
- **Type**: Linked Database View (Tasks)
- **Filter**: 
  - Due Date = Today OR Status = "In Progress"
- **Sort**: Priority (High → Low)
- **View Type**: List or Board
- **Properties Shown**:
  - Name
  - Priority (colored tags)
  - Energy Required
  - Status checkbox
- **Limit**: 5 items
- **Button**: "+ Add Priority Task"

#### Energy & Body Check-In (Toggle)
```
❤️ How Am I Doing?

☐ Took meds
☐ Ate something
☐ Hydrated
☐ Moved body

Mood: 😄 😊 😐 😔 😢 (select)
Energy: ⚡⚡⚡ (select 1-3)

[Link to full mood tracker entry]
```

#### Quick Wins Tracker
```
🎉 Quick Wins Today

☐ [Achievement 1]
☐ [Achievement 2]
☐ [Achievement 3]

Even tiny wins count! 🌟
```

---

### Center Column (40% width): ACTION CENTER

#### Brain Dump Inbox
```
🧠 Brain Dump Zone
Got thoughts bouncing around? Park them here!

[Button: "Dump a Thought" → Opens Brain Dump database]

Recent captures:
[Linked database view showing last 5 unprocessed items]
```

#### Quick-Add Task Buttons
```
➕ Quick Add:

[Button: "📋 Work Task"]
[Button: "🏃 Errand"]  
[Button: "💡 Idea"]
[Button: "📞 Call/Email"]

(Each button creates a task with pre-filled tags)
```

#### Habit Streak Dashboard
- **Type**: Linked Database View (Habits)
- **View Type**: Gallery or Board
- **Properties Shown**:
  - Name (with emoji)
  - Current Streak (🔥 counter)
  - Last Completed date
  - Frequency
- **Filter**: Show active habits only
- **Sort**: Current Streak (High → Low)
- **Button**: "+ Add New Habit"

#### Pomodoro / Focus Timer
```
⏱️ Focus Timer

[Embed: Simple timer or link to timer app]

Quick Sessions:
• 5 min break
• 15 min task
• 25 min Pomodoro
• 45 min deep work
```

#### AI Coach Quick Access (Callout Blocks)
```
✨ Need AI Help?

[Purple Callout: "🚀 Help Me Start" → Link to prompt]
[Purple Callout: "💪 Motivate Me" → Link to prompt]
[Purple Callout: "🧠 Break This Down" → Link to prompt]
[Purple Callout: "📚 Browse All Prompts" → Link to AI Library]
```

---

### Right Column (30% width): SUPPORT & REWARDS

#### Distraction Parking Lot
```
🐿️ Squirrel! Distraction Parking

[Quick capture field or toggle list]

Random thoughts that want attention:
• 
• 
• 

Process later during review time!
```

#### Rewards Shop
```
🎁 Rewards Shop

Current Points: [Number] 🌟

| Reward | Points | Claim |
|--------|--------|-------|
| 5-min break | 10 | ☐ |
| Favorite snack | 20 | ☐ |
| 15-min fun time | 30 | ☐ |
| Special treat | 50 | ☐ |
| Big reward | 100 | ☐ |

[Button: "Customize Rewards"]
```

#### Daily Affirmation / Quote
```
💫 Today's Reminder

[Rotating quote or affirmation]

"Progress over perfection. You're doing better than you think."

[Button: "Get New Quote"]
```

#### Quick Links & Resources
```
🔗 Quick Access

• [Goblin.tools](https://goblin.tools) - ADHD task helper
• [Focus Music Playlist]
• [Calm/Meditation App]
• [Body Doubling Co-working]
• [Emergency Contact]

[Button: "Add Custom Link"]
```

---

## 5. Collapsible Sections (Bottom)

### Toggle: Weekly Planning & Review
```
📅 Weekly Planning Hub

[Link to current week's page]
[Link to weekly template]
[Button: "Start This Week's Review"]
```

### Toggle: Life Areas Hub
```
🏠 Life Areas

Grid of linked pages:
📊 Career & Work
💰 Finances
❤️ Health & Wellness
🤝 Relationships
🏡 Home & Space
🎨 Hobbies & Creativity
📚 Learning & Growth
✈️ Travel & Adventure
```

### Toggle: Reflection & Archives
```
📖 Reflection & Journal Archive

• [Daily Journal entries database]
• [Weekly reviews archive]
• [Monthly reflections]
• [Quarterly reviews]
• [Annual review]
```

### Toggle: System Settings & Customization
```
⚙️ Customize Your System

• [How to Use This Dashboard]
• [Customization Guide]
• [Color Scheme Options]
• [Add/Remove Features]
• [AI Prompts Guide]
• [Troubleshooting]
• [Support & Community]
```

---

## Design Specifications

### Color Palette
- **Background**: Light lavender (#E6E6FA) or soft mint (#F0FFF0)
- **High Priority/Energy**: Coral (#FF6B6B)
- **Medium Priority**: Teal (#4ECDC4)
- **Low Priority/Rest**: Sage green (#95E1D3)
- **AI Features**: Purple (#A78BFA)
- **Completed/Archived**: Gray (#9CA3AF)

### Typography
- **Headers (H1)**: Large, bold, 28-32px equivalent
- **Subheaders (H2)**: Medium, 20-24px equivalent
- **Body Text**: 16-18px, comfortable reading size
- **Small Text**: 14px minimum for ADHD readability

### Spacing
- **Between Sections**: 24-32px vertical spacing
- **Within Sections**: 12-16px spacing
- **Button Padding**: Generous (mobile-friendly)

### Mobile Considerations
- Three-column layout stacks to single column on mobile
- All buttons remain large and tappable (44px minimum)
- Collapsible sections minimize scrolling
- Most-used features appear at top

---

## Implementation Notes

1. **Start with the header and navigation** - These provide orientation
2. **Build one column at a time** - Test each section before moving on
3. **Add sample data** - Makes the template immediately useful
4. **Test on mobile** - Ensure everything works on phone
5. **Use synced blocks** for elements that repeat across pages
6. **Keep it simple** - Can always add complexity later

---

## Database Relations to Set Up

This dashboard connects to these databases (create these separately):
- Tasks Database → Projects, Tags, Energy Levels
- Habits Database → Category, Frequency
- Mood Tracker → Daily Page relation
- Brain Dump → Tasks (for processing)
- Projects → Tasks (one-to-many)
- Life Areas → Tasks, Projects, Notes

See individual database structure files for full specifications.

---

**Remember**: This is YOUR system. Customize it to match your brain! Start with what you need most, and build from there. 🎨✨
