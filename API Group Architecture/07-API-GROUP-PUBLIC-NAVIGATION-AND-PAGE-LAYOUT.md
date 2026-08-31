# 07 — API GROUP PUBLIC NAVIGATION AND PAGE LAYOUT

## PURPOSE

This document defines how users move through the API Group website.

The public website must present the database-driven information in a clear hierarchy while allowing users to move between related information without becoming trapped inside a rigid hierarchy.

The navigation system must support:

- Main navigation
- Category landing pages
- Database-driven directories
- Expandable sidebars
- Breadcrumb navigation
- Profile pages
- Search
- Related information
- Optional left and right sidebars
- Deep navigation
- Multiple paths to the same profile

The navigation system is a presentation of the information architecture.

It must not become the information architecture itself.

---

# 1. API GROUP AND MONSTER NEWS ARE SEPARATE

API Group and Monster News are separate public website contexts.

The API Group website should not display Monster News navigation as part of its normal API Group navigation.

Monster News should not appear as an API Group category.

Each has its own:

- Branding
- Logo
- Navigation
- Templates
- Content
- Control panel
- Editorial structure
- Homepage
- Publishing workflow

Cross-references may exist where appropriate, but the two systems remain independent.

---

# 2. API GROUP HOMEPAGE

The API Group homepage is the primary entrance into the API Group information system.

It should communicate that API Group is a searchable collection of information, records, profiles, research, resources, and connections.

The homepage should provide:

- API Group branding
- Main navigation
- Search
- Featured content
- Latest content
- Major content destinations
- Clear entry points into profiles and the library
- Appropriate footer
- Optional configured sidebars where desired

---

# 3. MAIN API GROUP NAVIGATION

The exact final wording of the main navigation remains subject to refinement.

The important principle is that the main navigation should represent the major ways a user enters the API Group system.

The navigation should not be designed around every possible database entity.

It should provide broad entry points.

---

# 4. RECORD ROOM / PROFILE DISCOVERY

The profile system should provide a major public discovery area.

The user should be able to enter the profile system and progressively narrow their search.

The profile discovery system should not force every entity into one rigid hierarchy.

Instead, users should be able to enter through:

- Agency Profiles
- Personnel
- Search
- Jurisdiction
- Other configured profile entry points

---

# 5. API GROUP LIBRARY

The API Group Library is a separate content category.

It is not the same thing as Profiles.

The Library contains API Group's informational and organizational content.

Examples may include:

- API Group information
- About API Group
- Contact information
- Contributor information
- Guides
- Tips and tricks
- Checklists
- Help resources
- Agent Training
- Website information
- Other API Group resources

The Library is not the database-driven profile collection.

---

# 6. PROFILES

Profiles are the database-driven information system.

Profiles represent entities being documented by API Group.

Examples:

- Agencies
- Personnel
- Counties
- Cities
- Villages
- Civic organizations
- Federal entities
- State entities

Profiles are generated from structured database information.

---

# 7. AGENCY PROFILE ENTRY POINT

Agency Profiles should be a major entry point into the profile system.

When the user selects Agency Profiles, the system should open a dedicated agency-profile landing page.

This page should explain what agency profiles are and how they can be explored.

It should then provide database-driven navigation into the available agency classifications.

---

# 8. AGENCY PROFILE SIDEBAR

The Agency Profiles landing page should normally use a left sidebar.

The initial sidebar categories should include:

- Federal
- State
- County
- City
- Village
- Civic
- Personnel

The exact presentation may change during development.

The important requirement is that these are navigational views into the profile database.

---

# 9. DYNAMIC AGENCY SIDEBAR

The sidebar must not be a hard-coded list of every agency.

The categories themselves may be configured by the administrator.

Within those categories, the actual entity lists should come from the database.

Example:

STATE

→ Illinois

→ State Agencies

The system queries the database to determine which agencies exist.

---

# 10. ADDING A NEW CATEGORY

If the administrator adds another Agency Profile classification, the CMS should be capable of automatically making that classification available in the configured Agency Profile navigation.

The administrator should not need to modify source code.

Example:

Current:

Federal
State
County
City
Village
Civic

Administrator adds:

Regional

The configured sidebar can automatically display:

Regional

---

# 11. FEDERAL NAVIGATION

Selecting Federal should display federal entities being monitored or documented by API Group.

The federal section is specifically relevant to API Group's Illinois-focused mission.

Federal entities may be included because they:

- Affect Illinois
- Operate in Illinois
- Fund Illinois programs
- Regulate Illinois activities
- Provide grants
- Investigate matters involving Illinois
- Otherwise have meaningful Illinois implications

---

# 12. STATE NAVIGATION

