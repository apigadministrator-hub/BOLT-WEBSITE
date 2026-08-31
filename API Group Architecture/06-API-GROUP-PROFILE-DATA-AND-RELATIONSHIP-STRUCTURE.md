# 06 — API GROUP PROFILE DATA AND RELATIONSHIP STRUCTURE

## PURPOSE

API Group Profiles are database-driven entities.

They are not hard-written webpages.

The public profile pages are generated from structured database information and reusable templates.

The database is the source of truth.

The website is a presentation layer for that information.

This document defines how profiles, entities, jurisdictions, agencies, personnel, civic organizations, and their relationships should work together.

---

# 1. CORE PRINCIPLE

A profile is an entity in the database.

A profile is not a static article.

The system should be able to create a public profile page from database information without requiring an administrator to manually build a webpage.

Example:

PERSON
Pam Deig

The system stores the person.

The system then determines what information is connected to Pam Deig.

A personnel-profile template determines how that information is displayed.

---

# 2. PROFILE TYPES

The initial API Group profile system should support at least:

- Agency
- Personnel
- County
- City
- Village
- Civic Organization
- State
- Federal Entity

Additional entity types may be added later.

The architecture must not require rebuilding the CMS when a new profile type is introduced.

---

# 3. PROFILE IDENTITY

Every profile must have a unique database identity.

The identity should remain independent from where the profile is encountered.

For example:

Pam Deig

is one person.

She should not become a different person merely because she is encountered through:

- White County
- City of Carmi
- Housing Authority
- Personnel
- Agency
- Civic

The same database entity should be referenced from all applicable contexts.

---

# 4. PERSONNEL ARE NOT CHILD PAGES OF A JURISDICTION

Personnel profiles must not be permanently dependent upon:

- Federal
- State
- County
- City
- Village
- Civic

A person's profile exists independently.

The person can have relationships with any combination of those entities.

This prevents duplicate profiles.

---

# 5. EXAMPLE: PAM DEIG

The database may contain:

PERSON
Pam Deig

RELATIONSHIPS:

Pam Deig
→ holds_position
→ Executive Director

Pam Deig
→ works_for
→ Housing Authority

Housing Authority
→ located_in
→ White County

Pam Deig
→ holds_position
→ City of Carmi

Pam Deig
→ associated_with
→ City of Carmi

The exact relationship types should be configurable.

The important principle is that all of these relationships connect to the same person entity.

---

# 6. RELATIONSHIPS ARE FIRST-CLASS DATA

Relationships must be stored as structured database records.

A relationship should contain information such as:

- Source entity
- Relationship type
- Target entity
- Position, where applicable
- Start date, where applicable
- End date, where applicable
- Source
- Confidence
- Notes
- Status

Example:

SOURCE ENTITY:
Pam Deig

RELATIONSHIP:
holds_position

TARGET ENTITY:
Executive Director

ORGANIZATION:
Housing Authority

JURISDICTION:
White County

SOURCE:
Public record

---

# 7. RELATIONSHIP TYPES

The system should support multiple relationship types.

Examples:

- works_for
- employed_by
- holds_position
- member_of
- appointed_by
- elected_to
- represents
- governs
- located_in
- serves
- oversees
- reports_to
- associated_with
- connected_to
- funds
- regulates
- contracts_with
- partners_with
- references
- related_to

The relationship vocabulary should be extensible.

---

# 8. POSITION IS A SEPARATE CONCEPT

A person's position should not simply be stored as free text when the relationship needs to be tracked.

Instead:

PERSON
Pam Deig

POSITION
Executive Director

ORGANIZATION
Housing Authority

This allows the system to determine who currently holds a position and who previously held it.

---

# 9. POSITION HISTORY

Positions should support historical information.

Example:

Pam Deig
→ held
→ Executive Director
→ Housing Authority
→ Start: 2021
→ End: Present

If she later leaves the position, the relationship can be closed without deleting the historical record.

---

# 10. MULTIPLE POSITIONS

One person may hold multiple positions.

Example:

PERSON
Pam Deig

POSITION A
Executive Director
Housing Authority

POSITION B
City position
City of Carmi

Both relationships belong to the same person profile.

---

# 11. MULTIPLE JURISDICTIONS

A person may be connected to multiple jurisdictions.

For example:

Federal
State of Illinois
White County
Carmi

The system must allow all applicable relationships simultaneously.

---

# 12. JURISDICTION IS A RELATIONSHIP

Jurisdiction should generally be modeled as data rather than determining the person's identity.

Example:

