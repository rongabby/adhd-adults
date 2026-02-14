# Second Brain / Knowledge Vault Structure

## Overview
A simplified PARA-based system for capturing, organizing, and retrieving information. Designed to work with ADHD brains that need quick capture and visual organization.

---

## Database Structure

This uses 4 main databases connected together:

1. **Quick Capture / Inbox** (Everything starts here)
2. **Projects** (Active things with deadlines)
3. **Areas** (Ongoing responsibilities)
4. **Resources** (Reference material)
5. **Archives** (Completed/inactive items)

---

## Database 1: Quick Capture Inbox

### Properties

#### 1. Title (Title)
- **Type**: Title
- **Description**: Quick capture of thought/note/link
- **Examples**: "Research about X", "Idea for project", "Interesting article"

#### 2. Type (Select)
- **Type**: Select
- **Options**:
  - 📝 **Note** - Text-based information
  - 💡 **Idea** - Creative thoughts, brainstorms
  - 🔗 **Link** - Website, article, video
  - 📄 **Document** - File or document reference
  - ❓ **Question** - Something to explore
  - ✅ **To Process** - Needs filing

#### 3. Captured Date (Created time)
- **Type**: Created time
- **Automatic**: Yes

#### 4. Processed (Checkbox)
- **Type**: Checkbox
- **Description**: Have you filed this somewhere?

#### 5. Move To (Select)
- **Type**: Select
- **Description**: Where does this belong?
- **Options**:
  - 🎯 Project
  - 🏠 Area
  - 📚 Resource
  - 🗃️ Archive
  - 🗑️ Delete

#### 6. Content (Text)
- **Type**: Text (Long)
- **Description**: Full note or details

#### 7. Tags (Multi-select)
- **Type**: Multi-select
- **Options**: Custom to your life
- **Examples**: work, health, ideas, learning, creative, finance, etc.

---

## Database 2: Projects

### What Qualifies as a Project
- Has a defined end goal
- Multiple steps required
- Has a deadline (even if self-imposed)
- Will eventually be "done"

### Properties

#### 1. Project Name (Title)
- **Type**: Title
- **Example**: "Plan vacation", "Launch website", "Renovate kitchen"

#### 2. Status (Select)
- **Type**: Select
- **Options**:
  - 🟢 **Active** - Currently working on
  - 🟡 **On Hold** - Paused temporarily
  - 🔴 **Stuck** - Blocked/need help
  - ✅ **Completed** - Done!
  - ❌ **Cancelled** - No longer pursuing

#### 3. Area (Relation)
- **Type**: Relation to Areas database
- **Description**: Which life area does this support?

#### 4. Start Date (Date)
- **Type**: Date

#### 5. Target Completion (Date)
- **Type**: Date
- **Description**: When do you want this done?

#### 6. Priority (Select)
- **Type**: Select
- **Options**:
  - 🔴 High
  - 🟡 Medium
  - 🟢 Low

#### 7. Progress (Select)
- **Type**: Select
- **Options**:
  - 🌱 Just Started (0-25%)
  - 🌿 Making Progress (25-50%)
  - 🌳 Well Underway (50-75%)
  - 🌸 Nearly Done (75-99%)
  - ✅ Complete (100%)

#### 8. Next Action (Text)
- **Type**: Text
- **Description**: What's the very next step?
- **Critical**: Always know the next action!

#### 9. Notes & Resources (Text)
- **Type**: Text (Long)
- **Description**: Details, links, thoughts

#### 10. Related Tasks (Relation)
- **Type**: Relation to Tasks database
- **Description**: Link all tasks for this project

#### 11. Related Notes (Relation)
- **Type**: Relation to Resources database
- **Description**: Link relevant reference material

---

## Database 3: Areas (Ongoing Responsibilities)

### What Qualifies as an Area
- No end date (ongoing)
- Standard of maintenance required
- Part of your life roles/responsibilities
- Examples: Health, Career, Home, Finances

### Properties

#### 1. Area Name (Title)
- **Type**: Title
- **Examples**: "Physical Health", "Career Development", "Home Management"

#### 2. Vision/Goal (Text)
- **Type**: Text
- **Description**: What does success look like here?
- **Example**: "Feel energized and strong" for Physical Health