Selecting State should open the Illinois state profile area.

The initial project focus is Illinois.

The State section may contain:

- Illinois state agencies
- State offices
- State departments
- Boards
- Commissions
- Legislative entities
- Other state entities

---

# 13. COUNTY NAVIGATION

Selecting County should open a database-driven directory of Illinois counties for which API Group has records.

The list should be generated from the database.

The system must not assume a fixed number of counties.

When another county is added, it becomes available automatically.

---

# 14. CITY NAVIGATION

Selecting City should open a database-driven directory of Illinois cities represented in the system.

The list should be generated from the database.

---

# 15. VILLAGE NAVIGATION

Selecting Village should open a database-driven directory of Illinois villages represented in the system.

The list should be generated from the database.

---

# 16. CIVIC NAVIGATION

Selecting Civic should open the civic organization portion of the profile database.

Civic entities may include:

- Civic organizations
- Nonprofits
- Community organizations
- Advocacy groups
- Watchdog organizations
- Community media
- Contributors
- Partners
- Other relevant organizations

These organizations are first-class entities.

---

# 17. PERSONNEL NAVIGATION

Personnel should be independently searchable.

The user should not have to know which county, agency, city, village, or federal entity a person is connected to before finding that person.

The personnel directory should therefore provide a direct entry point into the personnel database.

---

# 18. PERSONNEL IS NOT A SUBSET OF ONE JURISDICTION

Personnel profiles are independent database entities.

A person may be connected to:

- Federal entities
- State entities
- Counties
- Cities
- Villages
- Civic organizations
- Multiple agencies
- Multiple positions

Therefore, Personnel should not be treated as permanently belonging to only one branch of the navigation tree.

---

# 19. PERSONNEL SEARCH

A user searching for a person should be able to search by:

- Name
- Position
- Organization
- Agency
- Jurisdiction
- County
- City
- Village
- Civic organization

The search results should return canonical personnel profiles.

---

# 20. PERSONNEL DIRECTORY DISPLAY

Personnel directories may contain many records.

Cards may not be the best presentation for large personnel collections.

The CMS should support a compact directory layout.

Example:

PHOTO | NAME | POSITION | ORGANIZATION | JURISDICTION

The administrator should be able to choose the appropriate presentation template.

---

# 21. DATABASE-DRIVEN DIRECTORY

All directories should be database-driven.

Examples:

COUNTIES

Database query:
Entity Type = County
State = Illinois
Published = Yes

CITIES

Database query:
Entity Type = City
State = Illinois
Published = Yes

PERSONNEL

Database query:
Entity Type = Person
Published = Yes

The website renders whatever records match the query.

---

# 22. HIERARCHICAL NAVIGATION

The public website may allow users to move progressively through the hierarchy.

Example:

Agency Profiles
→ State
→ Illinois
→ State Agencies
→ Agency
→ Personnel

Another path:

Agency Profiles
→ County
→ White County
→ County Agencies
→ Agency
→ Personnel

Another path:

Personnel
→ Search
→ Pam Deig
→ Connections

These paths may converge on the same canonical database entities.

---

# 23. EACH NAVIGATION STEP MAY BE A NEW PAGE

When a user selects a sidebar link, the destination should normally be a new page or distinct page state.

The page should be able to change:

- Title
- Description
- Breadcrumb
- Sidebar contents
- Sidebar position
- Main content
- Search
- Database query
- Cards
- Directory
- Related content

This allows each level of the hierarchy to have its own appropriate presentation.

---

# 24. SIDEBAR CONTENT CHANGES WITH LOCATION

The sidebar should be contextual.

Example:

AGENCY PROFILES

Sidebar:

Federal
State
County
City
Village
Civic
Personnel

User selects:

State

The next page may display a sidebar containing:

Illinois
State Agencies
Boards
Commissions
Other State Entities

User selects:

State Agencies

The sidebar may then display:

Alphabetical agency list
or
Agency categories
or
Configured database-driven navigation.

The sidebar is therefore a navigation tool that follows the user through the hierarchy.

---

# 25. LEFT SIDEBAR DEFAULT

The API Group system should generally favor the left sidebar for hierarchical navigation.

This provides a consistent visual location for navigation.

The administrator may override this on individual pages or templates.

---

# 26. RIGHT SIDEBAR

The right sidebar should generally be used for contextual information rather than primary hierarchical navigation.

Examples:

- Connections
- Related profiles
- Related articles
- Sources
- Documents
- Additional information
- Contact information
- Related organizations

---

# 27. BOTH SIDEBARS

Some pages may use both.

Example:

LEFT SIDEBAR:

Navigation through profile hierarchy

RIGHT SIDEBAR:

Connections and related information

MAIN CONTENT:

Current profile

This is particularly useful for personnel and agency profiles.

---

# 28. NO SIDEBAR

Some pages may intentionally use no sidebar.

Examples:

- Full-width article
- Landing page
- Featured story
- Certain informational pages
- Special presentation pages

The CMS must allow the administrator to turn sidebars off.

---

# 29. SIDEBAR CONFIGURATION

The administrator should be able to configure:

- Left sidebar
- Right sidebar
- Both
- None

The administrator should also be able to select what appears in the sidebar.

The administrator should not need to modify code.

---

# 30. DATABASE-DRIVEN SIDEBAR LISTS

A sidebar list of counties must come from the database.

A sidebar list of agencies must come from the database.

A sidebar list of personnel must come from the database.

A sidebar list of civic organizations must come from the database.

The sidebar should not contain manually maintained entity lists.

---

# 31. BREADCRUMBS

Breadcrumbs are a required navigation component.

They should appear before the main body content.

The breadcrumb should communicate where the user is in the current navigation path.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ State Agencies
→ Agency Name

---

# 32. BREADCRUMBS MUST REMAIN AVAILABLE

As the user moves deeper into the profile system, the breadcrumb should remain visible.

The user should be able to select an earlier breadcrumb level to return to that section.

This prevents the user from becoming trapped deep inside the hierarchy.

---

# 33. BREADCRUMBS ARE CONTEXTUAL

Breadcrumbs represent the user's current navigation path.

They should not redefine the underlying database relationships.

The same person may therefore be reached through different breadcrumb paths.

Example:

Agency Profiles
→ County
→ White County
→ Agency
→ Personnel
→ Pam Deig

Another user may arrive through:

Personnel
→ Pam Deig

Both reach the same person.

---

# 34. CANONICAL PROFILES

Every profile should have a canonical identity.

Navigation context should not create duplicate profiles.

For example:

Pam Deig

must remain one database entity regardless of whether the user arrives from:

- Personnel
- Housing Authority
- White County
- Carmi
- Civic
- Search

---

# 35. SEARCH AS AN ALTERNATIVE TO NAVIGATION

Users should not always be required to navigate through the hierarchy.

Search should provide a shortcut.

A user who knows:

Pam Deig

should be able to search directly for Pam Deig.

A user who knows:

Housing Authority

should be able to search directly for the agency.

A user who knows:

White County

should be able to search directly for the county.

---

# 36. PROFILE CONNECTIONS

Once a user reaches a profile, the profile should expose relevant relationships.

Example:

Pam Deig

Connections:

Housing Authority
White County
Carmi
Position
Related Personnel
Related Organizations
Related Articles

This creates an investigative navigation path through the database.

---

# 37. PROFILE PAGES ARE NOT DEAD ENDS

A profile page should encourage continued discovery.

Users should be able to move from:

Person
→ Organization

Organization
→ Personnel

Agency
→ Jurisdiction

Jurisdiction
→ Agencies

Agency
→ Related Personnel

Personnel
→ Related Organizations

This creates a connected information system rather than a collection of isolated webpages.

---

# 38. ARTICLE REFERENCES

Articles may reference profiles.

Example:

An API Group article may mention:

Housing Authority
Pam Deig
White County
Carmi

Those references should link to the corresponding database entities.

---

# 39. LIBRARY NAVIGATION

The API Group Library should have its own landing page.

It should explain what the Library contains.

The Library may contain cards or other visual entry points for categories such as:

- News
- Guides
- Checklists
- Agent Training
- About API Group
- Contributions
- Help
- Other API Group resources

The final list should be configurable through the CMS.

---

# 40. LIBRARY CATEGORIES ARE NOT PROFILE TYPES

Library categories organize API Group content.

Profile types organize database entities.

Do not combine these concepts.

For example:

Library
→ Agent Training

is content organization.

Profiles
→ Agency
→ Personnel
→ County

is database entity organization.

---

# 41. HOMEPAGE FEATURED CONTENT

The API Group homepage should support featured content.

An administrator should be able to mark an article or resource:

Featured

The homepage can then automatically display it.

Featured content should not require manually editing the homepage.

---

# 42. LATEST CONTENT

The homepage should also support automatically generated latest-content sections.

Examples:

Latest Articles
Latest Profiles
Latest Records
Recently Updated

The administrator should be able to configure which sections appear.

---

# 43. CATEGORY CARDS

Major API Group destinations may be presented as cards.

For example:

API Group Library

Agency Profiles

Personnel

Other configured destinations

Cards should link to their respective landing pages.

The cards should be generated from configured CMS content rather than permanently hard-coded whenever practical.

---