Pam Deig
→ associated_with
→ White County

Pam Deig
→ associated_with
→ Carmi

This means a personnel profile can be discovered from either jurisdiction.

---

# 13. AGENCY PROFILES

Agency profiles should be independent entities.

Example:

Housing Authority

The agency profile may contain:

- Name
- Agency type
- Government level
- Jurisdiction
- Address
- Website
- Contact information
- Personnel
- Leadership
- Programs
- Documents
- Sources
- Related articles
- Related civic organizations

---

# 14. AGENCY CLASSIFICATION

Initial Agency Profile classifications:

- Federal
- State
- County
- City
- Village
- Civic

The classification should be stored as structured data.

The administrator should be able to add classifications later.

---

# 15. FEDERAL AGENCIES

Federal agencies may be included when they have relevance to Illinois.

Examples may include federal entities that:

- Operate in Illinois
- Fund Illinois programs
- Regulate Illinois activities
- Investigate Illinois matters
- Provide grants
- Maintain Illinois offices
- Otherwise materially affect Illinois

The system should not require every federal agency in existence to be included.

The database contains the federal entities being monitored or documented by API Group.

---

# 16. STATE PROFILES

State profiles should represent Illinois state entities relevant to the project.

Examples:

- State agencies
- State offices
- State departments
- State boards
- State commissions
- State legislative entities
- Other state entities

The system should permit sub-agencies and divisions.

---

# 17. COUNTY PROFILES

County profiles represent Illinois counties being documented.

A county may contain relationships to:

- County agencies
- County personnel
- Cities
- Villages
- Civic organizations
- Documents
- Articles
- Other entities

---

# 18. CITY PROFILES

Cities are independent entities.

A city may belong geographically to a county while still maintaining its own relationships.

Example:

Carmi
→ located_in
→ White County

Carmi may then have:

- City agencies
- City personnel
- Civic relationships
- Documents
- Articles

---

# 19. VILLAGE PROFILES

Villages function similarly to cities.

A village is its own database entity.

It may be associated with:

- County
- State
- Agencies
- Personnel
- Civic organizations
- Documents
- Articles

---

# 20. CIVIC ORGANIZATIONS

Civic organizations must be treated as first-class entities.

They are not merely tags.

Examples may include:

- Community organizations
- Advocacy organizations
- Nonprofits
- Civic groups
- Watchdog organizations
- Community media
- Other relevant organizations

---

# 21. CONTRIBUTORS AND PARTNERS

Contributor and partner organizations are important entities.

Examples include:

Village Voice

Edgar County Watchdogs

These organizations should have their own profiles where appropriate.

They must not be treated as less important simply because they are not governmental agencies.

Their relationships to API Group and other entities should be representable in the database.

---

# 22. MEDIA ORGANIZATIONS

Media organizations may be connected to:

- Personnel
- Agencies
- Counties
- Cities
- Villages
- Civic organizations
- Articles
- Sources

A media organization can therefore participate in the same relationship system as other entities.

---

# 23. SOURCE AND PROVENANCE

Profile information should identify where information came from.

Possible sources:

- Government website
- Public record
- Document
- Meeting minutes
- Filing
- News article
- Contributor
- API Group research
- AI-assisted research
- Other documented source

The source should be stored as structured information where practical.

---

# 24. PROFILE DATA SHOULD BE MODULAR

Not every profile has the same fields.

An agency may need:

- Agency type
- Jurisdiction
- Address
- Website
- Leadership

A person may need:

- Name
- Photograph
- Positions
- Organizations
- Jurisdictions

A civic organization may need:

- Organization type
- Mission
- Personnel
- Partnerships
- Sources

The CMS should allow different profile templates and field sets.

---

# 25. REQUIRED VS OPTIONAL DATA

Profile schemas should distinguish between:

REQUIRED

and

OPTIONAL

information.

A profile should be allowed to exist even when information is incomplete.

Missing information should not require fake placeholder data.

---

# 26. INCOMPLETE PROFILES

A profile may initially contain only:

Name
Type
Source

Additional information can be added later.

The public profile template should gracefully handle missing fields.

---

# 27. AI PROFILE CREATION

AI should be able to propose or create structured profile records.

Example:

AI discovers:

County:
Example County

State:
Illinois

The AI can submit a structured entity.

The CMS then:

1. Checks for duplicates.
2. Validates required fields.
3. Creates or proposes the entity.
4. Creates applicable relationships.
5. Makes the entity available to configured database-driven lists.

---

# 28. AI RELATIONSHIP CREATION

AI may also propose relationships.

Example:

Pam Deig
→ Executive Director
→ Housing Authority

The AI should submit the relationship as structured data.

The administrator may review and approve it.

---

# 29. DATABASE-DRIVEN SIDEBARS

Sidebars must query the database.

Example:

LEFT SIDEBAR

Illinois Counties

The sidebar should not contain a hard-coded list.

Instead:

QUERY:
Entity Type = County
State = Illinois
Status = Published

RESULT:
All matching counties

---

# 30. AUTOMATIC SIDEBAR UPDATES

If a new county is added:

Example County

then the county sidebar should automatically include it if it matches the configured query.

The administrator should not have to edit the sidebar.

---

# 31. DATABASE-DRIVEN CARDS

Cards should also be generated from database records.

Example:

Agency Profiles

The CMS can query:

Entity Type = Agency

and display matching agencies using the selected card template.

If another agency is added, it automatically becomes eligible for the list.

---

# 32. PROFILE LISTS

The CMS should support multiple ways of displaying profile collections.

Examples:

- Cards
- Compact rows
- Thumbnail lists
- Alphabetical lists
- Search results
- Tables
- Featured profiles

The template determines the presentation.

The database determines the records.

---

# 33. PERSONNEL LISTS

Personnel lists may become too large for conventional cards.

The CMS should support a compact personnel directory.

Possible display:

[Photo] Pam Deig
Executive Director
Housing Authority
White County

[Photo] Person Name
Position
Organization
County

The administrator should be able to choose the presentation template.

---

# 34. PERSONNEL SEARCH

Personnel should be independently searchable.

A user should be able to search for:

Pam Deig

and reach the canonical personnel profile.

The search result may show:

- Name
- Photograph
- Current position
- Organization
- Jurisdiction

The user should then be able to explore all relationships from the profile.

---

# 35. PERSONNEL PROFILE

A personnel profile should be capable of displaying:

- Name
- Photograph
- Current positions
- Former positions
- Organizations
- Government entities
- Counties
- Cities
- Villages
- Civic organizations
- Related personnel
- Related articles
- Sources
- Documents

Only information that exists should be displayed.

---

# 36. PROFILE CONTEXT

A profile may be reached from multiple paths.

Example:

Agency Profiles
→ State
→ Illinois Department
→ Personnel
→ Pam Deig

or:

Personnel
→ Pam Deig

or:

White County
→ Personnel
→ Pam Deig

All paths should reach the same canonical personnel entity.

---

# 37. CONTEXTUAL BREADCRUMBS

The breadcrumb may reflect the user's navigation context.

Example:

Agency Profiles
→ State
→ Illinois
→ Agency
→ Personnel
→ Pam Deig

Another user might arrive through:

Personnel
→ Pam Deig

The person remains the same database entity.

The breadcrumb is navigation context, not identity.

---

# 38. RELATED INFORMATION

Profile templates should be able to query relationships.

For Pam Deig, a template might request:

All current positions

All organizations

All jurisdictions

All related personnel

All related articles

All sources

The database returns the appropriate records.

---

# 39. PROFILE CONNECTIONS SIDEBAR

Personnel profiles may use a right sidebar for connections.

Example:

CONNECTIONS

Organizations
Housing Authority

Jurisdictions
White County
Carmi

Positions
Executive Director

Related Personnel
Person A
Person B

Related Articles
Article A
Article B

This sidebar is database-driven.

---

# 40. PROFILE PAGE LAYOUT

Profile pages should support:

- No sidebar
- Left sidebar
- Right sidebar
- Both sidebars

The administrator selects the layout through the CMS.

The profile template determines the available components.

---

# 41. TEMPLATE VS DATA

The system must maintain a strict separation:

DATA
= What the system knows.

TEMPLATE
= How the information looks.

LAYOUT
= Where the information appears.

NAVIGATION
= How the user moves through it.

SIDEBAR
= Contextual navigation or information.

This separation is essential.

---

# 42. NO HARD-CODED ENTITY LISTS

The system must avoid hard-coded lists wherever the information is database-driven.

Do not manually code:

White County
Edgar County
Carmi
Example Village

Instead query the database.

---

# 43. NO DUPLICATED PERSON PROFILES

The system should prevent the creation of multiple profiles for the same person simply because they appear in different jurisdictions or organizations.

One person can have many relationships.

---

# 44. NO DUPLICATED AGENCY PROFILES

Likewise, an agency should have one canonical profile.

Its relationships can connect it to:

- State
- County
- City
- Village
- Personnel
- Civic organizations
- Federal entities

---

