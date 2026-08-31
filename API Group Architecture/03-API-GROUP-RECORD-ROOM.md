# 03 — API GROUP RECORD ROOM

## PURPOSE

The API Group Record Room is the primary discovery and navigation area for API Group's database-driven information.

It is not a conventional article archive.

It is the public-facing directory through which users discover profiles, records, documents, and other structured information collected by API Group.

The Record Room must be designed around database-driven navigation rather than a fixed number of manually created pages.

---

# 1. RECORD ROOM IDENTITY

The Record Room should communicate immediately that it is a place where users can:

- Search
- Browse
- Discover
- Follow relationships
- Navigate through the API Group information system

Primary description:

Search the API Group Collection by Title, Source, Topic, or Record.

The wording may be refined later, but the purpose must remain clear.

---

# 2. RECORD ROOM IS PART OF API GROUP

The Record Room belongs exclusively to the API Group website.

Monster News is not a category, subcategory, section, or dependency of the Record Room.

Monster News must never appear as part of API Group's Record Room navigation.

Monster News is an independent website/portal with its own:

- Navigation
- Content
- Templates
- Branding
- Administration
- Control panel

API Group information may be referenced by Monster News when appropriate, but that does not make Monster News part of the API Group Record Room.

---

# 3. RECORD ROOM LANDING PAGE

When a user opens the Record Room, the page should provide:

- Page title
- Description
- Search bar
- Primary discovery options
- Database-driven navigation
- Featured records
- Recently added records
- Relevant categories
- Footer

The visual design should remain consistent with the existing API Group website while using the new CMS architecture.

---

# 4. SEARCH

The Record Room should prominently display a search interface.

Users should be able to search the API Group collection by:

- Title
- Name
- Source
- Topic
- Record type
- Agency
- Personnel
- Jurisdiction
- Organization
- Tags
- Other indexed fields

Search results should be generated from the database.

Search must not depend on manually maintained navigation links.

---

# 5. RECORD ROOM NAVIGATION

The Record Room should provide a left sidebar by default.

The sidebar should contain database-driven navigation.

The administrator must be able to:

- Turn the sidebar off
- Turn the sidebar on
- Move it to the right side
- Use both sides
- Change the sidebar contents
- Change the order
- Add links
- Remove links
- Create expandable sections

The sidebar is a presentation/navigation component.

It is not the database hierarchy itself.

---

# 6. DATABASE-DRIVEN NAVIGATION

The sidebar must be populated dynamically where the navigation represents database entities.

For example:

COUNTIES

White County
Edgar County
Vermilion County
...

If another county is added to the database, it should automatically become available in the appropriate county list.

There should be no hard-coded limit such as:

County 1
County 2
County 3

The system displays however many records exist.

---

# 7. PROFILE DISCOVERY

The Record Room should make Profiles one of the major ways users discover information.

Profiles should include:

- Agency Profiles
- Personnel Profiles
- Civic Profiles
- Jurisdiction Profiles
- Contributor Profiles
- Partner Profiles
- Other administrator-defined profile types

The Record Room should not force all profiles into one geographic hierarchy.

---

# 8. AGENCY PROFILE DISCOVERY

Agency Profiles should be discoverable through classifications such as:

- Federal
- State
- County
- City
- Village
- Civic

These classifications should be database-driven and extensible.

When the administrator adds another agency classification, the CMS should be capable of adding it to the appropriate navigation automatically.

---

# 9. FEDERAL DISCOVERY

Federal records represent federal entities relevant to Illinois.

Users should be able to browse:

Federal
→ Federal Agency Profiles

The federal directory should contain only entities relevant to the API Group's Illinois-focused mission.

Federal information may include:

- Federal agencies
- Federal offices
- Federal programs
- Federal funding
- Federal personnel
- Federal records

---

# 10. STATE DISCOVERY

The initial state focus is:

Illinois

Users should be able to navigate:

State
→ Illinois
→ State Agency Profiles

The state directory may include:

- State agencies
- Offices
- Departments
- Authorities
- Boards
- Commissions
- Personnel
- Programs
- Records

---

