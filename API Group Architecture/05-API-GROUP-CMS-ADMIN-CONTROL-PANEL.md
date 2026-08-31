# 05 — API GROUP CMS ADMIN CONTROL PANEL

## PURPOSE

The API Group website must be manageable by an administrator who has no coding experience.

The administrator must be able to create, edit, organize, publish, display, and connect information through a visual control panel.

The CMS is the management layer between the database and the public website.

The administrator should not need to edit HTML, CSS, JavaScript, database queries, or source code to perform normal website operations.

---

# 1. ADMINISTRATOR-FIRST DESIGN

The CMS must be designed for a non-technical administrator.

The administrator should be able to understand:

- What content exists
- Where it appears
- How it is categorized
- What it is connected to
- How it is displayed
- Whether it is published
- Whether it is featured

The system should use visual controls, forms, menus, previews, drag-and-drop where useful, and clearly labeled settings.

---

# 2. ADMIN LOGIN

The website must provide secure administrator authentication.

The administrator should be able to:

- Log in
- Log out
- Reset a password
- Manage their account
- Access the control panel
- Be denied access to administrative functions when not authenticated

Administrative functions must not be exposed through the public website.

---

# 3. ADMIN CONTROL PANEL

The control panel should provide access to major management areas such as:

- Dashboard
- Profiles
- Articles
- Records
- Categories
- Relationships
- Media
- Templates
- Navigation
- Sidebars
- Search
- Featured Content
- Site Settings
- Users / Permissions
- Publishing
- Revision History

The exact menu may change as the system develops.

---

# 4. API GROUP ADMINISTRATION IS SEPARATE

The API Group control panel must be independent from the Monster News control panel.

API Group administration manages:

- API Group Library
- API Group Profiles
- API Group records
- API Group navigation
- API Group templates
- API Group sidebars
- API Group branding
- API Group content

Monster News administration manages:

- Monster News articles
- Monster News categories
- Monster News layouts
- Monster News templates
- Monster News navigation
- Monster News branding
- Monster News sidebars
- Monster News publishing

Neither administration system should accidentally overwrite the other.

---

# 5. DASHBOARD

The API Group administrator dashboard should provide an overview of the system.

Possible dashboard information:

- Recently added profiles
- Recently edited profiles
- Recently published articles
- Draft content
- Featured content
- Unreviewed AI submissions
- Missing information
- Recent database changes
- Content requiring attention

The dashboard should provide quick actions such as:

- Add Profile
- Add Article
- Add Record
- Add Category
- Add Relationship
- Upload Media
- Create Template

---

# 6. CREATE A PROFILE

The administrator should be able to create a new profile through a visual form.

Example:

PROFILE TYPE
Personnel

NAME
Pam Deig

POSITION
Executive Director

ORGANIZATION
Housing Authority

JURISDICTION
White County

CITY
Carmi

IMAGE
Upload image

SOURCE
Add source

The administrator saves the record.

The CMS creates the database entity.

The appropriate profile page becomes available automatically.

---

# 7. PROFILE CREATION MUST NOT REQUIRE PAGE CREATION

Creating a new profile must not require the administrator to:

- Create a webpage
- Copy an old webpage
- Write HTML
- Create navigation code
- Create a new URL manually
- Add the profile to a hard-coded list

The CMS should generate the public presentation from the database and assigned template.

---

# 8. CREATE A NEW COUNTY

The same principle applies to jurisdictions.

If White County exists and another county is missing, the administrator should be able to create the missing county as a database entity.

Example:

CREATE PROFILE

Type:
County

Name:
Example County

State:
Illinois

The CMS should then automatically make that county available to applicable:

- County directories
- Sidebars
- Search
- Related profiles
- Breadcrumbs
- Agency relationships
- Personnel relationships

---

# 9. DATABASE-DRIVEN LISTS

Lists must be generated from database queries.

The administrator should never have to manually maintain a list such as:

White County
Edgar County
Vermilion County

