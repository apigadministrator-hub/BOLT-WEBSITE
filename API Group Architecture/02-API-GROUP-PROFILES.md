# 02 — API GROUP PROFILES

## PURPOSE

This document defines how API Group Profiles work.

Profiles are the structured, database-driven representation of people, agencies, jurisdictions, civic organizations, contributors, partners, and other entities that API Group researches and connects.

Profiles are NOT manually written pages.

A profile is a database record rendered through a reusable template.

The database is the source of truth.

---

# 1. WHAT A PROFILE IS

A Profile represents a real-world entity that API Group wants to identify, document, research, monitor, or connect to other entities.

A Profile may represent:

- A person
- An agency
- A government organization
- A county
- A city
- A village
- A civic organization
- A contributor
- A partner
- Another organization
- Another entity type created by the administrator

The profile page is simply the presentation of the underlying database record.

---

# 2. PROFILES ARE NOT ARTICLES

This distinction is critical.

A Profile is structured data.

An Article is published content.

For example:

PERSONNEL PROFILE

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

This information belongs in structured database fields and relationships.

An article may discuss Pam Deig, but the article is not the profile.

Likewise, the profile should not need to be rewritten every time an article is published.

---

# 3. PROFILE TYPES

The initial API Group Profile system should support:

- Agency Profiles
- Personnel Profiles
- Civic Profiles
- Contributor Profiles
- Partner Profiles
- Jurisdiction Profiles

The system must be extensible.

The administrator must be able to create additional profile/entity types without requiring a developer to manually create a new page type.

Possible future types include:

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
- Other public-interest entity

---

# 4. AGENCY PROFILES

Agency Profiles represent governmental, public, civic, or other organizations that API Group is tracking.

Initial Agency Profile classifications are:

- Federal
- State
- County
- City
- Village
- Civic

These classifications are database-driven.

They are not permanently hard-coded.

The administrator must be able to create additional classifications when necessary.

---

# 5. FEDERAL AGENCY PROFILES

Federal profiles represent federal entities that have relevance to Illinois.

A federal agency may be included because it:

- Operates in Illinois
- Provides services in Illinois
- Regulates Illinois activity
- Funds Illinois programs
- Provides federal grants
- Oversees Illinois programs
- Investigates matters involving Illinois
- Maintains records relevant to Illinois
- Has another documented relationship to Illinois

Federal does not mean the entity must physically exist inside Illinois.

The determining factor is relevance to Illinois.

---

# 6. STATE AGENCY PROFILES

State profiles represent Illinois state-level entities.

Examples may include:

- State agencies
- Offices
- Departments
- Authorities
- Boards
- Commissions
- State constitutional offices
- Other state governmental entities

The system should allow state agencies to contain or reference subordinate offices, programs, divisions, and related entities.

Example:

Illinois
→ Attorney General
→ FOIA
→ OMA
→ Opinions
→ Enforcement
→ Other related records

These relationships should be stored in the database.

---

# 7. COUNTY AGENCY PROFILES

County-level profiles represent entities associated with an Illinois county.

Examples:

- County government
- County departments
- County offices
- County authorities
- County boards
- County commissions
- County agencies

A county agency should be connected to its county through a structured relationship.

Example:

Housing Authority
→ jurisdiction
→ White County

The agency should not merely contain "White County" as a text field and rely on that text for navigation.

---

# 8. CITY AGENCY PROFILES

City-level profiles represent agencies, offices, departments, boards, commissions, authorities, and other organizations associated with a city.

Example:

Carmi
→ City Government
→ City Departments
→ City Offices
→ Related Agencies
→ Related Personnel

The city itself is a database entity.

The agencies associated with it are separate database entities.

Relationships connect them.

---

# 9. VILLAGE AGENCY PROFILES

Village-level profiles follow the same database-driven model as city profiles.

A village is an entity.

Its agencies, departments, officials, personnel, records, and related organizations are separate entities connected through relationships.

The number of villages is not fixed.

The system displays however many village records exist in the database.

---

