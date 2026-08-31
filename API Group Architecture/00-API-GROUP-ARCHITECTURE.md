00-API-GROUP-ARCHITECTURE.md

# 00 — API GROUP ARCHITECTURE

API Group is a database-driven public information and research platform. The database is the source of truth; the website is the presentation and navigation layer.

## 1. TWO COMPLETELY SEPARATE WEBSITE ENTITIES

The platform contains two independent public website entities:

- API Group
- Monster News

They may share underlying technology and may intentionally reference selected data from one another, but they are NOT part of the same website hierarchy.

### API Group

API Group contains the API Group Library and the database-driven Profiles system.

### Monster News

Monster News is an entirely independent news and editorial publication system with its own:

- Branding
- Logo
- Navigation
- Homepage
- Categories
- Articles
- Article templates
- Editorial controls
- Featured content
- Search
- Breadcrumbs
- Sidebars
- Publishing workflow
- Control panel

Monster News must never automatically appear as a category, subcategory, profile, article, breadcrumb, sidebar item, search result, or navigation item within API Group.

API Group content must likewise not automatically become Monster News content.

Monster News may intentionally reference API Group information through controlled database relationships.

---

# 2. API GROUP TOP-LEVEL STRUCTURE

The API Group public navigation should remain simple:

API GROUP
├── API GROUP LIBRARY
└── PROFILES

API Group Library and Profiles are siblings.

Profiles is NOT a dependency of Library.

Library is NOT a dependency of Profiles.

---

# 3. API GROUP LIBRARY

The public-facing section should be called:

API GROUP LIBRARY

The Library contains resources and information about API Group, including its news, guidance, training, participation, operation, and related material.

Initial Library categories may include:

- API Group News
- Guides
- Checklists
- Agent Training
- About API Group
- How to Contribute
- Help / Tips & Tricks

These are initial examples, not a permanent hard-coded list.

The administrator must be able to create additional Library categories through the CMS without coding.

When a new Library category is created, it should automatically become available wherever Library categories are displayed.

Library content is database-driven.

The Library landing page should support:

- Search
- Category browsing
- Featured articles
- Latest articles
- Article cards
- Record/article lists
- Breadcrumbs
- Configurable sidebars
- Editorial footer

Prominent Library search language should communicate:

"Search the API Group Collection by Title, Source, Topic, or Record."

---

# 4. PROFILES

Profiles are the structured information system for entities being researched and connected by API Group.

Profiles are NOT ordinary hand-written articles.

A profile is a database record displayed through a reusable profile template.

The database is the source of truth.

Initial profile/entity types may include:

- Agency Profiles
- Personnel
- Civic
- Contributors
- Partners

Additional entity types must be possible through the CMS.

Profiles must not be restricted to a rigid parent/child structure.

An entity may have many relationships.

For example, one person may simultaneously be connected to:

- A federal agency
- A state agency
- A county agency
- A city government
- A village
- A civic organization
- A contributor
- A partner
- Multiple records

The person remains one database entity.

Relationships determine how that person can be discovered.

---

# 5. AGENCY PROFILES

Agency Profiles are database-driven.

Initial classifications may include:

- Federal
- State
- County
- City
- Village
- Civic

The primary geographic focus is Illinois.

Federal entities may be included when they affect, serve, fund, regulate, monitor, or otherwise have relevance to Illinois.

Agency navigation may progressively move through the hierarchy.

Example:

Profiles
→ Agency Profiles
→ State
→ Illinois
→ State Agency
→ Attorney General
→ FOIA

Each step may be represented by a separate page.

---

# 6. PERSONNEL

Personnel profiles are independent database entities.

A personnel profile must NOT permanently belong to only one:

- State
- County
- City
- Village
- Federal agency
- Civic organization
- Agency

Instead, relationships connect personnel to those entities.

Example:

Pam Deig
→ Position: Executive Director
→ Organization: Housing Authority
→ Geographic Relationship: White County
→ Additional Position/Relationship: City of Carmi
→ Related Organizations
→ Related Agencies
→ Related Records

The same personnel profile must be discoverable from multiple appropriate navigation paths.

The database must not duplicate the person's profile merely because the person has multiple relationships.

---

# 7. CONTRIBUTORS AND PARTNERS

Contributors and partners are first-class entities.

They must not be treated as miscellaneous articles or secondary content.

Organizations such as:

- Village Voice
- Edgar County Watchdogs

may have their own database-driven profiles.

They may have relationships with:

- Personnel
- Agencies
- Civic organizations
- Jurisdictions
- Articles
- Sources
- Records
- Other organizations

Their profiles and relationships are equally important to the system.

---

# 8. DATABASE-FIRST PRINCIPLE

THE DATABASE IS THE SOURCE OF TRUTH.