# 44. FEATURED ARTICLE CARDS

Articles marked Featured may be displayed using a reusable article-card template.

The administrator should be able to control:

- Image
- Title
- Excerpt
- Category
- Date
- Related profile
- Link

The actual article content remains in the database.

---

# 45. PAGE DESCRIPTIONS

Major landing pages should explain what the user is looking at.

Example:

AGENCY PROFILES

"Explore government and civic organizations documented by API Group, organized by federal, state, county, city, village, and civic relationships."

The exact wording will be finalized later.

---

# 46. SEARCH BAR

Search should be visually prominent on appropriate landing pages.

The search system should be capable of searching across database entities and content.

Possible search areas:

- Profiles
- Personnel
- Agencies
- Library articles
- Records
- Documents
- Sources

---

# 47. FILTERED SEARCH

Search results should support filters where useful.

Examples:

Search:
Housing

Filters:

Agency
County
City
Personnel
Civic
Article

The filters should be generated from available data where practical.

---

# 48. RESPONSIVE NAVIGATION

The navigation system must work on:

- Desktop
- Tablet
- Mobile

The sidebar should adapt appropriately.

On smaller screens it may become:

- Collapsible
- Drawer-based
- Accordion-based
- Top navigation
- Other appropriate mobile presentation

The information architecture should remain the same.

---

# 49. ACCESSIBILITY

Navigation should be accessible.

Requirements should include:

- Keyboard navigation
- Visible focus states
- Proper semantic navigation
- Accessible labels
- Adequate contrast
- Expand/collapse controls
- Mobile accessibility

---

# 50. ADMINISTRATIVE CONTROL OF NAVIGATION

The administrator should be able to configure navigation through the CMS.

Controls may include:

- Add item
- Remove item
- Rename item
- Reorder item
- Hide item
- Show item
- Choose destination
- Choose database query
- Configure sidebar
- Configure breadcrumbs

No coding should be required for normal changes.

---

# 51. AUTOMATIC NAVIGATION

Where a navigation item represents database entities, it should be dynamic.

Example:

Counties

The system automatically displays counties that exist in the database.

The administrator should not have to create a new navigation link for every county.

---

# 52. NAVIGATION AND CONTENT ARE SEPARATE

A navigation item should be capable of pointing to:

- A page
- A category
- A database query
- A profile
- A profile type
- A search
- An external destination

This gives the CMS flexibility.

---

# 53. DEEP HIERARCHIES

The system must support deep navigation.

There should be no architectural assumption that the hierarchy ends after:

Category
→ Subcategory

It may continue through many levels when necessary.

However, the public presentation should remain understandable.

---

# 54. CROSS-CONNECTIONS

The navigation system must not prevent cross-connections.

Example:

A personnel profile may be reached through a county but may also connect to a city and civic organization.

The user should be able to follow those relationships directly from the profile.

---

# 55. NAVIGATION PRINCIPLE

The user should always know:

WHERE AM I?

HOW DID I GET HERE?

WHAT IS AROUND ME?

WHAT CAN I EXPLORE NEXT?

HOW DO I GO BACK?

The combination of:

- Breadcrumbs
- Contextual sidebars
- Search
- Profile relationships
- Main navigation

should answer these questions.

---

# 56. FINAL PUBLIC NAVIGATION MODEL

API GROUP
↓
PUBLIC ENTRY POINT
↓
LIBRARY / PROFILE DISCOVERY
↓
CATEGORY OR PROFILE TYPE
↓
DATABASE-DRIVEN DIRECTORY
↓
ENTITY
↓
RELATED ENTITIES
↓
RELATED CONTENT

The user can enter the system at multiple points.

The database remains connected underneath all of them.

---

# 57. FINAL DESIGN PRINCIPLE

THE WEBSITE SHOULD LOOK LIKE A CAREFULLY DESIGNED EDITORIAL WEBSITE.

UNDERNEATH THAT DESIGN, IT SHOULD FUNCTION LIKE A DATABASE-DRIVEN INFORMATION SYSTEM.

THE SIDEBARS SHOULD GUIDE THE USER.

THE BREADCRUMBS SHOULD SHOW THE PATH.

THE SEARCH SHOULD PROVIDE SHORTCUTS.

THE PROFILES SHOULD PROVIDE THE DATA.

THE RELATIONSHIPS SHOULD CONNECT THE DATA.

THE TEMPLATES SHOULD CONTROL PRESENTATION.

THE CMS SHOULD ALLOW A NON-TECHNICAL ADMINISTRATOR TO CONTROL ALL OF IT.

THE API GROUP AND MONSTER NEWS SYSTEMS MUST REMAIN INDEPENDENT.