# 10. CIVIC PROFILES

Civic Profiles represent civic and community organizations.

Civic organizations may operate across:

- Counties
- Cities
- Villages
- Multiple jurisdictions
- Statewide areas
- Other geographic areas

A Civic Profile must therefore not be forced into one government hierarchy.

Example:

Civic Organization
→ operates_in
→ White County

Civic Organization
→ operates_in
→ Carmi

Civic Organization
→ related_to
→ Housing Authority

Civic Organization
→ related_to
→ Personnel

Civic relationships are stored independently.

---

# 11. PERSONNEL PROFILES

Personnel Profiles represent individual people.

A person is an independent database entity.

A person is NOT owned by an agency.

A person is NOT owned by a county.

A person is NOT owned by a city.

A person is NOT owned by a village.

A person is NOT owned by a federal entity.

A person may have relationships with any or all of these.

---

# 12. PERSONNEL MULTIPLE RELATIONSHIPS

One person may have:

- Multiple jobs
- Multiple positions
- Multiple agencies
- Multiple organizations
- Multiple jurisdictions
- Multiple civic relationships
- Multiple historical positions
- Multiple articles
- Multiple records

The database must support all of these relationships.

Example:

PERSON
Pam Deig

RELATIONSHIPS

Position:
Executive Director

Organization:
Housing Authority

Jurisdiction:
White County

Additional Position:
City of Carmi

City:
Carmi

Related Records:
Multiple

Related Articles:
Multiple

The person remains one database record.

---

# 13. PERSONNEL PROFILE STRUCTURE

A Personnel Profile may contain:

## Identity

- Full name
- Display name
- Photograph
- Pronunciation
- Alternate names
- Public identifiers

## Current Information

- Current position
- Current organization
- Current jurisdiction
- Current status

## Historical Information

- Previous positions
- Previous organizations
- Previous jurisdictions
- Relevant dates

## Relationships

- Agencies
- Organizations
- Counties
- Cities
- Villages
- Civic organizations
- Contributors
- Partners
- Other personnel

## Research Information

- Records
- Documents
- Articles
- Sources
- References
- Notes
- Tags

Not every field will apply to every person.

The template should display available information rather than requiring every field to contain data.

---

# 14. POSITION AS A SEPARATE CONCEPT

A person's position should be capable of being represented as structured information.

Example:

PERSON:
Pam Deig

POSITION:
Executive Director

ORGANIZATION:
Housing Authority

JURISDICTION:
White County

DATES:
Start / End when known

This allows the system to distinguish between:

- The person
- The position
- The organization
- The jurisdiction

This becomes especially important when one person holds multiple positions.

---

# 15. PERSONNEL DISCOVERY

Personnel should be discoverable independently.

A user should be able to start with:

Profiles
→ Personnel

and search or browse people without first choosing:

- Federal
- State
- County
- City
- Village
- Civic

This is important because personnel cross organizational and geographic boundaries.

A user looking for a person should not be forced to know which agency or jurisdiction the person belongs to before searching.

---

# 16. AGENCY DISCOVERY

Users should also be able to begin with:

Profiles
→ Agency Profiles

The Agency Profile system can then provide:

- Federal
- State
- County
- City
- Village
- Civic

These categories should be dynamically generated from the available database structure.

---

# 17. JURISDICTION PROFILES

Jurisdictions are themselves database entities.

Initial geographic focus:

ILLINOIS

The initial geographic hierarchy may include:

Illinois
→ Counties
→ Cities
→ Villages

Additional jurisdiction types may be added later.

A jurisdiction may contain or relate to:

- Agencies
- Personnel
- Civic organizations
- Records
- Documents
- Articles
- Programs
- Funding
- Other entities

---

# 18. ILLINOIS AS THE PRIMARY GEOGRAPHIC FOCUS

The initial API Group research scope is Illinois.

The system should be designed around Illinois without permanently preventing additional geographic areas later.

Federal information is included when it has an Illinois relationship or relevance.

The system should therefore support:

Federal
→ Illinois-related federal entities

