01-API-GROUP-CONTENT-MODEL.md

# 01 — API GROUP CONTENT MODEL

## PURPOSE

This document defines what information exists in the API Group system, how that information is stored, how different types of information relate to one another, and how the website presents those records.

The API Group website is a database-driven information system.

The database is the source of truth.

The website does not consist of individually hand-written pages. Pages, cards, lists, directories, sidebars, search results, profile displays, breadcrumbs, and related-content sections should be generated from database records and relationships.

---

# 1. THE TWO WEBSITE ENTITIES

The overall platform contains two completely independent public website entities:

1. API Group
2. Monster News

They must never be treated as categories or subcategories of one another.

## API GROUP

API Group is the investigative information and research platform.

Its database organizes information concerning:

- Agencies
- Personnel
- Jurisdictions
- Civic organizations
- Contributors
- Partners
- Records
- Documents
- Sources
- Articles
- Programs
- Funding
- Other researched entities
- Relationships between entities

## MONSTER NEWS

Monster News is an independent news and editorial publication.

It has its own:

- Articles
- News categories
- Authors
- Editorial content
- Tags
- Featured stories
- Templates
- Navigation
- Search
- Sidebars
- Homepage
- Administrative controls
- Branding

Monster News is NOT an API Group category.

API Group is NOT a Monster News category.

Monster News must never automatically appear inside API Group navigation.

API Group must never automatically appear inside Monster News navigation.

The two systems may share technical infrastructure and may intentionally reference selected records from one another, but they remain logically independent.

---

# 2. API GROUP DATA MODEL

The API Group database should be organized around entities and relationships rather than around static website pages.

A simplified conceptual model is:

API GROUP
│
├── LIBRARY CONTENT
│   ├── Articles
│   ├── Guides
│   ├── Checklists
│   ├── Agent Training
│   ├── API Group News
│   ├── About API Group
│   └── Other resources
│
└── PROFILES / INFORMATION DATABASE
    ├── Agencies
    ├── Personnel
    ├── Jurisdictions
    ├── Civic Organizations
    ├── Contributors
    ├── Partners
    ├── Records
    ├── Documents
    └── Other entities

This is a conceptual organization of the information.

It must not be interpreted as requiring every database entity to have only one parent.

Relationships are many-to-many whenever appropriate.

---

# 3. CONTENT TYPES VS. DATABASE ENTITIES

The system must distinguish between:

## CONTENT

Content is something intentionally published or presented to users.

Examples:

- Article
- Guide
- Checklist
- News item
- Agent Training document
- About page
- Help article

## ENTITY

An entity is something represented as a structured database object.

Examples:

- Person
- Agency
- County
- City
- Village
- Civic organization
- Contributor
- Partner
- Program
- Government office

## RECORD

A record represents information or evidence associated with an entity or subject.

Examples:

- Public record
- Document
- Filing
- Meeting record
- FOIA record
- OMA record
- Grant record
- Agency record
- Personnel record

An article may discuss an entity.

A record may document an entity.

A profile displays an entity.

A relationship connects entities and records.

These should not be confused with one another.

---

# 4. AGENCY PROFILE

An Agency Profile is a structured database entity.

It is not a manually hard-written webpage.

An Agency Profile may contain fields such as:

- Agency name
- Official name
- Agency type
- Government level
- Jurisdiction
- Geographic coverage
- Parent organization
- Website
- Contact information
- Address
- Phone
- Email
- Description
- Mission
- Authority
- Officials
- Personnel
- Related agencies
- Related organizations
- Related records
- Related documents
- Sources
- Notes
- Tags
- Status
- Dates
- Images/logo
- External references

The exact fields may evolve.

The CMS must allow additional fields to be added without requiring a developer to rebuild every profile page.

---

# 5. AGENCY CLASSIFICATIONS

Initial Agency Profile classifications are:

- Federal
- State
- County
- City
- Village
- Civic

The system must not assume these are the only possible classifications forever.

The administrator must be able to create additional classifications when necessary.

## FEDERAL

Federal agencies or federal entities that:

- Affect Illinois
- Operate in Illinois
- Fund Illinois programs
- Regulate Illinois activity
- Provide services to Illinois
- Monitor Illinois activity
- Have another documented relationship to Illinois

Federal information may be included even when the entity is not physically located in Illinois, provided that its relationship to Illinois is relevant.

## STATE

Illinois state agencies and state-level governmental entities.

## COUNTY

County governments, county agencies, departments, offices, authorities, boards, commissions, and related entities.

## CITY

Municipal governments and city-level entities.

## VILLAGE

Village governments and village-level entities.

## CIVIC

Non-governmental civic organizations and other organizations relevant to the public information system.

The definition of Civic must remain flexible because civic relationships may cross governmental boundaries.

---

# 6. JURISDICTIONS