# 11. COUNTY DISCOVERY

Users should be able to navigate:

County
→ County List
→ Selected County

For example:

County
→ White County

The selected county page can then expose:

- County agencies
- County personnel
- Cities
- Villages
- Civic organizations
- Records
- Documents
- Related articles

The available items are generated from database relationships.

---

# 12. CITY DISCOVERY

Users should be able to navigate:

City
→ City List
→ Selected City

The city page can display:

- City agencies
- City personnel
- Related county
- Civic organizations
- Records
- Documents
- Articles

---

# 13. VILLAGE DISCOVERY

Users should be able to navigate:

Village
→ Village List
→ Selected Village

The village page follows the same database-driven principles as the city page.

The number of villages is determined by the database.

---

# 14. CIVIC DISCOVERY

Civic organizations must not be forced into a single government hierarchy.

A civic organization may relate to:

- A county
- A city
- A village
- Multiple counties
- Multiple cities
- Multiple villages
- Personnel
- Agencies
- Other organizations

The Record Room must allow users to discover civic organizations independently.

---

# 15. PERSONNEL DISCOVERY

Personnel must be independently searchable.

A user should be able to select:

Personnel

and immediately search or browse people.

The user should not have to choose a county, city, state, federal agency, or other organization first.

This is essential because people can have multiple simultaneous or historical relationships.

---

# 16. CROSS-NAVIGATION

After opening a profile, users should be able to follow its relationships.

Example:

White County
→ Housing Authority
→ Pam Deig

or:

Personnel
→ Pam Deig
→ Housing Authority
→ White County
→ Carmi

The same database entity may therefore be reached through multiple navigation paths.

---

# 17. BREADCRUMBS

Breadcrumbs must remain visible near the top of the page.

They show the user's current navigation context.

Example:

API Group
→ Record Room
→ Agency Profiles
→ County
→ White County
→ Housing Authority

Another example:

API Group
→ Record Room
→ Personnel
→ Pam Deig

Breadcrumb links should allow the user to move backward through the hierarchy.

---

# 18. NEW PAGE AT EACH LEVEL

When a user follows a major sidebar link, the system should open a new page/view representing that level of the hierarchy.

Example:

Record Room
↓
County
↓
White County
↓
Housing Authority
↓
Personnel
↓
Pam Deig

Each level can have its own:

- Title
- Description
- Search
- Sidebar
- Content layout
- Cards
- Lists
- Filters
- Related information
- Template

The sidebar can change as the user moves deeper into the hierarchy.

---

# 19. CONTEXTUAL SIDEBARS

A sidebar should reflect the user's current location.

Example:

At the Record Room level:

- Federal
- State
- County
- City
- Village
- Civic
- Personnel

At the White County level:

- County Overview
- Agencies
- Personnel
- Cities
- Villages
- Civic
- Records

At an individual agency:

- Overview
- Departments
- Personnel
- Records
- Documents
- Related Organizations

The exact sidebar contents should be configurable by the administrator.

---

# 20. SIDEBARS MUST NOT BE HARD-CODED

Database-driven lists must never require manually updating the sidebar.

If the database contains:

White County
Edgar County
Vermilion County

the sidebar should display those records automatically.

If:

New County

is added to the database, it should appear automatically wherever the relevant county directory is displayed.

The same principle applies to:

- Agencies
- Personnel
- Cities
- Villages
- Civic organizations
- Other database entities

---

# 21. ADMINISTRATOR SIDEBAR CONTROL

A non-technical administrator must be able to configure sidebars from the CMS.

The administrator should be able to choose:

SIDEBAR POSITION

- None
- Left
- Right
- Both

SIDEBAR CONTENT

- Database list
- Navigation menu
- Related records
- Related profiles
- Search
- Custom links
- Text
- Images
- Widgets
- Other CMS components

The administrator should be able to configure these visually without writing code.

---

# 22. PROFILE LIST PRESENTATION

Not every database result should be displayed as a large card.

The CMS should support:

- Cards
- Compact cards
- Lists
- Directories
- Tables
- Search results
- Profile pages

The administrator should be able to select the appropriate presentation for each context.