#### 3. Current Status (Select)
- **Type**: Select
- **Options**:
  - 🟢 **Thriving** - Going well
  - 🟡 **Maintaining** - Steady state
  - 🟠 **Needs Attention** - Slipping
  - 🔴 **Crisis Mode** - Requires focus

#### 4. Active Projects (Relation)
- **Type**: Relation to Projects database
- **Description**: What projects support this area?

#### 5. Related Tasks (Relation)
- **Type**: Relation to Tasks database
- **Description**: Recurring tasks for this area

#### 6. Resources (Relation)
- **Type**: Relation to Resources database
- **Description**: Important info for this area

#### 7. Review Frequency (Select)
- **Type**: Select
- **Options**:
  - Weekly
  - Monthly
  - Quarterly
  - As needed

#### 8. Last Reviewed (Date)
- **Type**: Date

#### 9. Notes (Text)
- **Type**: Text (Long)
- **Description**: Ongoing thoughts and tracking

---

## Database 4: Resources (Reference Library)

### What Qualifies as a Resource
- Reference material you might need later
- Learning resources
- Templates and how-tos
- Inspiration and ideas

### Properties

#### 1. Resource Title (Title)
- **Type**: Title
- **Examples**: "Sourdough recipe", "Marketing tips", "Design inspiration"

#### 2. Type (Select)
- **Type**: Select
- **Options**:
  - 📄 **Article** - Written content
  - 🎥 **Video** - Tutorial or talk
  - 📚 **Book** - Book notes or quotes
  - 🎙️ **Podcast** - Episode notes
  - 🔧 **Tool/Template** - Useful resource
  - 💡 **Inspiration** - Ideas collection
  - 📖 **Course/Learning** - Educational material
  - 📊 **Reference Data** - Facts/info to look up

#### 3. Category (Multi-select)
- **Type**: Multi-select
- **Options**: Custom to your interests
- **Examples**: work-skills, health-wellness, creative-projects, adhd-tips, finance-info

#### 4. Area (Relation)
- **Type**: Relation to Areas database
- **Description**: Which life area does this support?

#### 5. URL/Link (URL)
- **Type**: URL
- **Description**: Link to external resource

#### 6. Status (Select)
- **Type**: Select
- **Options**:
  - 📥 **To Review** - Haven't looked at yet
  - 📖 **In Progress** - Currently reading/watching
  - ✅ **Completed** - Finished
  - ⭐ **Reference** - Keep for lookup

#### 7. Key Takeaways (Text)
- **Type**: Text (Long)
- **Description**: What you learned or want to remember

#### 8. Date Added (Created time)
- **Type**: Created time

#### 9. Tags (Multi-select)
- **Type**: Multi-select
- **Options**: Custom tags for easy search

#### 10. Rating (Select)
- **Type**: Select
- **Options**:
  - ⭐⭐⭐⭐⭐ Excellent
  - ⭐⭐⭐⭐ Good
  - ⭐⭐⭐ Okay
  - ⭐⭐ Meh
  - ⭐ Not useful

---

## Database 5: Archives

### Properties
- **Same as original database** (Projects, Areas, or Resources)
- **Plus**: Archived Date
- **Plus**: Reason Archived (completed, no longer relevant, etc.)

### When to Archive
- Projects: When completed or cancelled
- Areas: When life role changes (graduated from school, changed jobs, etc.)
- Resources: When information is outdated or no longer useful
- Keep at least 3 months before deleting (in case you need to reference)

---

## Key Views

### Quick Capture Views

#### View 1: Inbox to Process
- **Filter**: Processed = No
- **Sort**: Captured Date (newest first)
- **Use**: Daily processing routine

#### View 2: By Type
- **Group**: Type
- **Filter**: Processed = No
- **Use**: Process similar items together

---

### Projects Views

#### View 1: Active Projects (Board)
- **Filter**: Status = Active
- **Board Columns**: Priority or Progress
- **Sort**: Target Completion Date

#### View 2: Stuck Projects (List)
- **Filter**: Status = Stuck
- **Highlight**: These need attention or help

#### View 3: Projects by Area (Board)
- **Board Columns**: Area
- **Filter**: Status = Active
- **Use**: See project balance across life areas