Jurisdictions are structured database entities.

The initial geographic focus is Illinois.

Possible jurisdiction types include:

- State
- County
- City
- Village
- Township
- District
- Other governmental jurisdiction

Illinois should be represented as a structured jurisdiction rather than simply as text repeated across records.

Example:

State
→ Illinois

County
→ White County

City
→ Carmi

Village
→ Example Village

Relationships connect agencies and personnel to jurisdictions.

---

# 7. PERSONNEL

Personnel are independent database entities.

A personnel record must not be permanently subordinate to one agency, county, city, village, state, or federal organization.

A person may have multiple positions and relationships.

A Personnel Profile may contain:

- Name
- Preferred/display name
- Photograph
- Biography
- Position
- Positions
- Current position
- Former positions
- Agency relationships
- Organization relationships
- Jurisdiction relationships
- Civic relationships
- Contributor relationships
- Partner relationships
- Contact information when appropriate
- Public records
- Documents
- Articles
- Sources
- Tags
- Notes
- Dates
- Status

A person must exist as one database entity even when that person has many relationships.

---

# 8. PERSONNEL RELATIONSHIPS

Personnel relationships are critical to the system.

Example:

PERSON
Pam Deig

RELATIONSHIPS

Position
→ Executive Director

Organization
→ Housing Authority

Jurisdiction
→ White County

Additional Position
→ City of Carmi

City
→ Carmi

Related Agencies
→ Housing Authority
→ Other organizations

Related Records
→ Documents
→ Meetings
→ Articles
→ Other records

The system must allow users to discover the same person through multiple paths.

For example:

Profiles
→ Personnel
→ Pam Deig

or:

Profiles
→ Agency Profiles
→ County
→ White County
→ Housing Authority
→ Personnel

or:

Profiles
→ Agency Profiles
→ City
→ Carmi
→ Personnel

All of these paths can lead to the same underlying person record.

Do not duplicate the person simply because there are multiple discovery paths.

---

# 9. CONTRIBUTORS

Contributors are structured entities.

A contributor may be:

- Person
- Organization
- Publication
- Research group
- Media organization
- Other entity

Contributor relationships may connect to:

- Articles
- Records
- Sources
- Agencies
- Personnel
- Civic organizations
- Other entities

Contributor status and relationships should be stored in the database.

---

# 10. PARTNERS

Partners are first-class entities.

Partners are not miscellaneous articles.

A Partner Profile may represent:

- Organization
- Publication
- Research organization
- Civic organization
- Individual
- Other partner entity

Examples may include:

- Village Voice
- Edgar County Watchdogs

Partners may have relationships with:

- API Group
- Personnel
- Agencies
- Civic organizations
- Articles
- Sources
- Records
- Projects

Contributors and Partners are equally important and must not be treated as lesser content types.

---

# 11. CIVIC ORGANIZATIONS

Civic organizations are structured database entities.

A civic organization may have relationships to:

- Counties
- Cities
- Villages
- Agencies
- Personnel
- Contributors
- Partners
- Articles
- Records
- Programs
- Events

Civic relationships may cross jurisdictional boundaries.

Therefore, Civic should not be forced into a simple:

State → County → City → Civic

parent-child structure.

Instead, civic organizations should be represented as independent entities with relationships to the jurisdictions and organizations they interact with.

---

# 12. RECORDS

Records are structured database objects.

A record may be associated with one or more entities.

Possible record types include:

- Government record
- Public record
- Document
- FOIA record
- OMA record
- Meeting record
- Grant record
- Funding record
- Filing
- Report
- Contract
- Policy
- Ordinance
- Resolution
- Other record

Records should contain appropriate metadata, including when available:

- Title
- Record type
- Date
- Source
- Agency
- Person
- Jurisdiction
- Description
- Document
- URL
- Source reference
- Related entities
- Tags
- Status

---

# 13. DOCUMENTS

Documents are distinct from the entities they describe.

A document may be connected to:

- Agency
- Person
- Jurisdiction
- Civic organization
- Partner
- Contributor
- Article
- Other record

A document may have:

- Title
- Date
- Author
- Source
- File
- URL
- Document type
- Description
- Related entities
- Tags
- Notes

The system should preserve provenance whenever possible.

---

# 14. SOURCES

Sources are structured entities or references.

A source may be:

- Government website
- Government agency
- Public document
- News organization
- Contributor
- Partner
- Public database
- Other source

Source information should be associated with the records and claims it supports.

The system should not rely on an AI model's memory as the source of truth.

---

# 15. ARTICLES

Articles are published content objects.

An API Group article may contain:

- Title
- Subtitle
- Body
- Author
- Publication date
- Updated date
- Category
- Tags
- Featured status
- Image
- Related entities
- Related records
- Sources
- References
- Connections

Articles may reference profiles without becoming profiles.