The following must be generated from database records whenever applicable:

- Navigation
- Sidebar links
- Cards
- Directories
- Search results
- Breadcrumb destinations
- Profile pages
- Related records
- Related personnel
- Related agencies
- Category lists
- Subcategory lists
- Featured content
- Latest content
- Tags
- Connections
- References

Do not hard-code entity names into the frontend.

Do not hard-code the number of entities.

If the database contains 10 counties, display 10.

If it contains 100 counties or county-related records, display the appropriate 100 records.

If another record is added, applicable database-driven components automatically update.

If a record is changed, applicable displays update.

If a record is removed, applicable displays update.

---

# 9. AI DATA INJECTION

Authorized AI must be able to create and update structured database information through the CMS.

AI must be able to provide structured information such as:

Entity Type: County
Name: Vermilion County
State: Illinois

or:

Entity Type: Agency
Name: Example Agency
Jurisdiction: White County
State: Illinois

or:

Entity Type: Personnel
Name: Example Person
Position: Example Position
Organization: Example Agency

AI must not be limited to generating prose.

AI must be capable of creating and updating structured records and relationships.

When an authorized administrator or AI creates a new entity, applicable:

- Navigation
- Cards
- Directories
- Search results
- Breadcrumbs
- Related records
- Profile displays

must automatically reflect the new record.

---

# 10. DYNAMIC NAVIGATION

Navigation must be generated from the database and current page context.

There must be no fixed number of:

- Counties
- Cities
- Villages
- Agencies
- Personnel
- Civic organizations
- Contributors
- Partners
- Other entities

A sidebar containing counties, for example, should query the database.

Example:

COUNTIES

Adams County
Edgar County
White County
Vermilion County
...

If another county/entity record is added, it automatically becomes available.

The sidebar is a database view, not a manually maintained list of links.

---

# 11. HIERARCHICAL PAGE NAVIGATION

When a user clicks a hierarchy item, it normally opens a new page representing that level.

This is not simply a filter applied to the same page.

Example:

API Group
→ API Group Library
→ State Records
→ Illinois
→ Attorney General
→ FOIA

or:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ Attorney General

Each level may have its own page layout, content, sidebar configuration, and database-driven navigation.

---

# 12. BREADCRUMBS

Breadcrumbs remain visible as the user moves through the hierarchy.

Example:

API Group
→ API Group Library
→ Guides
→ Research Guide

or:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ Attorney General
→ FOIA

Each breadcrumb item should be clickable.

Breadcrumbs allow users to move back up the hierarchy at any time.

The breadcrumb represents:

WHERE AM I?
AND
HOW DO I GET BACK?

---

# 13. SIDEBAR ARCHITECTURE

Sidebars are configurable independently for each page or template.

A page may have:

- Left Sidebar
- Right Sidebar
- Both Sidebars
- No Sidebar

The normal default for hierarchical browsing should be the Left Sidebar.

Profiles may frequently use:

- Left Sidebar for navigation
- Right Sidebar for connections and related information

Example:

LEFT SIDEBAR
= Where can I go next?

RIGHT SIDEBAR
= What is connected to what I am viewing?

The page administrator must be able to choose the sidebar configuration without coding.

---

# 14. DYNAMIC SIDEBAR BEHAVIOR

The sidebar changes as the user moves down the hierarchy.

The system must NOT create one giant permanent sidebar containing every possible category and entity.

Instead, the sidebar represents the user's current location and available navigation at that level.

Example:

Record Room / Collection
→ State
→ Illinois

The sidebar may then change to display Illinois-related navigation.

If the user selects Attorney General, the next page may display:

Attorney General
- FOIA
- OMA
- Opinions
- Enforcement
- Other database-created categories

If a new category is added through the CMS, it automatically becomes available in the appropriate sidebar.

---

# 15. SIDEBAR CONTENT

The administrator must be able to manage sidebars without coding.

The CMS should allow the administrator to:

- Turn the left sidebar on/off
- Turn the right sidebar on/off
- Select sidebar content
- Add/remove sidebar blocks
- Add lists of links
- Display related records
- Display categories
- Display database-generated lists
- Reorder sidebar components
- Configure different sidebars for different templates/pages

Lists representing database entities must be generated dynamically.

---

# 16. CARDS

Cards should be reusable presentation components.

Cards may represent:

- Library categories
- Articles
- Agencies
- Counties
- Cities
- Villages
- Civic organizations
- Personnel
- Contributors
- Partners
- Other database entities

Cards must be generated from the underlying database records.

Do not manually create individual cards in code.

Example:

DATABASE
→ 10 COUNTY RECORDS
→ 10 COUNTY CARDS

If an additional county record is added:

DATABASE
→ 11 COUNTY RECORDS
→ 11 COUNTY CARDS

