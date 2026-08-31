# 10 — API GROUP CMS AND ADMINISTRATOR CONTROL PANEL

## PURPOSE

This document defines the administrative control system for the API Group website.

The API Group website must be manageable by an administrator with no coding experience.

The administrator should be able to manage content, profiles, categories, navigation, templates, sidebars, page layouts, media, publishing, and database records through a secure control panel.

The CMS is the management layer between the administrator and the underlying database-driven website.

---

# 1. NO-CODE ADMINISTRATION

The administrator must not need knowledge of:

- HTML
- CSS
- JavaScript
- SQL
- Database programming
- Web development

Ordinary content, navigation, layout, and presentation changes should be possible entirely through the CMS.

---

# 2. ADMINISTRATOR LOGIN

The website must provide a secure administrator login.

The administrative control panel must not be publicly accessible.

Authentication should protect:

- Content management
- Profile management
- Database management
- Template management
- Navigation management
- Sidebar management
- User management
- Site settings

---

# 3. ADMINISTRATOR DASHBOARD

The dashboard should provide clear access to the major administrative functions.

Initial dashboard sections should include:

- Dashboard
- Articles
- Profiles
- Agencies
- Personnel
- Civic Organizations
- Jurisdictions
- Categories
- Sources
- Documents
- Media
- Templates
- Page Layouts
- Navigation
- Sidebars
- Users
- Publishing
- Revision History
- Settings

The exact dashboard organization may evolve as the system develops.

---

# 4. CONTENT MANAGEMENT

Administrators must be able to create and manage content records without coding.

Supported actions should include:

- Create
- Edit
- Preview
- Publish
- Unpublish
- Archive
- Duplicate
- Restore
- Delete where appropriate

---

# 5. ARTICLE MANAGEMENT

The article manager should allow administrators to:

- Create articles
- Edit articles
- Select article templates
- Assign categories
- Assign subcategories
- Add tags
- Add sources
- Add profile references
- Add media
- Mark articles as featured
- Schedule publication
- Save drafts
- Submit for review
- Publish
- Unpublish
- Archive

---

# 6. PROFILE MANAGEMENT

Profiles are database-driven records.

The administrator must be able to create and manage profiles without creating static webpages manually.

Initial profile types include:

- Federal
- State
- County
- City
- Village
- Agency
- Civic Organization
- Personnel

Additional profile types may be added later.

---

# 7. PROFILE RECORDS ARE NOT ARTICLES

A profile is a structured database record.

It should not require an administrator to write an article every time a new person, agency, county, city, village, or civic organization is added.

The profile template retrieves the information from the database.

---

# 8. AUTOMATIC PROFILE PAGES

When an administrator creates and publishes a new profile record, the website should automatically be capable of generating the appropriate public profile page.

Example:

Administrator creates:

Profile Type:
County

Name:
Edgar County

State:
Illinois

The system automatically makes that record available through the appropriate directory, search, navigation, and profile template.

---

# 9. AUTOMATIC DIRECTORY UPDATES

Directories must be database-driven.

The administrator must not manually edit a directory when adding a new record.

Example:

Existing counties:

White County
Edgar County
Clark County

Administrator adds:

Crawford County

The county directory automatically displays Crawford County.

---

# 10. AUTOMATIC SIDEBAR UPDATES

If a sidebar is configured to display database records, adding a new record should automatically update the sidebar.

Example:

County sidebar:

White County
Edgar County
Clark County

Administrator adds:

Crawford County

The sidebar automatically becomes:

White County
Edgar County
Clark County
Crawford County

No HTML editing should be required.

---

# 11. CATEGORY MANAGEMENT

Categories must be manageable through the CMS.

Administrators should be able to:

- Create categories
- Rename categories
- Reorder categories
- Create subcategories
- Move categories
- Hide categories
- Publish categories
- Archive categories

---

# 12. HIERARCHICAL CATEGORIES