State
→ Illinois

County
→ Illinois counties

City
→ Illinois cities

Village
→ Illinois villages

Civic
→ Illinois-related civic entities

---

# 19. PROFILE RELATIONSHIPS

Profiles should be connected through explicit relationships.

Examples:

PERSON
→ works_for
→ AGENCY

PERSON
→ holds_position
→ POSITION

AGENCY
→ located_in
→ COUNTY

COUNTY
→ part_of
→ ILLINOIS

AGENCY
→ serves
→ CITY

CIVIC ORGANIZATION
→ operates_in
→ COUNTY

PERSON
→ associated_with
→ CIVIC ORGANIZATION

PARTNER
→ associated_with
→ API GROUP

These relationships allow the same information to be discovered through different paths.

---

# 20. PROFILE CROSS-NAVIGATION

Every applicable profile should expose relevant relationships.

Example:

AGENCY PROFILE

Housing Authority

Related:

- White County
- Personnel
- City of Carmi
- Civic Organizations
- Records
- Documents
- Articles
- Sources

Example:

PERSONNEL PROFILE

Pam Deig

Related:

- Housing Authority
- White County
- Carmi
- Positions
- Organizations
- Records
- Articles
- Sources

Example:

COUNTY PROFILE

White County

Related:

- County Government
- Agencies
- Personnel
- Cities
- Villages
- Civic Organizations
- Records
- Articles

The exact information shown depends on the relationships stored in the database.

---

# 21. PROFILE TEMPLATE SYSTEM

Profiles must be rendered through reusable templates.

The administrator should not need to create HTML or code to build each profile.

A template may define:

- Header
- Profile image
- Name
- Classification
- Description
- Key facts
- Relationships
- Records
- Documents
- Articles
- Sources
- Related entities
- Sidebar content
- Footer

The same template can render hundreds or thousands of records.

---

# 22. DIFFERENT PROFILE TEMPLATES

Different profile types may require different layouts.

For example:

AGENCY PROFILE

May emphasize:

- Agency information
- Jurisdiction
- Authority
- Departments
- Personnel
- Records
- Documents

PERSONNEL PROFILE

May emphasize:

- Photograph
- Name
- Current positions
- Organizations
- Jurisdictions
- Connections
- Articles
- Records

CIVIC PROFILE

May emphasize:

- Organization
- Mission
- Jurisdictions
- Personnel
- Agencies
- Partners
- Articles
- Records

The administrator must be able to choose or assign templates without coding.

---

# 23. PROFILE SIDEBARS

Profile pages may use:

- No sidebar
- Left sidebar
- Right sidebar
- Both sidebars

The administrator determines the appropriate layout.

A common Personnel Profile layout may be:

LEFT SIDEBAR
→ Navigation

MAIN CONTENT
→ Personnel Profile

RIGHT SIDEBAR
→ Connections / Related Information

The right sidebar is especially useful for relationship-driven information.

---

# 24. DYNAMIC PROFILE SIDEBARS

Profile sidebars must be capable of displaying database-driven information.

Examples:

RELATED AGENCIES

Housing Authority
Other Agency

RELATED JURISDICTIONS

White County
Carmi

RELATED PERSONNEL

Person A
Person B
Person C

RELATED RECORDS

Record A
Record B

These are database queries.

They are not manually typed into the profile template.

---

# 25. PROFILE SEARCH

Users should be able to search profiles.

Search should support:

- Name
- Agency
- Jurisdiction
- Organization
- Position
- Profile type
- Tags
- Related entities
- Other searchable fields

Personnel search should not require the user to know the person's jurisdiction beforehand.

---

# 26. PROFILE LISTS

Profile directories should be generated from database queries.

Examples:

All Federal Agencies
All Illinois State Agencies
All White County Agencies
All Carmi Agencies
All Village Agencies
All Civic Organizations
All Personnel

The system displays however many records exist.

There is no predetermined number.

---

# 27. PROFILE CARDS

Profile cards are presentation components.

Agency cards may show:

- Logo
- Agency name
- Type
- Jurisdiction
- Short description

Personnel cards may show:

- Photograph
- Name
- Position
- Organization

Civic cards may show:

- Logo/photo
- Organization name
- Area
- Short description

The card design should be reusable.

The card content should come from the database.

---

# 28. PROFILE LIST VS. CARD VIEW

Not every profile type should be forced into a large card.

The CMS/template system should support multiple display modes.

Possible modes:

- Large cards
- Compact cards
- List
- Directory
- Table
- Search results
- Profile detail

Personnel directories may use a compact list because potentially large numbers of people must be displayed efficiently.

The administrator should be able to choose the appropriate display mode.

---

# 29. PROFILE IMAGES

Profiles may include images when available.

Possible images include:

- Agency logos
- Personnel photographs
- Organization logos
- Civic organization images
- Other identifying imagery

Images should be stored as media records and associated with database entities.

A missing image must not prevent the profile from being created.

The template should provide an appropriate fallback presentation.

---

# 30. PROFILE DATA COMPLETENESS

Profiles may be incomplete.

A profile should be able to exist with partial information.

For example:

Agency:
Example Agency

Known:
Name
Jurisdiction

Unknown:
Website
Phone
Personnel
Description

The profile should still be valid.

As additional information is discovered, the database record can be updated.

The page automatically reflects the new information.

---

# 31. PROFILE VERSIONING AND HISTORY

Where appropriate, the CMS should preserve changes to important profile information.

This is especially useful for:

- Personnel positions
- Agency leadership
- Jurisdiction relationships
- Organizational changes
- Historical information

The system should support current and historical relationships where practical.

A person's previous position should not necessarily be deleted simply because the person has moved to a new position.

---

# 32. PROFILE SOURCES

Important profile information should be capable of being associated with sources.

Example:

Personnel:
Pam Deig

Position:
Executive Director

Source:
Official agency document

Date:
YYYY-MM-DD

Source links and documents should be retained when available.

The source is part of the research record.

---

# 33. PROFILE RELATIONSHIP HISTORY

Relationships may change over time.

Examples:

Person
→ worked_for
→ Agency A
→ 2020–2023

Person
→ works_for
→ Agency B
→ 2023–present

The system should be capable of preserving this history.

Historical information should remain available where appropriate.

---

# 34. PROFILE DATA VS. PRESENTATION

The database record must remain independent of the visual design.

Changing a profile template must not change the underlying profile data.

Changing the sidebar must not change the underlying profile data.

Changing the card design must not change the underlying profile data.

Changing the website theme must not change the underlying profile data.

This separation allows the administrator to redesign the website without rebuilding the database.

---

# 35. AI-CREATED PROFILES

Authorized AI must be able to create profile records through the CMS or approved data interfaces.

AI should provide structured information.

Example:

PROFILE TYPE:
Personnel

NAME:
Example Person

POSITION:
Example Position

ORGANIZATION:
Example Agency

JURISDICTION:
White County

RELATED CITY:
Carmi

SOURCE:
Example Source

The system should create the structured record and relationships.

AI should not manually construct a webpage.

---

# 36. AI UPDATES

AI should also be able to update existing profiles.

If an existing person changes positions, the system should update the person's relationship and preserve relevant history.

If an agency changes its name, the database record should be updated.

If a new relationship is discovered, AI should be able to add the relationship.

The CMS should allow human review and approval of AI-created or AI-updated information.

---

# 37. DUPLICATE DETECTION

The system should attempt to prevent duplicate entities.

Before creating a new profile, the system should check for possible existing matches.

Examples:

- Same person
- Same agency
- Same county
- Same city
- Same village
- Same civic organization

If a likely duplicate exists, the administrator should be able to review and merge or reject the new record.

---

# 38. PROFILE MERGING

Where duplicate records are discovered, the CMS should eventually support merging.

Example:

PERSON A
Pam Deig

PERSON B
Pamela Deig

If both represent the same person, the administrator should be able to merge the records while preserving:

- Relationships
- Sources
- Records
- Articles
- Historical information
- Notes
- Media

The result should be one authoritative database entity.

---

# 39. PROFILE URLS

Each profile should have a stable public URL.

The URL should identify the profile without depending on its current navigation path.

This is important because the same profile may be discovered through many paths.

For example, a person should have one canonical profile URL even if users reach that person through:

- Personnel
- Agency
- County
- City
- Civic
- Search
- Article
- Related record

The navigation path may change.

The profile's identity should not.

---

# 40. BREADCRUMBS ON PROFILE PAGES

Profile pages should display breadcrumbs showing how the user arrived at the current context.

Example:

API Group
→ Profiles
→ Agency Profiles
→ County
→ White County
→ Housing Authority

or:

API Group
→ Profiles
→ Personnel
→ Pam Deig

The profile itself remains the same database record.

The breadcrumb represents the user's current navigation context.

---

# 41. PROFILE NAVIGATION IS NOT THE DATABASE

The website hierarchy is a way to discover profiles.

It is not the underlying database structure.

A person may be discovered through:

Agency
→ County
→ City
→ Civic

without being permanently nested underneath those entities.

The database stores the relationships independently.

The website uses those relationships to create useful navigation.

---

# 42. EXAMPLE: CROSS-JURISDICTIONAL PERSON

Consider:

Pam Deig

She may be:

Executive Director
→ Housing Authority
→ White County

and also hold a position or relationship with:

City of Carmi

The system should represent:

Pam Deig
├── Position → Executive Director
├── Organization → Housing Authority
├── Jurisdiction → White County
├── Position/Relationship → City of Carmi
└── Related Records / Articles / Sources

The user should be able to reach Pam's profile from either organizational or geographic context.

There should still be only one Pam Deig profile.

---

# 43. PROFILE ADMINISTRATION

The administrator must be able to manage profiles without coding.

The administrator should be able to:

- Create profiles
- Edit profiles
- Delete/archive profiles
- Add profile types
- Add fields
- Edit fields
- Add relationships
- Remove relationships
- Add images
- Add sources
- Add records
- Add notes
- Assign tags
- Assign templates
- Configure profile layouts
- Configure sidebars
- Preview profiles
- Publish profiles

---

# 44. DYNAMIC CATEGORY CREATION

When an administrator creates a new applicable profile category, the system should be capable of automatically making it available in:

- Profile landing pages
- Navigation
- Sidebars
- Search filters
- Cards
- Directories
- Templates

The administrator should not need to manually create a new frontend page for the category.

---

# 45. DYNAMIC ENTITY CREATION

When an administrator adds a new entity:

Example:

County:
New County

The system should automatically make the new county available to applicable:

- County lists
- Cards
- Sidebars
- Search
- Breadcrumbs
- Related records
- Agency navigation
- Personnel relationships

The frontend should query the database.

---

# 46. API GROUP PROFILE PRINCIPLE

Profiles are not static pages.

Profiles are database entities rendered through templates.

A profile can be:

- Found through search
- Found through an agency
- Found through a county
- Found through a city
- Found through a village
- Found through a civic organization
- Referenced by an article
- Referenced by a record
- Referenced by another profile

The entity remains one authoritative database record.

---

# 47. FINAL ARCHITECTURAL RULE

THE PROFILE IS THE ENTITY.

THE DATABASE IS THE SOURCE OF TRUTH.

THE RELATIONSHIPS DEFINE CONNECTIONS.

THE TEMPLATE DEFINES PRESENTATION.

THE SIDEBAR PROVIDES CONTEXTUAL NAVIGATION.

THE BREADCRUMB PROVIDES NAVIGATION HISTORY.

SEARCH PROVIDES DIRECT DISCOVERY.

AI AND HUMAN ADMINISTRATORS MANAGE THE DATA.

The website should never require manually constructed profile pages for each person, agency, county, city, village, civic organization, contributor, partner, or other entity.

The system must be capable of growing from a small demonstration database to a very large information system without changing this fundamental architecture.