A profile may be referenced by an article without becoming part of the article itself.

---

# 16. LIBRARY CONTENT

API Group Library content is separate from the Profiles database.

The Library contains information about API Group and resources useful to people using or contributing to the system.

Initial Library content categories include:

- API Group News
- Guides
- Checklists
- Agent Training
- About API Group
- How to Contribute
- Help / Tips & Tricks

The administrator must be able to create additional Library categories.

Library categories are database records.

Library articles are database records.

Library navigation should be generated from those records.

---

# 17. AGENT TRAINING

Agent Training is a Library category.

Agent Training contains documents intended to teach AI agents how to understand and work with API Group.

Each training document should be capable of becoming an individual article/resource within:

API Group
→ API Group Library
→ Agent Training

The training documents may define:

- Architecture
- Data structures
- Content rules
- Profile rules
- Navigation rules
- Database behavior
- Administrative rules
- AI operating rules
- Research procedures
- Other system requirements

Agent Training is not the same thing as API Group Profiles.

It describes how the system works.

Profiles contain the information the system is collecting.

---

# 18. TAGS

Tags provide an additional discovery mechanism.

Tags must not replace structured relationships.

For example:

A person may have the tag:

"White County"

but the actual relationship should also exist in the database:

Person
→ jurisdiction
→ White County

Tags are useful for:

- Search
- Topic discovery
- Editorial organization
- Related content
- News connections

Structured relationships are authoritative for entity connections.

---

# 19. RELATIONSHIPS

Relationships are a core part of the database.

Examples:

PERSON
→ works_for
→ AGENCY

AGENCY
→ located_in
→ COUNTY

COUNTY
→ part_of
→ ILLINOIS

PERSON
→ holds_position
→ POSITION

POSITION
→ belongs_to
→ AGENCY

CIVIC ORGANIZATION
→ operates_in
→ CITY

PARTNER
→ contributes_to
→ API GROUP

ARTICLE
→ references
→ PERSON

ARTICLE
→ references
→ AGENCY

RECORD
→ concerns
→ PERSON

RECORD
→ concerns
→ AGENCY

The database should store relationships explicitly.

The frontend should query and display them.

---

# 20. MANY-TO-MANY RELATIONSHIPS

The system must support many-to-many relationships.

Examples:

One person may work for multiple organizations.

One agency may operate across multiple jurisdictions.

One civic organization may operate across multiple counties.

One article may reference many people.

One person may be referenced by many articles.

One record may concern multiple agencies.

One agency may have many records.

Do not design the database around the assumption that one entity can have only one parent.

---

# 21. DATABASE-DRIVEN NAVIGATION

Navigation must be generated from database records whenever the navigation represents database entities.

Example:

COUNTIES

The system queries:

All jurisdiction records
where type = County
and state = Illinois

It then displays the resulting records.

Do not hard-code:

Adams County
Edgar County
White County

into the frontend.

If the database changes, navigation changes automatically.

---

# 22. DATABASE-DRIVEN CARDS

Cards must be generated from database records.

Example:

Agency Profiles
→ Federal
→ State
→ County
→ City
→ Village
→ Civic

If a new profile type is created through the CMS, it can automatically become available wherever profile categories are displayed.

Likewise:

County records
→ 10 database records
→ 10 cards

Add another county:

County records
→ 11 database records
→ 11 cards

The administrator should never need to ask a developer to manually create a new card.

---

# 23. DATABASE-DRIVEN SIDEBARS

Sidebar lists that represent entities must be generated from the database.

Example:

LEFT SIDEBAR

COUNTIES

Adams County
Edgar County
White County
...

These are not manually authored navigation links.

They are database results.

When a new county is added, the sidebar automatically includes it.

When a county is removed or renamed, the sidebar automatically reflects the database.

---

# 24. DATABASE-DRIVEN BREADCRUMBS

Breadcrumbs should represent the user's current navigation path.

Where the path corresponds to database entities, the breadcrumb should be generated from the current record and its relationships.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ Attorney General

The breadcrumb links must remain usable as the user navigates deeper.

---

# 25. PROFILE PRESENTATION

Profiles are rendered through reusable templates.

The profile itself is database data.

The template determines presentation.

This means the same Personnel Profile can be displayed through the same template regardless of whether the user reached it from:

- Personnel
- Agency
- County
- City
- Village
- Civic
- Search
- Article
- Related record
- Another profile

The data remains the same.

Only the navigation context may change.

---

# 26. SEARCH

Search must search the database rather than a collection of manually maintained pages.

Search should eventually be capable of searching:

- Profiles
- Personnel
- Agencies
- Jurisdictions
- Civic organizations
- Contributors
- Partners
- Articles
- Documents
- Records
- Sources
- Tags
- Relationships

Search should be able to return the appropriate type of result and link to the underlying record.

---