The CMS must support hierarchical category structures.

A category may contain subcategories.

Subcategories may contain additional subcategories.

The system should not impose an unnecessarily shallow hierarchy.

---

# 13. AUTOMATIC CATEGORY NAVIGATION

Where a sidebar or navigation component is configured to use database categories, newly created categories should automatically appear.

Example:

Agent Training
→ Specifications
→ Workflows
→ Data Models

If the administrator creates:

Agent Training
→ Tutorials

the configured navigation automatically includes Tutorials.

---

# 14. NAVIGATION IS NOT HARD-CODED

The navigation system should be treated as a presentation layer.

The administrator should be able to manage navigation without editing source code.

Navigation may be:

- Database-driven
- Manually configured
- Automatically generated
- A combination of these approaches

---

# 15. NAVIGATION MANAGEMENT

The administrator should be able to:

- Add links
- Remove links
- Rename labels
- Reorder links
- Nest links
- Expand links
- Collapse links
- Hide links
- Show links
- Assign links to specific site contexts

---

# 16. PROFILE NAVIGATION

Profile navigation should be capable of being generated from the database.

Example:

Agency Profiles

Sidebar:

Federal
State
County
City
Village
Civic
Personnel

These should not be treated as an immutable list.

If the administrator creates an additional profile classification, the system should be capable of incorporating it into the configured navigation.

---

# 17. DYNAMIC HIERARCHICAL NAVIGATION

As a user moves through the Profile System, the navigation should change to reflect the user's current location.

Example:

Profile Directory

→ State

→ Illinois

The sidebar may then change to show:

Agencies
Personnel
Counties
Cities
Villages
Civic

The sidebar should be generated from the current context and available database records.

---

# 18. SIDEBAR CONTROL

The administrator must be able to determine whether a page has:

- Left sidebar
- Right sidebar
- Both sidebars
- No sidebar

This must be configurable without coding.

---

# 19. PAGE-SPECIFIC SIDEBARS

Different pages may use different sidebar configurations.

Example:

Record Room:
Left sidebar

Agency Directory:
Left sidebar

Personnel Profile:
Right sidebar

Article:
Left sidebar + Right sidebar

Homepage:
No sidebar

---

# 20. SIDEBAR CONTENT MANAGEMENT

The administrator must be able to determine what appears in a sidebar.

Possible sidebar components include:

- Navigation
- Categories
- Subcategories
- Profile directories
- Personnel
- Agencies
- Counties
- Cities
- Villages
- Civic organizations
- Recent articles
- Featured articles
- Related articles
- Related profiles
- Sources
- Documents
- Search
- Custom links
- Custom text
- Images
- Widgets

---

# 21. DYNAMIC SIDEBAR QUERIES

A sidebar should be capable of retrieving information using database rules.

Example:

SIDEBAR:

Illinois Counties

QUERY:

Profile Type = County
State = Illinois
Published = Yes
Sort = Alphabetical

The sidebar automatically displays all matching records.

There should be no manually maintained list.

---

# 22. CONTEXT-AWARE SIDEBARS

Sidebar content may change based on the current page.

Example:

User is viewing:

Illinois
→ White County

The sidebar may automatically display:

White County Agencies
White County Personnel
White County Cities
White County Villages
White County Civic Organizations

---

# 23. RIGHT SIDEBAR FOR CONNECTIONS

Personnel and other profile pages may use the right sidebar for relationships and contextual information.

Example:

RELATED CONNECTIONS

Housing Authority
White County
City of Carmi
Civic Organizations
Related Personnel

These relationships should come from the database.

---

# 24. SIDEBAR TEMPLATES

Administrators should be able to create reusable sidebar configurations.

Example:

"Illinois County Index"

may contain:

- County search
- Alphabetical county list
- Recent county profiles

That sidebar configuration can then be assigned to multiple pages.

---

# 25. PAGE LAYOUT CONTROL

