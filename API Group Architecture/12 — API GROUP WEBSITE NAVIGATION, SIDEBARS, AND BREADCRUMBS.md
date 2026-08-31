# 12 — API GROUP WEBSITE NAVIGATION, SIDEBARS, AND BREADCRUMBS

## PURPOSE

This document defines how users navigate the API Group website.

Navigation must reflect the database-driven structure of the site while remaining simple enough for users to understand.

The website should allow users to move through hierarchical information without losing their place.

The primary navigation, secondary navigation, sidebars, breadcrumbs, directories, and search must work together.

---

# 1. NAVIGATION PRINCIPLE

The API Group website should provide multiple ways to reach information.

Users may enter through:

- Main navigation
- Library
- Profiles
- Search
- Featured content
- Latest content
- Category directories
- Profile directories
- Sidebars
- Breadcrumbs
- Related records
- Related articles
- Cross-references

No single navigation path should be required.

---

# 2. API GROUP AND MONSTER NEWS ARE SEPARATE

API Group and Monster News are separate website contexts.

Monster News must not appear as an ordinary API Group navigation category.

API Group navigation belongs to the API Group website.

Monster News has its own navigation system.

The two systems may intentionally reference one another, but they must remain independent.

---

# 3. PRIMARY API GROUP NAVIGATION

The API Group header should contain the primary API Group navigation.

The exact labels may evolve, but the primary navigation should provide access to the major API Group areas.

The navigation should not expose unnecessary database complexity.

---

# 4. LIBRARY

The public-facing Library should be presented as the API Group's information and resource library.

The Library may contain:

- News
- Guides
- Checklists
- Agent Training
- About API Group

The Library is primarily editorial and informational.

---

# 5. PROFILES

Profiles are the primary structured-information system.

The public navigation may expose an entry point for Profiles or Agency Profiles depending on the final navigation design.

Profiles lead into the database-driven information system.

---

# 6. PROFILE NAVIGATION

The Profile System must allow users to browse by record type and jurisdiction.

Initial navigation should support:

- Federal
- State
- County
- City
- Village
- Civic
- Personnel

These are navigation entry points.

They are not intended to create duplicate copies of the underlying records.

---

# 7. AGENCY PROFILES

Agency Profiles may be presented as a major entry point.

When the user enters Agency Profiles, the page should provide access to:

- Federal
- State
- County
- City
- Village
- Civic
- Personnel

The administrator should be able to change or expand this navigation through the CMS.

---

# 8. DATABASE-DRIVEN PROFILE NAVIGATION

Profile navigation should be generated from database records wherever appropriate.

The system must not assume a permanent fixed number of:

- Counties
- Cities
- Villages
- Agencies
- Civic organizations
- Personnel

If a new record is added, it should become available through the appropriate directory automatically.

---

# 9. FEDERAL NAVIGATION

Federal navigation leads to federal records relevant to Illinois.

Examples may include:

- Federal agencies
- Federal programs
- Federal officials
- Federal funding
- Federal oversight
- Federal activity affecting Illinois

Federal records should be included based on their relevance to the API Group's Illinois focus.

---

# 10. STATE NAVIGATION

State navigation leads to Illinois state records.

Possible areas include:

- State agencies
- State offices
- State departments
- State boards
- State commissions
- State officials
- State legislators

---

# 11. COUNTY NAVIGATION

County navigation leads to the Illinois counties represented in the database.

Example:

Counties

→ White County

→ Edgar County

→ Clark County

The list must be generated from database records.

---

# 12. CITY NAVIGATION

City navigation leads to cities represented in the database.

The system must not contain a manually maintained list of cities.

Cities should be retrieved from the database.

---

# 13. VILLAGE NAVIGATION

Village navigation operates in the same manner.

The directory is generated from database records.

---

# 14. CIVIC NAVIGATION

Civic navigation leads to civic organizations and other relevant civic entities.

The system must allow civic organizations to have relationships with:

- People
- Agencies
- Counties
- Cities
- Villages
- Articles
- Documents

---

# 15. PERSONNEL NAVIGATION

Personnel must be independently searchable and browsable.

Personnel should not be accessible only through an agency or jurisdiction.

A user should be able to begin with:

Personnel

and search directly for a person.

---

# 16. PERSONNEL CROSS-NAVIGATION

A personnel profile may be reached through:

Personnel Search

or:

Agency
→ Personnel

or:

County
→ Personnel

or:

City
→ Personnel

or:

Civic Organization
→ Personnel