The layout automatically adjusts.

Personnel may require a more compact presentation than agencies or categories.

Personnel listings should support:

- Name
- Thumbnail/photo when available
- Position
- Organization
- Relevant relationship information

---

# 17. API GROUP LIBRARY / RECORD ROOM CONCEPT

The public-facing destination should be called:

API GROUP LIBRARY

The Library is the public collection of API Group resources and information.

The visual collection/search experience may use a Record Room concept where appropriate, but "API Group Library" is the primary public name.

The Library should explain what material is available and provide discovery through:

- Search
- Categories
- Records
- Articles
- Sources
- Topics

Search should support language such as:

"Search the API Group Collection by Title, Source, Topic, or Record."

---

# 18. RECORD TYPES

The collection may contain many types of records.

The Record Room/collection experience should allow users to discover available record types rather than forcing everything into the Profiles hierarchy.

Possible record types include:

- Federal Records
- State Records
- Agency Records
- County Records
- City Records
- Village Records
- Civic Records
- Personnel Records
- Documents
- Programs
- Funding
- Other database-created record types

These are not permanent hard-coded categories.

The administrator must be able to add additional record types.

---

# 19. RECORD ROOM HIERARCHICAL BROWSING

The collection can be explored hierarchically.

For example:

API Group Library
→ State Records
→ Illinois
→ State Agencies
→ Attorney General
→ FOIA
→ Individual Record

Each step may open a new page.

The breadcrumb remains visible.

The sidebar changes to represent the current level.

The content area displays the records, categories, cards, or articles available at that level.

---

# 20. PROFILES VS. RECORD ROOM

These are two different ways of exploring the same underlying information.

PROFILES answers:

"Who and what are connected?"

The Record Room / collection answers:

"What records and information do we have?"

A user might find a person through:

Profiles
→ Personnel
→ Pam Deig

Another user might reach the same personnel record through:

API Group Library
→ County Records
→ White County
→ Housing Authority
→ Personnel

Both paths can lead to the same underlying database entity.

Do not duplicate the entity merely because it is discoverable through multiple paths.

---

# 21. SEARCH

Search must be database-driven.

Search should eventually support:

- Library content
- Profiles
- Agencies
- Personnel
- Organizations
- Jurisdictions
- Records
- Articles
- Sources
- Relationships

Search results should link to the underlying database-driven page or profile.

---

# 22. RELATIONSHIP MODEL

Relationships are fundamental.

The system should store relationships as structured database relationships rather than duplicating information into multiple pages.

Example:

Pam Deig
↕
Housing Authority
↕
White County
↕
Carmi
↕
Related Civic Organizations
↕
Related Records

A relationship can be displayed from multiple directions.

The relationship should be stored once and rendered wherever appropriate.

---

# 23. MONSTER NEWS INTEGRATION

Monster News remains independent.

However, an editor may intentionally associate a Monster News article with API Group entities.

Example:

MONSTER NEWS ARTICLE
├── Tags
├── References
├── Related Articles
└── API GROUP CONNECTIONS
    ├── Agency
    ├── Personnel
    ├── County
    ├── City
    ├── Village
    ├── Civic Organization
    ├── Contributor
    └── Partner

These connections are optional and intentional.

A Monster News article does not become an API Group article because it references an API Group profile.

An API Group profile does not become a Monster News article because it is referenced by a news story.

---

# 24. MONSTER NEWS CONTROL PANEL

Monster News must have its own independent control-panel experience.

The Monster News administrator must be able to manage independently:

- News article templates
- Categories
- Subcategories
- Article layouts
- Featured stories
- Latest stories
- Authors
- Contributors
- Images
- Media
- Tags
- References
- Related content
- Sidebars
- Navigation
- Breadcrumbs
- Homepage sections
- Publishing status

The Monster News control panel must not require coding for normal administrative operations.

The API Group control panel and Monster News control panel may technically exist inside one administrative application, but their content management environments must remain logically and visually separated.

---

# 25. TEMPLATE SYSTEM

Templates must be reusable and database-driven.

The administrator should be able to configure or create templates for:

- Library articles
- Agency profiles
- Personnel profiles
- Organization profiles
- Civic profiles
- Contributor profiles
- Partner profiles
- News articles
- Category pages
- Directory pages
- Landing pages

Templates control presentation.

Templates do not replace the database record.

---

# 26. HOMEPAGE

The API Group homepage should function as the public entry point into the API Group information system.

It should include:

- Correct API Group branding
- Main navigation
- Search
- Featured content
- Latest content
- Library access
- Profiles access
- Editorial/card-based presentation
- Footer

Featured content should be database-driven.

An administrator should be able to mark an article or record as Featured.

New/latest content should be generated automatically from publishing dates or configured CMS rules.