If a new county is added to the database, it should automatically appear in every configured location where the county list is used.

The same applies to:

- Agencies
- Personnel
- Cities
- Villages
- Civic organizations
- Other entities

---

# 10. RELATIONSHIP MANAGEMENT

The administrator must be able to connect entities without coding.

Example:

Pam Deig

Add Relationship:

WORKS FOR
→ Housing Authority

ASSOCIATED WITH
→ White County

HOLDS POSITION
→ Executive Director

ASSOCIATED WITH
→ City of Carmi

The relationship should be stored in the database.

The system should then be able to display that relationship automatically wherever the appropriate template requests it.

---

# 11. RELATIONSHIPS ARE NOT MANUAL LINKS

A relationship should not simply be stored as a manually typed hyperlink.

For example:

Do not treat:

"Pam Deig — Housing Authority"

as merely text.

Instead store:

PERSON:
Pam Deig

RELATIONSHIP:
works_for

ENTITY:
Housing Authority

This allows the system to:

- Search it
- Display it
- Reverse it
- Filter it
- Reference it
- Use it in sidebars
- Use it in articles
- Use it in profiles
- Update it centrally

---

# 12. REVERSE RELATIONSHIPS

Relationships should be usable in both directions.

If:

Pam Deig
→ works_for
→ Housing Authority

then the Housing Authority profile should be able to display:

Personnel
→ Pam Deig

The administrator should not have to enter the relationship twice.

---

# 13. AUTOMATIC NAVIGATION UPDATES

When database entities are added, applicable navigation should update automatically.

Example:

Administrator adds:

New County

The CMS should automatically make it available in configured:

- County directories
- County sidebars
- Search
- Related content
- Breadcrumbs
- Filters

No coding should be required.

---

# 14. CATEGORY MANAGEMENT

The administrator should be able to create and manage categories.

A category may contain:

- Articles
- Resources
- Records
- Other content types

Categories should not be confused with database relationships.

A category organizes content.

A relationship connects entities.

---

# 15. PROFILE CLASSIFICATION

The administrator should be able to classify profiles.

Initial Agency Profile classifications:

- Federal
- State
- County
- City
- Village
- Civic

The system should allow additional classifications later.

---

# 16. CATEGORY HIERARCHY

The CMS should support hierarchical categories.

A category may have:

- Parent category
- Child category
- Grandchild category
- Additional nested levels

There should be no artificial two-level limitation.

However, the public navigation should remain understandable even when the underlying hierarchy becomes deep.

---

# 17. CONTENT HIERARCHY AND DATABASE HIERARCHY ARE DIFFERENT

The administrator must be able to distinguish between:

CONTENT CATEGORIES

and

DATABASE RELATIONSHIPS.

For example:

Library
→ Agent Training

is a content hierarchy.

While:

Pam Deig
→ works_for
→ Housing Authority

is a database relationship.

The CMS must support both without confusing them.

---

# 18. ARTICLE CREATION

The administrator should be able to create articles through a visual editor.

An article should support:

- Title
- Subtitle
- Author
- Publication date
- Body
- Images
- Documents
- Categories
- Tags
- Featured status
- Related profiles
- Related records
- Sources
- References
- Draft/published status

---

# 19. ARTICLES CAN REFERENCE PROFILES

An article may reference database entities.

Example:

Article:
Housing Authority Developments in White County

Related Profiles:

- Housing Authority
- Pam Deig
- White County
- City of Carmi

The article should link to those existing profiles.

The administrator should not have to duplicate profile information inside the article.

---

# 20. PROFILE INFORMATION CAN APPEAR IN ARTICLES

The system may allow an article template to display selected information from related profiles.

For example:

PERSONNEL PROFILE
Pam Deig

could be referenced in an article with:

Name
Position
Organization
Jurisdiction
Profile link

This information should come from the database.

If the underlying profile changes, future rendered references should use the current database information where appropriate.

---

# 21. AI CONTENT INJECTION

Authorized AI systems must be capable of submitting structured data to the CMS.