All paths lead to the same canonical personnel record.

---

# 17. HIERARCHICAL NAVIGATION

The website may use a hierarchy for browsing.

Example:

Profiles
→ Agency Profiles
→ State
→ Illinois
→ State Agencies
→ Agency

The hierarchy describes the user's navigation path.

It does not define permanent ownership of the records.

---

# 18. JURISDICTIONAL NAVIGATION

The system should support navigation through jurisdictions.

Example:

Illinois
→ White County
→ Carmi

From Carmi, the user may be able to view:

- Agencies
- Personnel
- Civic organizations
- Related documents
- Related articles

---

# 19. CROSSOVER BETWEEN JURISDICTIONS

A person, agency, or organization may be connected to more than one jurisdiction.

The navigation system must not prevent this.

Example:

A person may work for:

White County Housing Authority

and also hold a position associated with:

City of Carmi

The user should be able to follow either relationship to reach the same personnel profile.

---

# 20. SIDEBARS

The website must support optional sidebars.

A page may have:

- Left sidebar
- Right sidebar
- Both
- Neither

The administrator controls this through the CMS.

---

# 21. LEFT SIDEBAR

The left sidebar should generally provide navigation.

Typical uses:

- Hierarchical categories
- Profile types
- Counties
- Agencies
- Subcategories
- Directory indexes
- Navigation links

---

# 22. RIGHT SIDEBAR

The right sidebar should generally provide contextual information.

Typical uses:

- Related profiles
- Connections
- Related articles
- Sources
- Documents
- Additional resources
- Recent content

---

# 23. SIDEBARS ARE PAGE-SPECIFIC

The sidebar configuration may change as the user moves through the site.

Example:

Record Room:
Left sidebar

State Directory:
Left sidebar

Agency Profile:
Left sidebar

Personnel Profile:
Right sidebar

Article:
Left and right sidebars

Homepage:
No sidebar

---

# 24. SIDEBAR CONTENT MUST BE CONFIGURABLE

An administrator must be able to choose what appears in each sidebar.

The administrator should be able to add:

- Link lists
- Category lists
- Database-driven directories
- Search boxes
- Related records
- Featured records
- Recent records
- Custom text
- Images
- Documents
- Widgets

No coding should be required.

---

# 25. DYNAMIC SIDEBAR LISTS

Sidebar lists should be capable of being database-driven.

Example:

COUNTIES

Query:

Profile Type = County
State = Illinois
Published = Yes
Sort = Alphabetical

The sidebar automatically displays every matching county.

---

# 26. AUTOMATIC SIDEBAR UPDATES

If a new record is added to the database, the appropriate dynamic sidebar should update automatically.

Example:

New record:

Crawford County

Result:

Crawford County automatically appears in the configured county sidebar.

---

# 27. SIDEBAR HIERARCHY

A sidebar may display nested information.

Example:

State

→ Illinois

→ Agencies

→ Attorney General's Office

→ FOIA

→ OMA

The nesting should reflect the current content hierarchy or database relationships.

---

# 28. CONTEXTUAL SIDEBARS

Sidebar content should be capable of changing according to the page currently being viewed.

Example:

User is viewing:

White County

The sidebar may automatically show:

Agencies
Personnel
Cities
Villages
Civic Organizations
Related Records

---

# 29. PROFILE CONNECTION SIDEBAR

Personnel and agency profiles may use the right sidebar to display connections.

Example:

RELATED CONNECTIONS

White County Housing Authority

City of Carmi

White County

Related Personnel

Related Civic Organizations

Related Articles

---

# 30. SIDEBAR COLLAPSING

Sidebars should support expandable and collapsible sections.

This is especially important for large datasets.

Example:

COUNTIES

▼ A
▼ B
▼ C
▼ D

The administrator should not have to manually rebuild the structure as records are added.

---

# 31. LARGE SIDEBAR DATASETS

Large lists should support:

- Search
- Filtering
- Alphabetical navigation
- Expand/collapse
- Pagination where appropriate

The system must remain usable when the database becomes large.

---

# 32. BREADCRUMBS

Breadcrumbs must remain visible near the top of content pages.

Breadcrumbs show the user's current location.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ State Agencies
→ Agency Name

---

# 33. BREADCRUMB NAVIGATION

Each breadcrumb level should be clickable where that level represents a valid public destination.

The user should be able to move backward through the hierarchy without repeatedly using the browser Back button.

---

# 34. BREADCRUMBS ARE DYNAMIC

Breadcrumbs should be generated automatically from:

- Current page
- Category
- Profile type
- Jurisdiction
- Navigation context

They should not be manually typed into every page.

---

# 35. MULTIPLE PATHS AND BREADCRUMBS

Because a record may be reachable through multiple paths, the system should distinguish between:

CANONICAL RECORD

and

CURRENT NAVIGATION PATH

The record remains the same.

The breadcrumb may reflect the route the user took to reach it.

---

# 36. CANONICAL PROFILE LINKS

Each profile should have a canonical destination.

All references to that profile should ultimately point to the same record.

---

# 37. BREADCRUMBS AND SEARCH

If a user reaches a profile through search, the breadcrumb should still provide useful navigation.

The system should not require the user to know the original hierarchy.

---

# 38. SEARCH

Search should be a major navigation mechanism.

Users should be able to search:

- Articles
- Profiles
- Personnel
- Agencies
- Counties
- Cities
- Villages
- Civic organizations
- Documents
- Sources

---

# 39. GLOBAL SEARCH

A global search may search across the API Group database.

Results should identify the record type.

Example:

SEARCH RESULTS

Pam Deig
Personnel Profile

White County Housing Authority
Agency Profile

White County
County Profile

---

# 40. FILTERED SEARCH

Search should support filters.

Possible filters:

- Record type
- Jurisdiction
- Category
- Date
- Organization
- County
- City
- Village
- Source

---

# 41. SEARCH AND NAVIGATION WORK TOGETHER

A user may:

Browse

or

Search

and then continue navigating through related records.

Search should not be a dead end.

---

# 42. RECORD ROOM

The Record Room is the user's entry point for discovering structured records.

It should explain the available record types and provide navigation into them.

The Record Room may contain:

- Search
- Record type links
- Featured records
- Recent records
- Directory links

---

# 43. RECORD TYPE DIRECTORY

The Record Room should provide clear entry points for major record types.

Example:

Federal
State
County
City
Village
Civic
Agency
Personnel

The exact presentation may use cards, lists, or a combination.

---

# 44. DIRECTORY PAGES

Clicking a record type should open a new page dedicated to that type.

Example:

User clicks:

County

The system opens:

County Directory

with its own navigation and sidebar.

---

# 45. NEW PAGE PER NAVIGATION LEVEL

When the user follows a hierarchical navigation link, the destination should be treated as a new page context.

The content changes.

The sidebar may change.

The available navigation may change.

The breadcrumb updates.

---

# 46. EXAMPLE NAVIGATION FLOW

USER STARTS:

Record Room

↓

Clicks:

State

↓

NEW PAGE:

Illinois State Records

↓

Sidebar changes to:

State Agencies
State Personnel
State Offices
State Boards
State Commissions

↓

User clicks:

Agency

↓

NEW PAGE:

Agency Profile

↓

Sidebar changes to:

Agency Sections

↓

User clicks:

Personnel

↓

PERSONNEL DIRECTORY

The navigation context changes at every level.

---

# 47. AGENCY NAVIGATION

Agency navigation should support internal subcategories.

Example:

Attorney General's Office

→ FOIA

→ OMA

→ Divisions

→ Offices

→ Personnel

The exact structure depends on the available database records.

---

# 48. AGENCY SUBCATEGORIES

Agency subcategories should not be hard-coded into static pages.

They should be represented by appropriate database records or configurable categories.

---

# 49. PROFILE DIRECTORY CARDS

Directories may use cards for relatively small collections.

Example:

State Agencies

[Agency Card]

[Agency Card]

[Agency Card]

Cards may display:

- Logo
- Name
- Type
- Short description

---

# 50. LARGE DIRECTORY LISTS

Large directories should switch to compact list layouts.

This is especially important for:

- Personnel
- Counties
- Large agency collections
- Large civic organization collections

---

# 51. PERSONNEL DIRECTORY

Personnel should generally use a compact presentation.

Example:

[Photo] Pam Deig
Executive Director
White County Housing Authority

[Photo] Jane Smith
Director
Agency Name

The complete profile is opened by selecting the person.

---

# 52. RESPONSIVE NAVIGATION

Navigation must work on:

- Desktop
- Tablet
- Mobile

Sidebars may transform into:

- Accordions
- Drawers
- Expandable sections

on smaller screens.

---

# 53. MOBILE BREADCRUMBS

Breadcrumbs must remain usable on mobile.

If the breadcrumb becomes too long, the interface may collapse intermediate levels while preserving access to them.

---

# 54. HEADER

The API Group header should contain:

- API Group logo
- Primary navigation
- Search where appropriate
- User/account controls where appropriate

The header should remain visually distinct from Monster News.

---

# 55. FOOTER

The API Group footer should provide appropriate secondary navigation.

Possible footer areas:

- API Group information
- Library
- Profiles
- Contact
- Contributor information
- Legal information
- Site information

---

# 56. NAVIGATION LABELS

Public-facing labels should prioritize clarity over technical database terminology.

The CMS may use technical names internally.

The public interface should use terminology ordinary users understand.

---

# 57. NAVIGATION LABEL CONFIGURATION

Administrators should be able to change visible navigation labels without changing the underlying database structure.

Example:

Internal:

profile_directory_agency

Public label:

Agency Profiles

---

# 58. NAVIGATION ORDER

Administrators should be able to reorder navigation items.

The order should not require code changes.

---

# 59. HIDDEN NAVIGATION

An administrator should be able to hide a navigation item without deleting the underlying content or database records.

---

# 60. TEMPORARY NAVIGATION

The CMS may allow temporary navigation items for:

- Announcements
- Special projects
- Research collections
- Events
- Campaigns

These should be removable without destroying underlying records.

---

# 61. FEATURED NAVIGATION

The administrator may designate certain sections as featured.

Featured sections may appear on:

- Homepage
- Landing pages
- Navigation
- Sidebars

---

# 62. NAVIGATION PERMISSIONS

Some administrative navigation should be visible only to authorized users.

Public navigation should expose only published information.

---

# 63. ADMINISTRATIVE NAVIGATION

The public navigation and administrative navigation are separate.

The administrator control panel should provide access to:

- Articles
- Profiles
- Categories
- Relationships
- Templates
- Sidebars
- Navigation
- Media
- Users
- Settings

---

# 64. NAVIGATION PREVIEW

The administrator should be able to preview navigation changes before publishing them.

---

# 65. NAVIGATION VERSIONING

Significant navigation changes should ideally be recorded in revision history.

This allows administrators to determine what changed and when.

---

# 66. DATABASE-DRIVEN NAVIGATION PRINCIPLE

Whenever a navigation list represents database records, it should be generated from the database.

Example:

County list:

Database records
→ Query
→ County sidebar
→ County directory

Not:

Developer
→ Manually edits list
→ HTML

---

# 67. RELATIONAL NAVIGATION PRINCIPLE

When a navigation list represents relationships, it should be generated from relationships.

Example:

Personnel associated with Agency X:

Agency X
→ Personnel relationship query
→ Personnel list

Not:

Agency X
→ Manually typed personnel list

---

# 68. AUTOMATIC RECORD ADDITION

When a new database record is created, all appropriate database-driven navigation components should be able to recognize it automatically.

Example:

New agency

→ Agency directory updates

→ Appropriate sidebar updates

→ Search updates

→ Related personnel queries update

→ Related jurisdiction pages update

---

# 69. NAVIGATION SHOULD NOT CREATE DATA

Navigation should expose data.

It should not become the source of the data.

The database creates the record.

The navigation finds and displays the record.

---

# 70. FINAL NAVIGATION PRINCIPLE

THE USER SHOULD ALWAYS KNOW:

WHERE THEY ARE.

WHERE THEY CAME FROM.

WHAT IS AVAILABLE HERE.

HOW TO GO BACK.

WHAT IS CONNECTED.

HOW TO SEARCH FOR SOMETHING ELSE.

BREADCRUMBS SHOW WHERE THE USER IS.

SIDEBARS SHOW WHAT IS AVAILABLE IN THE CURRENT CONTEXT.

SEARCH PROVIDES AN ALTERNATIVE ENTRY POINT.

DIRECTORIES PROVIDE DATABASE-DRIVEN BROWSING.

RELATIONSHIPS PROVIDE CROSS-NAVIGATION.

THE HEADER PROVIDES PRIMARY SITE NAVIGATION.

THE FOOTER PROVIDES SECONDARY SITE NAVIGATION.

THE CMS CONTROLS THE PRESENTATION.

THE DATABASE PROVIDES THE RECORDS.

API GROUP AND MONSTER NEWS REMAIN SEPARATE.

THE WEBSITE SHOULD NEVER REQUIRE A DEVELOPER TO MANUALLY ADD A NEW COUNTY, AGENCY, PERSON, CITY, VILLAGE, CIVIC ORGANIZATION, ARTICLE, OR CATEGORY TO A DATABASE-DRIVEN NAVIGATION LIST.