Administrators should be able to select page layouts through the CMS.

Initial layouts should include:

- Full Width
- Left Sidebar
- Right Sidebar
- Two Sidebars
- Directory
- Profile
- Article
- Landing Page

---

# 26. TEMPLATE MANAGEMENT

The administrator must be able to manage reusable templates.

Initial template types may include:

- Article Template
- Guide Template
- Checklist Template
- Training Template
- Profile Template
- Agency Template
- Personnel Template
- Directory Template
- Category Template
- Search Template
- Landing Page Template

---

# 27. TEMPLATE ASSIGNMENT

Templates may be assigned by:

- Content type
- Profile type
- Category
- Subcategory
- Section
- Individual record
- Page layout

---

# 28. TEMPLATE OVERRIDES

An individual page should be able to override a default template configuration without changing every page using that template.

Example:

Default Personnel Profile:

Right sidebar

One specific personnel page:

Both sidebars

The administrator should be able to make that exception through the CMS.

---

# 29. VISUAL TEMPLATE EDITING

Where practical, templates should be configurable through a visual interface.

The administrator should be able to select and arrange:

- Sections
- Columns
- Cards
- Lists
- Images
- Text
- Sidebars
- Search
- Related records
- Featured content

without writing code.

---

# 30. PAGE BUILDER

The CMS should eventually provide a visual page builder.

The administrator should be able to:

- Add a section
- Add a component
- Move a component
- Remove a component
- Resize a component
- Configure a component
- Select a data source
- Preview the result

---

# 31. DATABASE-DRIVEN COMPONENTS

Components should be able to retrieve database records.

Example:

FEATURED PERSONNEL

Query:

Profile Type = Personnel
Featured = Yes
Published = Yes
Limit = 12

The component displays the matching records automatically.

---

# 32. LATEST CONTENT COMPONENT

A Latest Content component should automatically retrieve the newest records.

Example:

Published = Yes
Sort = Publication Date Descending
Limit = 10

When a new article is published, it automatically becomes eligible for the component.

---

# 33. FEATURED CONTENT COMPONENT

A Featured Content component should retrieve records marked:

Featured = Yes

Administrators should not need to manually place featured content into the homepage.

---

# 34. CARD COMPONENTS

Cards should be reusable components.

Possible card types:

- Article Card
- Profile Card
- Agency Card
- Personnel Card
- County Card
- City Card
- Village Card
- Civic Organization Card

---

# 35. LARGE DIRECTORY LISTS

The CMS should allow administrators to choose between card and list presentation.

Large Personnel directories should generally support compact list or directory layouts.

A personnel directory may display:

- Thumbnail
- Name
- Position
- Organization
- Jurisdiction

---

# 36. BREADCRUMB MANAGEMENT

Breadcrumbs should normally be generated automatically from the hierarchy.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ County
→ White County
→ Housing Authority

The administrator should be able to configure breadcrumb behavior.

---

# 37. BREADCRUMB PRESENTATION

Breadcrumbs should remain visible near the top of the page beneath the primary header/navigation area.

They provide the user's current location and allow navigation back to previous levels.

---

# 38. MEDIA MANAGEMENT

The CMS should provide a media library.

Administrators should be able to:

- Upload images
- Upload documents
- Search media
- Replace media
- Add descriptions
- Add captions
- Associate media with records

---

# 39. LOGO MANAGEMENT

API Group branding assets should be manageable independently from Monster News branding assets.

The API Group CMS must not accidentally replace or alter Monster News branding.

---

# 40. API GROUP BRANDING

API Group should have its own configurable:

- Logo
- Colors
- Typography
- Header
- Navigation
- Footer
- Theme settings

These settings belong to API Group.

---

# 41. MONSTER NEWS SEPARATION

Monster News is a separate website context.

It must not be treated as an ordinary API Group category.

Monster News should have its own:

- Branding
- Homepage
- Navigation
- Articles
- Categories
- Templates
- Editorial workflow
- Featured content
- Sidebar configuration
- Administrative configuration

---

# 42. INDEPENDENT CONTROL PANELS

API Group and Monster News should be independently configurable.

An administrator working on API Group should not accidentally alter Monster News settings.

Likewise, Monster News configuration should not automatically alter API Group.

---

# 43. CONTROLLED CROSS-SITE REFERENCES

Although the two systems remain independent, Monster News may intentionally reference API Group database information.

Example:

Monster News Article

→ References

API Group Personnel Profile

The reference should point to the canonical API Group record.

---

# 44. NO AUTOMATIC CONTENT MERGING

API Group articles must not automatically become Monster News articles.

Monster News articles must not automatically become API Group articles.

The two editorial systems remain separate.

---

# 45. AI MANAGEMENT

The CMS should eventually provide controlled AI integration.

AI may be permitted to:

- Create draft profiles
- Update proposed profile information
- Create draft articles
- Suggest categories
- Suggest tags
- Suggest relationships
- Identify possible duplicates
- Extract information from documents
- Suggest sources
- Suggest related records

---

# 46. AI REVIEW

AI-created or AI-modified information should be reviewable.

The administrator or authorized editor should be able to:

- Approve
- Edit
- Reject
- Merge
- Request additional research

---

# 47. AI MUST NOT BYPASS DATABASE STRUCTURE

AI must create or update structured database records.

AI should not solve a database problem by creating hard-coded HTML.

Example:

CORRECT:

AI creates County record
→ Database updates
→ County directory updates
→ Sidebar updates
→ Search updates

INCORRECT:

AI edits a static HTML list
→ Adds "Crawford County"

---

# 48. AUTOMATIC CASCADE OF DATABASE CHANGES

The intended system behavior is:

ADMINISTRATOR OR AI CREATES RECORD

↓

DATABASE RECORD IS CREATED

↓

RELATIONSHIPS ARE STORED

↓

DIRECTORIES UPDATE

↓

SIDEBARS UPDATE

↓

SEARCH UPDATES

↓

RELATED CONTENT UPDATES

↓

BREADCRUMBS BECOME AVAILABLE

↓

PROFILE PAGE IS RENDERED FROM THE APPROPRIATE TEMPLATE

No manual coding should be necessary.

---

# 49. PUBLISHING WORKFLOW

Content should support a controlled publishing workflow.

Suggested states:

- Draft
- Review
- Published
- Unpublished
- Archived

---

# 50. REVIEW QUEUE

The CMS should provide a review queue.

The queue may contain:

- AI-generated profiles
- AI-generated articles
- Contributor submissions
- Suggested corrections
- Suggested relationships
- Imported records

---

# 51. USER ROLES

The system should eventually support multiple administrative roles.

Examples:

Administrator
Editor
Contributor
Researcher
Reviewer

---

# 52. PERMISSIONS

Permissions should control access to functions such as:

- Create
- Edit
- Review
- Publish
- Archive
- Delete
- Manage profiles
- Manage templates
- Manage navigation
- Manage sidebars
- Manage users
- Manage settings

---

# 53. CONTRIBUTOR ACCESS

Approved contributors and partners may eventually receive controlled access.

Contributors should not automatically receive full administrator privileges.

---

# 54. AUDIT LOG

The CMS should maintain an audit log of important changes.

Examples:

- Record created
- Record edited
- Record published
- Record unpublished
- Category created
- Category moved
- Sidebar changed
- Navigation changed
- Template changed
- User permission changed

---

# 55. REVISION HISTORY

Articles and other appropriate content should retain revision history.

The administrator should be able to see:

- Previous version
- Current version
- Editor
- Date
- Changes

---

# 56. PREVIEW

Administrators should be able to preview content before publication.

Preview should show the actual configured template and layout.

The administrator should be able to inspect:

- Desktop layout
- Mobile layout
- Sidebars
- Breadcrumbs
- Cards
- Images
- Typography
- Related content

---

# 57. RESPONSIVE LAYOUT

Templates must work on:

- Desktop
- Tablet
- Mobile

The administrator should not have to create separate copies of the content for different screen sizes.

---

# 58. MOBILE SIDEBARS

On smaller screens, sidebars may become:

- Expandable sections
- Accordions
- Drawers
- Sections below the primary content

The content itself remains the same database-driven content.

---

# 59. SITE SETTINGS

The API Group CMS should provide configurable settings for:

- Site name
- Logo
- Favicon
- Theme
- Typography
- Header
- Navigation
- Footer
- Default layout
- Default sidebar
- Search
- Social links where applicable

---

# 60. DEFAULTS AND OVERRIDES

The CMS should support reasonable defaults.

Example:

Default Profile Template:
Left sidebar

Default Personnel Template:
Right sidebar

Individual page:
Both sidebars

The individual configuration overrides the default without changing the global template.

---

# 61. ADMINISTRATOR EXPERIENCE

The administrator should be able to perform common tasks intuitively.

Examples:

"I want to add a county."

→ Create County Profile
→ Enter information
→ Save
→ Publish

The county automatically appears in the appropriate database-driven directories and sidebars.

---

"I want to feature this article."

→ Edit Article
→ Select Featured
→ Save

The article automatically appears in configured Featured Article areas.

---

"I want this page to have a right sidebar."

→ Edit Page
→ Layout
→ Right Sidebar
→ Configure Sidebar
→ Save

No code is required.

---

# 62. PRESENTATION SHOULD FOLLOW DATA

The CMS should not require administrators to manually synchronize:

- Profiles
- Directories
- Sidebars
- Navigation
- Search
- Breadcrumbs
- Related content

These should derive from the underlying database whenever possible.

---

# 63. DATABASE-FIRST ARCHITECTURE

The fundamental architecture is:

DATABASE
↓
RECORDS
↓
RELATIONSHIPS
↓
QUERIES
↓
TEMPLATES
↓
COMPONENTS
↓
PAGE
↓
USER

The CMS manages the system without requiring the administrator to understand this technical architecture.

---

# 64. API GROUP AND MONSTER NEWS

API Group and Monster News are separate entities.

They should not be combined into one general content hierarchy.

API Group controls API Group information.

Monster News controls Monster News information.

Controlled references may connect them when intentionally configured.

---

# 65. FINAL PRINCIPLE

THE CMS IS THE ADMINISTRATOR'S CONTROL PANEL.

THE ADMINISTRATOR SHOULD NOT NEED TO CODE.

THE DATABASE IS THE SOURCE OF STRUCTURED INFORMATION.

THE CMS MANAGES THE DATABASE.

THE TEMPLATES PRESENT THE DATABASE.

THE PAGE BUILDER CONTROLS PRESENTATION.

THE SIDEBARS PROVIDE NAVIGATION AND CONTEXT.

THE BREADCRUMBS SHOW THE USER'S PATH.

DIRECTORIES ARE GENERATED FROM DATABASE RECORDS.

SEARCH IS GENERATED FROM DATABASE RECORDS.

NAVIGATION CAN BE GENERATED FROM DATABASE RECORDS.

SIDEBARS CAN BE GENERATED FROM DATABASE RECORDS.

FEATURED CONTENT IS DATABASE-DRIVEN.

LATEST CONTENT IS DATABASE-DRIVEN.

AI CREATES OR PROPOSES STRUCTURED DATA, NOT HARD-CODED WEBPAGES.

API GROUP AND MONSTER NEWS REMAIN INDEPENDENT SYSTEMS.

THE GOAL IS A TRUE NO-CODE, DATABASE-DRIVEN, ADMINISTRATOR-CONTROLLED WEBSITE.