AI may create:

- Profiles
- Relationships
- Records
- Articles
- Tags
- References
- Sources
- Other structured content

AI should not bypass the database architecture by creating arbitrary static webpages.

---

# 22. AI REVIEW WORKFLOW

AI-created information should support an optional review process.

Possible statuses:

- AI Draft
- Needs Review
- Approved
- Published
- Rejected
- Archived

The administrator should be able to review AI-generated information before publication.

---

# 23. BULK DATA ENTRY

The system should eventually support importing multiple records.

Possible methods:

- CSV
- Spreadsheet
- Structured JSON
- API
- AI-generated batches
- Other supported import methods

Imported records should pass through validation and duplicate detection.

---

# 24. DUPLICATE DETECTION

When creating a new entity, the CMS should identify possible duplicates.

Example:

Existing:
Pam Deig

New submission:
Pamela Deig

The system should warn:

Possible existing profile found.

The administrator can then:

- Open existing profile
- Compare
- Merge
- Create anyway
- Cancel

---

# 25. MEDIA MANAGEMENT

The CMS should include a media library.

Media may include:

- Profile photographs
- Agency logos
- Civic organization logos
- Article images
- Documents
- Other files

Media should be reusable.

The administrator should not need to upload the same image repeatedly.

---

# 26. TEMPLATE MANAGEMENT

The administrator must be able to create and modify templates without coding.

Templates may exist for:

- Agency Profiles
- Personnel Profiles
- Civic Profiles
- Jurisdiction Profiles
- Articles
- Resource pages
- Search results
- Directory pages
- Landing pages

---

# 27. VISUAL TEMPLATE BUILDER

The ideal template system should function similarly to a visual CMS/page builder.

The administrator should be able to choose components such as:

- Title
- Image
- Text
- Metadata
- Relationship list
- Search
- Database list
- Cards
- Articles
- Related profiles
- Sidebar
- Breadcrumb
- Footer

The administrator can arrange components visually.

---

# 28. TEMPLATE DATA SOURCES

Template components should be capable of receiving data from the database.

Examples:

RELATIONSHIP LIST

Source:
Current Profile

Relationship:
Personnel

Result:
All Personnel connected to the current profile

DATABASE LIST

Source:
Counties

Filter:
Illinois

Result:
All matching county entities

The administrator should configure this visually.

---

# 29. TEMPLATE REUSE

A template should be reusable.

For example:

PERSONNEL PROFILE TEMPLATE

may render:

Person A
Person B
Person C
Person D

without requiring four separate page designs.

The template controls presentation.

The database controls content.

---

# 30. PAGE LAYOUT CONTROL

The administrator should be able to select:

- Full width
- Left sidebar
- Right sidebar
- Both sidebars

for appropriate pages.

The setting should be available per:

- Page
- Category
- Template
- Content type

depending on the CMS design.

---

# 31. SIDEBAR BUILDER

The administrator should be able to visually configure a sidebar.

Example:

LEFT SIDEBAR

Section:
Illinois Counties

Component:
Database List

Source:
County Profiles

Filter:
State = Illinois

Sort:
Name

Display:
Links

The sidebar automatically displays matching database entities.

---

# 32. RIGHT SIDEBAR

The administrator may configure a right sidebar for contextual information.

Example:

PERSONNEL PROFILE

Right Sidebar:

Connections

- Agencies
- Organizations
- Jurisdictions
- Civic Organizations
- Related Personnel
- Related Articles

These lists should be generated from relationships.

---

# 33. SIDEBAR VISIBILITY

The administrator should be able to turn sidebars on or off.

Options:

NONE

LEFT

RIGHT

BOTH

The choice should not require code changes.

---

# 34. SIDEBAR INHERITANCE

The CMS should eventually support inherited layout settings.

Example:

All Personnel Profiles

→ Right Sidebar

But:

Specific Personnel Profile

→ Both Sidebars

A page-level setting can override a template-level setting.