---

# 23. PERSONNEL DIRECTORY

Personnel directories should generally favor compact presentation.

A personnel result may include:

[PHOTO]

NAME
Position
Organization
Jurisdiction

The result should be clickable and open the person's full profile.

Large card layouts should not be required when thousands of personnel records eventually exist.

---

# 24. AGENCY DIRECTORY

Agency directories may use cards when appropriate.

An agency card may contain:

[LOGO]

Agency Name
Classification
Jurisdiction
Short Description

Clicking the card opens the agency profile or next level of navigation.

---

# 25. JURISDICTION DIRECTORY

Jurisdiction pages may use visual cards.

For example:

[ILLINOIS]

Illinois

Then:

[WHITE COUNTY]
[EDGAR COUNTY]
[VERMILION COUNTY]

The cards are generated from database records.

If another county is added, another card becomes available automatically.

---

# 26. FEATURED RECORDS

The Record Room landing page may display Featured Records.

An administrator should be able to mark a record as:

Featured

The homepage or Record Room landing page can then automatically display the selected records.

Featured status is a database property.

It should not require manually editing the homepage.

---

# 27. LATEST RECORDS

The Record Room may also display:

Latest Records

These should be generated automatically from the database according to publication/creation/update date.

The administrator should not need to manually add a new record to the Latest Records section.

---

# 28. RECORD TYPES

The Record Room may eventually contain many types of information.

Possible record types include:

- Profiles
- Documents
- Government records
- Public records
- Sources
- Research records
- Reference materials
- Guides
- Checklists
- Other API Group resources

The system must be extensible.

---

# 29. SEARCH RESULTS AND RELATIONSHIPS

Search results should expose useful relationships where appropriate.

Example:

Pam Deig
Executive Director
Housing Authority
White County
Carmi

This allows users to understand the context of a result without opening multiple pages.

---

# 30. RECORD ROOM AND ARTICLES

Articles may reference Record Room entities.

For example:

An API Group article may reference:

- Pam Deig
- Housing Authority
- White County
- City of Carmi

Those references should link back to their corresponding database profiles.

The article and profile remain separate content types.

---

# 31. DATABASE-FIRST ARCHITECTURE

The Record Room must be built around the following principle:

DATABASE
↓
QUERY
↓
RESULTS
↓
TEMPLATE
↓
PAGE

Not:

PAGE
↓
MANUALLY TYPED LINKS
↓
MANUALLY TYPED CONTENT

The database determines what exists.

The CMS determines how it is presented.

---

# 32. EMPTY STATES

If a category contains no records, the page should still function.

Example:

Federal Agencies

No federal agency profiles have been added yet.

The administrator should be able to add the first record without creating a new webpage.

When the first record is added, it should automatically appear in the appropriate directory.

---

# 33. RECORD ROOM GROWTH

The system must not assume a fixed number of:

- Counties
- Cities
- Villages
- Agencies
- Personnel
- Civic organizations
- Records
- Documents

The Record Room must scale according to the database.

The navigation grows with the data.

---

# 34. ADMINISTRATIVE PRINCIPLE

A non-coding administrator should be able to:

- Add a record
- Create a profile
- Add a county
- Add an agency
- Add a person
- Add a civic organization
- Create a relationship
- Assign a category
- Mark a record Featured
- Add an image
- Add a source
- Change a sidebar
- Change a template
- Publish the record

The system should immediately reflect appropriate changes throughout the website.

---

# 35. FINAL RECORD ROOM PRINCIPLE

The Record Room is the public discovery interface for the API Group information system.

It should make the complexity of the underlying database understandable without artificially limiting the relationships between entities.

Users should be able to:

SEARCH directly.

BROWSE hierarchically.

FOLLOW relationships.

RETURN through breadcrumbs.

DISCOVER people independently.

DISCOVER agencies independently.

DISCOVER jurisdictions independently.

FOLLOW cross-jurisdictional connections.

The navigation hierarchy helps users explore the information.

The database relationships determine how the information is actually connected.

The CMS determines how administrators present that information.

The system must remain database-driven from the beginning.