# 27. CROSS-NAVIGATION

Users should be able to navigate between related entities.

Example:

PERSONNEL PROFILE
Pam Deig

Related:

Housing Authority
White County
Carmi
Related Agencies
Related Civic Organizations
Related Articles
Related Records
Related Sources

Likewise, an agency profile should show relevant personnel.

A county profile should show relevant agencies.

A city profile should show relevant agencies and personnel.

A civic profile should show related personnel, jurisdictions, agencies, and records.

This is relationship-driven navigation.

---

# 28. NO DUPLICATION OF DATABASE ENTITIES

The system must avoid creating duplicate records merely because an entity appears in multiple categories or navigation paths.

Example:

There is one Pam Deig record.

That record may be displayed through:

Personnel
White County
Carmi
Housing Authority
Articles
Search
Related Records

There should not be five separate Pam Deig database records.

---

# 29. CONTENT AND DATABASE SEPARATION

An article about an agency is not the agency.

A profile about an agency is the agency's structured database representation.

A document about an agency is a document.

A record concerning an agency is a record.

A news article mentioning an agency is a news article.

They may all be connected through relationships.

They must not be collapsed into one object simply because they concern the same subject.

---

# 30. MONSTER NEWS DATA

Monster News has its own content model.

At minimum it may contain:

- News Article
- News Category
- Author
- Contributor
- Image
- Tag
- Reference
- Featured Story
- Related Story

Monster News data must remain separate from API Group Library content.

Monster News articles may intentionally reference API Group entities.

For example:

Monster News Article
→ references
→ Pam Deig

or:

Monster News Article
→ references
→ White County

or:

Monster News Article
→ references
→ Housing Authority

Those references should point to existing API Group database records where appropriate.

This does not turn the Monster News article into an API Group article.

---

# 31. API GROUP / MONSTER NEWS CROSS-REFERENCE

The two systems may share selected database relationships.

Example:

MONSTER NEWS ARTICLE
"The Housing Authority Controversy"

References:

→ White County
→ Housing Authority
→ Pam Deig
→ Carmi
→ Related API Group Records

The Monster News article remains a Monster News article.

The API Group entities remain API Group entities.

The connection is intentional and database-driven.

---

# 32. CONTROL PANEL REQUIREMENT

The administrator must be able to manage the content model without coding.

The CMS should provide tools for:

- Creating entities
- Editing entities
- Creating articles
- Creating categories
- Creating relationships
- Adding fields
- Creating templates
- Configuring layouts
- Managing sidebars
- Managing navigation
- Managing featured content
- Managing tags
- Managing sources
- Managing records
- Managing publishing status

API Group and Monster News must have separate logical administrative environments.

---

# 33. AI DATA CREATION

Authorized AI should be able to create and update database records.

AI should be able to enter structured data.

Example:

Entity Type:
County

Name:
White County

State:
Illinois

or:

Entity Type:
Personnel

Name:
Pam Deig

Position:
Executive Director

Organization:
Housing Authority

Jurisdiction:
White County

Additional Relationship:
City of Carmi

The AI should be creating or updating the underlying record and relationships.

It should not be manually constructing a new HTML page.

---

# 34. AUTOMATIC PROPAGATION

When a new database entity is created, applicable website components must automatically recognize it.

Example:

An administrator adds:

County
→ New County

The system should automatically make that record available to:

- County directories
- County cards
- County sidebars
- Search
- Breadcrumbs
- Related records
- Profile navigation
- Other applicable database queries

No frontend code change should be required.

---

# 35. EXTENSIBILITY

The content model must be designed to grow.

Do not assume the final system will contain only:

- Federal
- State
- County
- City
- Village
- Civic
- Personnel

Additional entity types may eventually be required.

Examples:

- Township
- School District
- Special District
- Authority
- Board
- Commission
- Program
- Contractor
- Grant
- Election
- Organization
- Event
- Other public-interest entities

The CMS should make it possible to add new types and relationships without rebuilding the entire site.

---

# 36. FUNDAMENTAL RULE

The most important rule in this document is:

THE DATABASE DEFINES WHAT EXISTS.

THE RELATIONSHIPS DEFINE HOW THINGS ARE CONNECTED.

THE CMS DEFINES HOW ADMINISTRATORS MANAGE THE INFORMATION.

THE TEMPLATES DEFINE HOW INFORMATION IS DISPLAYED.

THE NAVIGATION DEFINES HOW USERS DISCOVER THE INFORMATION.

THE WEBSITE SHOULD NEVER REQUIRE A DEVELOPER TO MANUALLY BUILD A NEW PAGE, CARD, SIDEBAR LINK, OR NAVIGATION ITEM FOR EVERY NEW DATABASE RECORD.

API Group is therefore not a collection of static webpages.

It is a database-driven information system presented through a configurable content-management interface.