This provides flexibility without requiring the administrator to configure every page individually.

---

# 35. NAVIGATION BUILDER

The administrator should be able to manage navigation visually.

Navigation items may be:

- Manual links
- Categories
- Database queries
- Profile types
- Dynamic lists
- Search links
- External links

The administrator should be able to reorder items.

---

# 36. DYNAMIC NAVIGATION

Dynamic navigation should be preferred for database entities.

Example:

County Profiles

should automatically list all counties.

The administrator should not have to manually add:

White County

Edgar County

Vermilion County

etc.

---

# 37. BREADCRUMB CONFIGURATION

The CMS should support breadcrumb configuration.

The administrator should be able to determine:

- Whether breadcrumbs appear
- Where they appear
- What separators are used
- What hierarchy they represent

However, profile identity must remain independent from navigation context.

---

# 38. FEATURED CONTENT

The administrator should be able to mark content:

Featured

Featured content may appear automatically on configured:

- Homepages
- Library pages
- Profile pages
- Category pages
- Landing pages

The administrator should not have to manually edit a homepage every time a featured article changes.

---

# 39. LATEST CONTENT

The CMS should automatically identify recent content.

Possible feeds:

- Latest Articles
- Latest Profiles
- Latest Records
- Recently Updated
- Recently Added

The administrator can choose which feeds appear on each page.

---

# 40. PUBLISHING

Content should support publishing states.

Possible states:

- Draft
- Review
- Scheduled
- Published
- Archived

The administrator should be able to change the state through the control panel.

---

# 41. SCHEDULING

The CMS should eventually support scheduled publishing.

An administrator may prepare an article and specify:

Publish:
Date
Time

The CMS automatically publishes it at the scheduled time.

---

# 42. REVISION HISTORY

Important content should maintain revision history.

The administrator should be able to:

- View previous versions
- Compare versions
- Restore a previous version

This is particularly important for database-driven profiles.

---

# 43. ARCHIVING

Deleting information should not always mean permanent destruction.

The system should support archiving where appropriate.

Archived records may remain available to administrators while being removed from normal public discovery.

---

# 44. PERMISSIONS

The CMS should eventually support multiple administrative roles.

Possible roles:

- Administrator
- Editor
- Contributor
- Researcher
- Reviewer
- AI Service Account

Permissions should determine what each role can:

- Read
- Create
- Edit
- Approve
- Publish
- Delete
- Manage

---

# 45. AI SERVICE ACCESS

AI systems should have controlled access to the database and CMS.

AI permissions should be configurable.

An AI system may be permitted to:

- Read profiles
- Create drafts
- Suggest relationships
- Update records
- Submit articles

Publishing permissions should be separately controllable.

---

# 46. AUDIT LOG

Administrative changes should eventually be logged.

The system should record:

- Who made the change
- What changed
- When it changed
- Previous value where appropriate
- New value
- Publication status

AI changes should also be identifiable as AI-generated or AI-assisted.

---

# 47. SEARCH MANAGEMENT

The administrator should be able to configure searchable fields.

Examples:

Personnel:

- Name
- Position
- Organization
- Jurisdiction

Agency:

- Name
- Classification
- Jurisdiction
- Department

Article:

- Title
- Body
- Topic
- Tags
- Related profiles

---

# 48. SEO AND PUBLIC URLs

The administrator should be able to manage basic public-facing metadata.

Possible fields:

- Page title
- Description
- Slug
- Social preview image
- Canonical URL

Public URLs should remain stable when possible.

---

# 49. PREVIEW

Before publishing, the administrator should be able to preview content.

Preview should show:

- Desktop layout
- Mobile layout
- Sidebar configuration
- Breadcrumbs
- Images
- Related content
- Final template

The administrator should be able to make changes and preview again without publishing.

---

# 50. LIVE EDITING GOAL

The long-term goal is that an administrator can browse a page and determine:

"This sidebar should be on the right."

or:

"This page needs no sidebar."

or:

"I want this database list here."

or:

"I want these related profiles displayed here."

The administrator should then be able to make that change through the CMS without touching source code.

---

# 51. FRONT-END EDITING

Where practical, the CMS should support front-end editing.

An authenticated administrator viewing the public site may see editing controls such as:

Edit Page
Edit Profile
Edit Sidebar
Edit Template
Add Component

The administrator should be able to make changes while viewing the actual page.

This is similar in concept to a Joomla-style frontend editing experience.

---

# 52. ADMINISTRATOR SHOULD NOT NEED TO KNOW THE DATABASE

The database architecture must remain sophisticated internally.

The administrator interface should translate that complexity into understandable controls.

Instead of requiring the administrator to understand database schemas, provide:

Add Relationship
Add Profile
Add Category
Add Record
Add Person
Add Agency
Add Jurisdiction

The CMS handles the underlying database operations.

---

# 53. CMS SAFETY

Administrative tools should prevent accidental destructive actions.

Examples:

Deleting a profile should warn about related records.

Deleting an agency should identify connected personnel.

Deleting a category should identify affected articles.

Deleting a relationship should clearly identify what connection will be removed.

---

# 54. DATA VALIDATION

The CMS should validate structured data.

Examples:

- Required profile name
- Valid relationship type
- Valid entity reference
- Valid dates
- Valid category
- Valid media reference

The system should identify errors before publishing.

---

# 55. API GROUP BRANDING SETTINGS

The API Group control panel should provide branding controls.

Possible settings:

- API Group logo
- Header logo size
- Footer logo
- Typography
- Accent colors
- Backgrounds
- Button styles
- Border styles
- Card styles

The administrator should be able to modify presentation without changing content.

---

# 56. VISUAL DESIGN REFERENCE

The existing API Group website should remain the primary visual reference.

The CMS should preserve the visual qualities that the existing site already demonstrates while providing substantially more powerful content management.

The goal is not to replace the visual identity.

The goal is to build a CMS underneath it.

---

# 57. MONSTER NEWS CONTROL PANEL

Monster News must eventually have its own independent control panel.

It should support its own:

- Article templates
- News categories
- Tags
- Navigation
- Sidebars
- Featured stories
- Latest stories
- Publishing workflow
- Branding
- Media
- Editorial tools

Monster News may reference API Group Profiles when useful.

However, Monster News administration must remain separate from API Group administration.

---

# 58. CROSS-SITE DATA REFERENCES

Although API Group and Monster News are independent, Monster News may reference API Group database entities.

Example:

Monster News Article
→ references
→ Pam Deig Profile

The article can display:

Pam Deig
Position
Organization
Profile link

The data remains owned by the API Group profile system.

Monster News does not create a second copy of the person's canonical profile.

---

# 59. FINAL CMS ARCHITECTURE

The intended architecture is:

DATABASE
↓
ENTITIES
↓
RELATIONSHIPS
↓
CONTENT
↓
TEMPLATES
↓
PAGE LAYOUT
↓
SIDEBARS
↓
NAVIGATION
↓
PUBLIC WEBSITE

The administrator controls these layers through the CMS.

The administrator should not need to write code.

---

# 60. CORE ADMINISTRATOR PRINCIPLE

THE DATABASE STORES THE INFORMATION.

THE CMS MANAGES THE INFORMATION.

THE RELATIONSHIPS CONNECT THE INFORMATION.

THE TEMPLATES PRESENT THE INFORMATION.

THE SIDEBARS PROVIDE CONTEXT.

THE NAVIGATION PROVIDES DISCOVERY.

THE BREADCRUMBS PROVIDE CONTEXTUAL PATH.

AI CAN HELP CREATE AND UPDATE INFORMATION.

HUMANS RETAIN CONTROL OF APPROVAL AND PUBLICATION.

API GROUP AND MONSTER NEWS REMAIN INDEPENDENT SYSTEMS.

The ultimate goal is a powerful database-driven publishing system that can grow indefinitely while remaining manageable by a person with no coding experience.