The homepage must not require developers to manually add new cards every time content is created.

---

# 27. VISUAL DESIGN

The existing APIG Resources Platform is the primary visual reference.

Preserve the visual qualities we like, including:

- Editorial/card-based presentation
- Strong typography
- Clear spacing
- Search presentation
- Featured content
- Category cards
- Breadcrumbs
- Sidebar navigation
- Attractive footer
- Responsive behavior
- Professional editorial appearance

Monster News has its own separate visual identity.

The Monster News identity is specifically based around:

- Bubblegum pink
- Black
- White
- Gold

The Monster News visual system may use its own:

- Typography
- Cards
- Borders
- Badges
- Stickers
- Shadows
- Layout
- Editorial treatments

Do not merge API Group and Monster News visual identities.

Use the correct logo for each website context.

---

# 28. NAVIGATION LINKS

Current navigation links on the existing website are not necessarily correct or final.

The current site should be studied for its:

- Visual navigation treatment
- Header structure
- Link presentation
- Spacing
- Mobile behavior
- Sidebar behavior

Do not assume current link destinations are final.

The CMS must allow navigation to be changed without coding.

---

# 29. ADMINISTRATOR EXPERIENCE

The administrator should require no coding experience.

The administrator should be able to work from the control panel and, where appropriate, from the public-facing interface.

The administrator should be able to:

- Create records
- Edit records
- Create categories
- Create subcategories
- Create profiles
- Create relationships
- Create articles
- Create templates
- Configure layouts
- Turn sidebars on/off
- Configure sidebar content
- Manage navigation
- Feature content
- Manage latest content
- Manage media
- Manage tags
- Manage references
- Manage publishing
- Configure breadcrumbs
- Preview changes
- Publish changes

---

# 30. AI + DATABASE + CMS

AI is a potential data-entry and research assistant.

AI should be able to inject structured information into the database through authorized interfaces.

The system should be designed so that AI-created information can be:

- Validated
- Reviewed
- Edited
- Approved
- Published
- Connected to existing entities
- Used by templates
- Used by navigation
- Used by search

AI should not be required to create HTML pages manually for each profile.

AI should create or update the underlying structured records.

---

# 31. NO HARD-CODED ENTITY NAVIGATION

This rule is critical.

Do not build:

"Here are the ten counties."

Build:

"Display every database record classified as a county within the current geographic context."

Do not build:

"Here are the current agencies."

Build:

"Query the database for agencies applicable to the current context and display the results."

Do not manually create navigation links for every new entity.

The database determines what exists.

The CMS determines how it is presented.

---

# 32. PAGE LAYOUT CONFIGURATION

Each page/template should have configurable layout settings.

Possible configurations include:

- Full width
- Left sidebar + content
- Content + right sidebar
- Left sidebar + content + right sidebar
- No sidebar

The administrator should be able to change the configuration without coding.

Different pages at different hierarchy levels may use different configurations.

Example:

Agency browsing:
Left sidebar + content

Personnel profile:
Left sidebar + content + right sidebar

Simple article:
Full width

The administrator determines the appropriate presentation.

---

# 33. BREADCRUMB + SIDEBAR + CONTENT MODEL

Every hierarchical page should conceptually contain:

BREADCRUMB
→ Shows the user's path

SIDEBAR
→ Shows relevant navigation at the current level

MAIN CONTENT
→ Shows the records/articles/entities at the current level

OPTIONAL RIGHT SIDEBAR
→ Shows relationships, references, related records, or other contextual information

FOOTER
→ Provides site-wide editorial/footer content

These are separate functional components.

---

# 34. BUILD PHILOSOPHY

Do not attempt to finish the entire information architecture before deploying the first working version.

The immediate goal is to get a functional API Group website online quickly.

Once the basic system is online, use demonstration data and real content to evaluate:

- Cards
- Search
- Breadcrumbs
- Hierarchical navigation
- Dynamic sidebars
- Profile layouts
- Related records
- Database relationships
- Different page layouts
- AI-created records
- Templates

The system must be built for iteration.

Do not create temporary hard-coded structures that prevent later database-driven behavior.

---

# 35. FUNDAMENTAL ARCHITECTURAL PRINCIPLE

API Group is not a collection of individually hand-built pages.

It is a database-driven information system with a public presentation layer.

The database stores the information.

Relationships connect the information.

The CMS allows humans and authorized AI to manage the information.

Templates determine how information is presented.

Navigation allows users to explore the information.

Search allows users to find the information.

Cards, sidebars, breadcrumbs, directories, and profile pages are dynamic views of the underlying information.

The system must be capable of growing substantially without requiring a developer to manually create a new page or navigation link for every new record.

The website hierarchy is a way of navigating the database.

The website hierarchy is NOT the database itself.