# 45. GRAPH-LIKE INFORMATION MODEL

The underlying information model should behave like a connected graph.

Entities are nodes.

Relationships are connections.

Examples:

PERSON
↓
holds_position
↓
AGENCY
↓
located_in
↓
COUNTY
↓
contains
↓
CITY

Another connection may be:

PERSON
↓
associated_with
↓
CIVIC ORGANIZATION

The public website presents this graph through understandable pages and navigation.

---

# 46. NAVIGATION DOES NOT DEFINE THE DATABASE

The public website may present information hierarchically.

The database should not be forced into the same hierarchy.

This is critical.

A person can belong to multiple contexts.

An agency can serve multiple jurisdictions.

A civic organization can connect to multiple government entities.

The database must support these relationships without duplicating entities.

---

# 47. PUBLIC NAVIGATION IS A VIEW

The sidebar and breadcrumb are views of the underlying information structure.

They are not the underlying structure itself.

This allows the same database to support multiple navigation paths.

---

# 48. RECORD ROOM / PROFILE DISCOVERY

The public profile discovery system should allow users to begin with a broad category and progressively narrow the results.

For example:

Agency Profiles
→ State
→ Illinois
→ State Agencies
→ Agency
→ Personnel

Or:

Agency Profiles
→ County
→ White County
→ County Agencies
→ Personnel

Or:

Personnel
→ Search
→ Person
→ Connections

---

# 49. CROSSOVER IS EXPECTED

Crossover between jurisdictions and entity types is not a problem to eliminate.

It is a core purpose of the system.

A person may connect:

Federal
State
County
City
Village
Civic

The database must represent those connections naturally.

---

# 50. SEARCH SHOULD EXPLOIT RELATIONSHIPS

Search should eventually allow users to discover connections.

Example:

Search:
Pam Deig

Result:

Pam Deig
Executive Director
Housing Authority
White County

Connections:

White County
Carmi
Housing Authority
Related organizations
Related personnel

---

# 51. FILTERING

Users should eventually be able to filter profiles by:

- Entity type
- Government level
- County
- City
- Village
- Civic
- Organization
- Position
- Date
- Topic
- Source

Filters should query the database.

---

# 52. PROFILE URLS

Every canonical profile should have a stable public URL.

The URL should identify the entity without making the entity permanently dependent upon a navigation path.

For example, a person should not require separate URLs merely because the person is reachable through different jurisdictions.

---

# 53. CANONICAL ENTITY

The CMS should identify one canonical record for each entity.

All references should point back to that canonical record.

This allows:

- Central updates
- Consistent information
- Relationship discovery
- Duplicate prevention
- Search
- Cross-referencing

---

# 54. DATABASE CHANGES PROPAGATE

When an administrator updates a profile, the change should become available anywhere that profile is dynamically displayed.

For example:

Update:

Pam Deig
Position

The updated position should appear in:

- Her profile
- Personnel search
- Agency personnel list
- County personnel list
- Related article components
- Sidebars

where those components use live database information.

---

# 55. PROFILE TEMPLATE COMPONENTS

Profile templates should be able to contain components such as:

- Profile Header
- Photograph
- Description
- Metadata
- Positions
- Organizations
- Jurisdictions
- Personnel
- Agencies
- Civic Connections
- Related Profiles
- Related Articles
- Sources
- Documents
- Timeline
- Map
- Sidebar
- Breadcrumb

The administrator should be able to configure which components appear.

---

# 56. FUTURE EXPANSION

The architecture should be prepared for additional entities such as:

- Boards
- Commissions
- Committees
- Elected offices
- Contractors
- Vendors
- Programs
- Grants
- Campaigns
- Meetings
- Documents
- Investigations
- Cases
- Projects

These should be additions to the data model, not reasons to rebuild the CMS.

---

# 57. CORE RULE

DO NOT BUILD THE PROFILE SYSTEM AS A COLLECTION OF STATIC PAGES.

BUILD THE PROFILE SYSTEM AS A DATABASE OF ENTITIES AND RELATIONSHIPS.

THE PUBLIC PAGES ARE GENERATED VIEWS OF THAT DATABASE.

---

# 58. FINAL MODEL

ENTITY
↓
DATABASE RECORD
↓
RELATIONSHIPS
↓
QUERY
↓
TEMPLATE
↓
PAGE
↓
SIDEBAR / RELATED INFORMATION
↓
USER NAVIGATION

This architecture allows API Group to grow from a small collection of Illinois records into a large investigative information system without requiring the administrator to manually rebuild the website every time new information is added.