---

### Areas Views

#### View 1: All Areas (Gallery)
- **Display**: Large cards
- **Properties**: Vision, Status, Active Projects count
- **Use**: Life at a glance

#### View 2: Needs Attention (List)
- **Filter**: Status = Needs Attention OR Crisis Mode
- **Sort**: Last Reviewed (oldest first)

---

### Resources Views

#### View 1: Reading List
- **Filter**: Type = Article OR Book
- **Filter**: Status = To Review
- **Sort**: Date Added

#### View 2: By Category (Board)
- **Board Columns**: Category
- **Use**: Browse by topic

#### View 3: Best Resources (Gallery)
- **Filter**: Rating = 4 or 5 stars
- **Use**: Quick reference to best content

---

## Quick Capture Workflow

### Daily (5 minutes)
1. Throughout day: Dump everything into Inbox
2. Don't organize while capturing (breaks flow)
3. Use mobile app for quick captures on the go

### Weekly Processing (15-30 minutes)
1. Open "Inbox to Process" view
2. For each item, ask: "Where does this belong?"
   - **Project**: Active goal-oriented work
   - **Area**: Ongoing responsibility
   - **Resource**: Reference for later
   - **Archive**: Done/no longer relevant
   - **Delete**: Not useful
3. Move or link to appropriate database
4. Check "Processed" box
5. Clear inbox to zero (feels good!)

---

## Project Management Workflow

### Starting a Project
1. Create project entry
2. Define next action (first step)
3. Link to Area it supports
4. Add any related resources
5. Create initial tasks in Tasks database

### Weekly Project Review
1. Check "Active Projects" view
2. Update progress for each
3. Update "Next Action" field
4. Move stuck projects to "On Hold" or get help
5. Archive completed projects

---

## Area Maintenance

### Quarterly Area Review
1. Review each life area
2. Update current status
3. Check if vision/goals still align
4. Archive completed projects in this area
5. Start new projects to support area health

---

## Integration with Main System

### Link to Dashboard
- **Quick Capture button** on homepage
- **Active Projects** view embedded
- **Areas overview** in Life Areas hub

### Link to Tasks Database
- Tasks can link to Projects
- Tasks can link to Areas
- Tasks can reference Resources

### Link to Daily Pages
- Embed quick capture form
- Show today's project next actions
- Link daily notes to relevant areas

---

## ADHD-Friendly Features

### Visual Organization
- Color-coded by status
- Emoji icons for types
- Progress indicators
- Gallery views for scanning

### Low Friction Capture
- One-click inbox entry
- No required fields except title
- Process later, not during capture
- Mobile-friendly

### Forgiveness Built-In
- "Stuck" status is valid
- Can archive without completing
- Resources can be "Meh" (that's data!)
- Processing backlog is expected

### Search-Friendly
- Comprehensive tagging
- Multiple views per database
- Relations connect everything
- Full-text search works across all

---

## Customization Tips

### Common Areas People Track
- 💼 Career & Work
- ❤️ Physical Health
- 🧠 Mental Health
- 💰 Finances
- 🏠 Home & Environment
- 👨‍👩‍👧 Family & Relationships
- 🎨 Hobbies & Creativity
- 📚 Learning & Growth
- ✈️ Travel & Adventure
- 🌍 Community & Service

### Custom Resource Categories
Adjust to your interests:
- Professional: industry-news, skills, networking
- Personal: recipes, home-projects, travel-ideas
- ADHD: strategies, tools, accommodations
- Creative: inspiration, tutorials, techniques

### Project Templates
Create templates for recurring project types:
- Event planning template
- Content creation template
- Home project template
- Learning project template

---

## Maintenance Schedule

### Daily (2 minutes)
- Capture to inbox as needed

### Weekly (15 minutes)
- Process inbox to zero
- Update project next actions
- Archive completed items

### Monthly (30 minutes)
- Review all active projects
- Check areas needing attention
- Archive old resources

### Quarterly (1 hour)
- Deep area review
- Archive completed projects
- Clean up categories/tags
- Adjust system to current needs

---

**Remember**: This is a living system. It should reduce mental load, not add to it. Start simple with just inbox + one area, then expand as needed. 🧠✨
