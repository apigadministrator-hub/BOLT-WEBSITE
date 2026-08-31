# 11 — API GROUP PROFILE AND DATABASE RECORD SYSTEM

## PURPOSE

This document defines how API Group profiles are structured, stored, connected, displayed, searched, and maintained.

Profiles are the core structured-information system of API Group.

Profiles are NOT hard-written articles.

Profiles are database records rendered through reusable templates.

The purpose of the Profile System is to allow API Group to document real-world entities and the relationships between them without making any individual entity dependent upon a particular article, county, agency, or jurisdiction.

---

# 1. PROFILE SYSTEM PRINCIPLE

Every profile represents an entity.

Examples:

- Person
- Agency
- Organization
- County
- City
- Village
- Civic Organization
- Federal entity
- State entity

The entity exists independently in the database.

Its relationships to other entities are stored separately.

---

# 2. PROFILES ARE DATABASE RECORDS

A profile should contain structured fields appropriate to its record type.

The public profile page is generated from the database.

The administrator should never have to manually create a separate webpage for every profile.

---

# 3. PROFILE TYPES

The initial API Group Profile System should support:

- Federal
- State
- County
- City
- Village
- Agency
- Civic
- Personnel

Additional profile types may be introduced later.

---

# 4. ILLINOIS-FIRST SCOPE

The initial Profile System is focused on Illinois.

Illinois is the primary geographic context.

Federal profiles may be included when they have a meaningful relationship to Illinois.

Examples:

- Federal agencies operating in Illinois
- Federal programs affecting Illinois
- Federal funding affecting Illinois
- Federal officials relevant to Illinois
- Federal oversight of Illinois agencies
- Federal investigations involving Illinois
- Federal regulations affecting Illinois

---

# 5. FEDERAL PROFILES

Federal profiles should not mean that API Group is attempting to document every federal entity in the United States.

Federal records should generally be included because of their relationship to Illinois or because API Group is specifically monitoring them.

---

# 6. STATE PROFILES

State profiles primarily concern Illinois state government.

Examples may include:

- State agencies
- State offices
- State departments
- State boards
- State commissions
- State officials
- State legislators
- State programs

---

# 7. COUNTY PROFILES

County profiles represent Illinois counties being tracked by API Group.

A county record should be independent of the agencies and personnel associated with that county.

---

# 8. CITY PROFILES

City profiles represent municipalities.

A city record should be independent of:

- City agencies
- City officials
- County records
- Civic organizations

Relationships connect these records.

---

# 9. VILLAGE PROFILES

Village profiles function similarly to city profiles.

A village is its own database entity.

It may be related to:

- A county
- Personnel
- Agencies
- Civic organizations
- Other municipalities
- State agencies
- Federal programs

---

# 10. CIVIC PROFILES

Civic profiles represent organizations and entities outside ordinary governmental agency structures.

Examples may include:

- Civic organizations
- Nonprofit organizations
- Community organizations
- Advocacy organizations
- Associations
- Foundations
- Other organizations relevant to API Group research

---

# 11. AGENCY PROFILES

Agency profiles represent governmental or institutional agencies.

An agency may have relationships to:

- Federal government
- State government
- County government
- City government
- Village government
- Civic organizations
- Personnel
- Documents
- Sources
- Programs

---

# 12. PERSONNEL PROFILES

Personnel profiles represent people.

A personnel record must exist independently from any single agency or jurisdiction.

A person may have:

- Multiple positions
- Multiple agencies
- Multiple organizations
- Multiple jurisdictions
- Multiple civic relationships
- Historical positions
- Current positions

---

# 13. PERSON AS THE CANONICAL ENTITY

The person is the primary database entity.

Employment and organizational relationships belong in related records.

Example:

PERSON

Pam Deig

may be connected to:

POSITION
Executive Director

ORGANIZATION
White County Housing Authority

and also:

POSITION
City position

ORGANIZATION
City of Carmi

The person does not need to be duplicated to represent these relationships.

---

# 14. PERSONNEL MUST NOT BE ORGANIZED AS CHILD PAGES

Personnel should not exist only as pages beneath:

- Federal
- State
- County
- City
- Village
- Civic

Instead, personnel should be independently searchable.

A person may be reached from any relevant organizational or jurisdictional context.

---

# 15. RELATIONSHIP MODEL

The Profile System should use relationships.

Conceptually:

PERSON
↕
POSITION
↕
ORGANIZATION
↕
JURISDICTION

A person may have multiple relationships.

---

# 16. EXAMPLE OF CROSSOVER

Example:

Pam Deig

Relationship 1:

Pam Deig
→ Executive Director
→ White County Housing Authority
→ White County
→ Illinois

Relationship 2:

Pam Deig
→ Position
→ City of Carmi
→ White County
→ Illinois

The database stores both relationships.

The personnel profile displays both.

---

# 17. NO DUPLICATION

The same person should not be entered multiple times simply because that person has multiple roles.

Likewise:

The same agency should not be duplicated simply because it operates in multiple jurisdictions.

The database should maintain one canonical record whenever the entity is the same.

---

# 18. UNIQUE RECORD IDENTIFIERS

Every profile should have a unique internal identifier.

The identifier should remain stable even if:

- The display name changes
- The profile URL changes
- The person changes positions
- The organization changes its name

---

# 19. PROFILE NAME

Every profile should have a primary display name.

Additional names may include:

- Legal name
- Former name
- Common name
- Abbreviation
- Acronym
- Alias

---

# 20. PROFILE STATUS

Profiles should support statuses such as:

- Draft
- Review
- Published
- Unpublished
- Archived

---

# 21. PROFILE VISIBILITY

An administrator should be able to determine whether a profile is publicly visible.

A database record may exist before its public profile is published.

---

# 22. PROFILE TEMPLATE

Each profile type should have a reusable template.

Examples:

Agency Profile Template

Personnel Profile Template

County Profile Template

City Profile Template

Village Profile Template

Civic Organization Profile Template

---

# 23. PROFILE PAGE GENERATION

When a profile is published, the website generates the public-facing profile page from:

- Profile data
- Relationships
- Template
- Layout settings
- Sidebar configuration

---

# 24. PROFILE INTRODUCTION

A profile page should provide a concise explanation of the entity.

The content should be generated from structured information where practical.

Long-form editorial material may be displayed separately.

---

# 25. PROFILE INFORMATION

Depending on the profile type, the page may display:

- Name
- Type
- Location
- Jurisdiction
- Address
- Website
- Contact information where appropriate
- Current positions
- Organizations
- Related agencies
- Related personnel
- Related civic organizations
- Sources
- Documents
- Articles
- Dates
- Status

---

# 26. PROFILE RELATIONSHIPS

Relationships are first-class database records.

Examples:

PERSON
works_for
AGENCY

AGENCY
located_in
COUNTY

COUNTY
contains
CITY

PERSON
holds_position
ORGANIZATION

ORGANIZATION
related_to
CIVIC ORGANIZATION

AGENCY
receives_funding_from
FEDERAL AGENCY

---

# 27. RELATIONSHIP ATTRIBUTES

A relationship may contain additional information.

Examples:

- Start date
- End date
- Position title
- Role
- Relationship type
- Source
- Confidence
- Notes
- Status

---

# 28. HISTORICAL RELATIONSHIPS

The database should preserve historical relationships.

Example:

Person A

Position:
Director

Organization:
Agency X

Start:
2018

End:
2022

Later:

Position:
Director

Organization:
Agency Y

Start:
2022

The historical relationship remains part of the record.

---

# 29. CURRENT RELATIONSHIPS

Current relationships should be distinguishable from historical relationships.

The system should not delete history merely because a person changes positions.

---

# 30. PROFILE CONNECTIONS

Profile pages should display relevant connections.

A personnel profile may show:

- Current positions
- Former positions
- Agencies
- Organizations
- Jurisdictions
- Civic relationships
- Related personnel

---

# 31. RIGHT SIDEBAR FOR PROFILE CONNECTIONS

Personnel profiles may use a right sidebar for contextual connections.

Example:

RELATED CONNECTIONS

White County Housing Authority

City of Carmi

White County

Related Personnel

Related Civic Organizations

Sources

---

# 32. LEFT SIDEBAR FOR PROFILE NAVIGATION

The left sidebar may be used for hierarchical navigation.

Example:

AGENCY PROFILES

Federal

State

County

City

Village

Civic

Personnel

The administrator controls whether the sidebar is enabled.

---

# 33. PROFILE DIRECTORY

Each profile type should have a directory.

Examples:

Illinois Counties

Illinois Cities

Illinois Villages

State Agencies

County Agencies

Personnel

Civic Organizations

---

# 34. DIRECTORY GENERATION

Directories must be generated from database records.

There must not be a fixed list of entities hard-coded into the website.

---

# 35. AUTOMATIC DIRECTORY UPDATE

When a new record is published:

The appropriate directory automatically includes it.

Example:

New county added:

Crawford County

The county directory automatically displays:

Crawford County

No developer intervention is required.

---

# 36. PROFILE SEARCH

Users should be able to search profiles.

Search may include:

- Name
- Organization
- Agency
- County
- City
- Village
- Civic organization
- Position
- Profile type
- Keyword
- Relationship

---

# 37. PERSONNEL SEARCH

Personnel should have an independent search capability.

A user should be able to search:

Pam Deig

without first knowing:

- Her county
- Her agency
- Her city
- Her position

The results should identify the relationships associated with the person.

---

# 38. AGENCY SEARCH

A user should be able to search directly for an agency.

The result may identify:

- Agency name
- Agency type
- Jurisdiction
- Personnel
- Parent organization
- Related agencies
- Related articles

---

# 39. JURISDICTION SEARCH

Users should be able to search for jurisdictions.

Examples:

Illinois

White County

Carmi

A jurisdiction profile can then lead to associated agencies, personnel, organizations, and records.

---

# 40. HIERARCHICAL NAVIGATION

The public website may provide hierarchical navigation.

Example:

Agency Profiles

→ State

→ Illinois

→ State Agencies

→ Attorney General's Office

→ Related Personnel

However, the hierarchy is a navigation method.

It does not mean the underlying records are permanently dependent on that hierarchy.

---

# 41. CROSS-NAVIGATION

Users should be able to move between related records.

Example:

County
→ Agency
→ Personnel
→ City
→ Civic Organization
→ Related Article

The database relationships make this possible.

---

# 42. BREADCRUMBS

Breadcrumbs should show the user's current navigation path.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ Attorney General's Office

Breadcrumbs should be generated dynamically.

---

# 43. BREADCRUMBS ARE NOT DATABASE DEPENDENCIES

The breadcrumb represents the user's path.

It does not define the ownership of the underlying records.

A personnel profile may be reached through several different paths.

---

# 44. MULTIPLE PATHS TO THE SAME PROFILE

The same personnel profile may be reached through:

Personnel Search

or:

Agency
→ Personnel

or:

County
→ Agencies
→ Personnel

or:

City
→ Personnel

All paths should lead to the same canonical personnel record.

---

# 45. PROFILE URLS

Every published profile should have a stable canonical URL.

The URL should identify the record without requiring the entire organizational hierarchy to be embedded in the URL.

---

# 46. DATABASE-DRIVEN PROFILE LINKS

Links to profiles should be generated from record identifiers.

If a profile's display name changes, references should continue pointing to the same record.

---

# 47. PROFILE CARDS

Profiles may be displayed as cards when appropriate.

Card examples:

- County
- City
- Village
- Agency
- Civic organization

---

# 48. PERSONNEL DISPLAY

Large personnel collections should generally use compact directory layouts rather than large article-style cards.

A personnel entry may include:

- Thumbnail
- Name
- Current position
- Organization
- Jurisdiction

---

# 49. PROFILE PHOTOGRAPHS

Personnel profiles may include a photograph or thumbnail.

The system should support profiles without photographs.

A missing photograph must not prevent publication.

---

# 50. PROFILE SOURCES

Profiles should support source references.

Sources may include:

- Government websites
- Public records
- Official documents
- Meeting minutes
- Filings
- News reports
- Contributor information
- Research documents

---

# 51. SOURCE-BASED PROFILE CREATION

AI may extract information from source material and propose a profile.

Example:

Source document identifies:

Name:
Pam Deig

Position:
Executive Director

Organization:
White County Housing Authority

AI proposes the corresponding structured records and relationships.

---

# 52. AI PROFILE CREATION

AI should be capable of proposing:

- New profile records
- New relationships
- Updated positions
- New organizations
- New jurisdictions
- Source references

The AI should not bypass editorial review where review is required.

---

# 53. AI MUST USE STRUCTURED DATA

AI should create structured database records.

It should not generate a hard-coded profile webpage.

Correct:

AI
→ Creates Person Record
→ Creates Position Record
→ Creates Organization Relationship
→ Adds Source
→ Profile Template Displays Information

Incorrect:

AI
→ Writes a static HTML page

---

# 54. DUPLICATE DETECTION

Before creating a new profile, the system should attempt to identify possible existing records.

Examples:

Two entries for:

Pam Deig

should trigger a possible duplicate warning.

Two agency records with similar names should also be reviewed.

---

# 55. MERGING RECORDS

Administrators should be able to merge duplicate records.

The system should preserve:

- Relationships
- Sources
- Articles
- Historical data
- Identifiers

where possible.

---

# 56. RECORD CORRECTIONS

An administrator should be able to correct profile information without rewriting the profile page.

The database record is updated.

The profile template automatically reflects the correction.

---

# 57. PROFILE EDITING

The administrator should be able to edit:

- Name
- Description
- Type
- Location
- Contact information
- Relationships
- Positions
- Dates
- Sources
- Media
- Status

depending on the profile type.

---

# 58. PROFILE FIELD CONFIGURATION

Profile types should support configurable fields.

For example:

Personnel:

- Name
- Photograph
- Position
- Organization
- Start date
- End date
- Biography
- Sources

Agency:

- Name
- Agency type
- Jurisdiction
- Address
- Website
- Parent organization
- Personnel
- Sources

---

# 59. CUSTOM FIELDS

The CMS should eventually permit administrators to create additional structured fields where necessary.

Custom fields should remain structured database fields rather than arbitrary HTML.

---

# 60. PROFILE HISTORY

Where appropriate, profiles should preserve historical information.

Examples:

- Former names
- Former positions
- Former agencies
- Organizational changes
- Jurisdictional changes

---

# 61. PROFILE TIMELINES

The system may eventually display important historical relationships as timelines.

Example:

2018
Position A

2021
Position B

2024
Position C

The underlying information remains database-driven.

---

# 62. PROFILE ARTICLES

A profile may have related editorial articles.

Example:

Personnel Profile:
Pam Deig

Related Articles:

"White County Housing Authority"

"Carmi Housing Issues"

The articles remain independent records.

---

# 63. PROFILE DOCUMENTS

A profile may have associated documents.

Examples:

- Meeting minutes
- Government reports
- Filings
- Public records
- Notices

Documents remain separate records that can be associated with multiple profiles.

---

# 64. PROFILE REFERENCES FROM ARTICLES

Articles may reference profiles.

Example:

Article:

"White County Housing Authority Announces New Program"

References:

White County Housing Authority

Pam Deig

White County

Carmi

---

# 65. PROFILE REFERENCES FROM MONSTER NEWS

Monster News may intentionally reference API Group profiles.

This does not make the profile part of Monster News.

The API Group profile remains the canonical API Group record.

---

# 66. PROFILE SYSTEM INDEPENDENCE

Profiles must not depend upon the existence of articles.

A profile can exist without an article.

An article can exist without a profile.

Relationships may connect them when relevant.

---

# 67. PROFILE PAGE LAYOUT

The administrator should be able to configure:

- Left sidebar
- Right sidebar
- Both
- Neither

depending on the profile type or individual page.

---

# 68. DEFAULT PROFILE LAYOUTS

Suggested defaults:

Agency:
Left sidebar

Jurisdiction:
Left sidebar

Personnel:
Right sidebar

Civic:
Left sidebar

The administrator may override these defaults.

---

# 69. PROFILE DIRECTORY LAYOUT

Directories should be optimized for large datasets.

The system must not assume that a directory will contain only a few records.

Potential tools include:

- Search
- Filtering
- Sorting
- Pagination
- Alphabetical navigation
- Jurisdiction filters
- Profile-type filters

---

# 70. SCALABILITY

The database architecture must support growth.

The system should remain usable when there are:

- Hundreds of profiles
- Thousands of profiles
- Tens of thousands of profiles

Large datasets must not require manually designed pages.

---

# 71. PROFILE DATA API

The application should expose structured profile data internally through appropriate services or APIs.

The frontend should request records rather than storing copies of profile information in static page files.

---

# 72. CACHE AND PERFORMANCE

Database-driven pages should be optimized for performance.

Caching may be used where appropriate.

Caching must not prevent newly published or updated information from becoming available within the expected publishing workflow.

---

# 73. PROFILE SECURITY

Administrative profile editing must be protected by permissions.

Public users should only see information marked for public display.

Sensitive or restricted information must not be exposed merely because it exists in the database.

---

# 74. PUBLIC RECORD PRINCIPLE

The system should distinguish between:

- Information collected
- Information verified
- Information published

A database record may contain research information that is not yet ready for public display.

---

# 75. SOURCE AND CONFIDENCE

Where appropriate, structured information should support source and confidence indicators.

Possible values:

- Confirmed
- Supported
- Reported
- Unverified
- Under Review

The exact terminology may be refined later.

---

# 76. PROFILE CONNECTION GRAPH

The long-term system should be capable of representing relationships as a network.

Example:

PERSON
↓
POSITION
↓
AGENCY
↓
COUNTY
↓
CITY
↓
CIVIC ORGANIZATION

The user should be able to follow these relationships through the website.

---

# 77. SEARCH AS AN ALTERNATIVE TO HIERARCHY

The hierarchy is a navigation tool.

Search is an alternative entry point.

A user who does not know where an entity belongs should be able to search for it directly.

---

# 78. HIERARCHY AND RELATIONSHIPS WORK TOGETHER

The system should provide both:

HIERARCHICAL NAVIGATION

and

RELATIONAL NAVIGATION

Hierarchy answers:

"Where am I?"

Relationships answer:

"Who or what is connected to this?"

---

# 79. PROFILE SYSTEM FINAL STRUCTURE

The conceptual structure is:

API GROUP

→ PROFILES

→ AGENCY PROFILES

→ Federal
→ State
→ County
→ City
→ Village
→ Civic
→ Personnel

These are navigation and classification structures.

The underlying database remains relational.

---

# 80. IMPORTANT DISTINCTION

PERSONNEL IS NOT A SUBORDINATE COPY OF AGENCY DATA.

AGENCIES ARE NOT SUBORDINATE COPIES OF COUNTY DATA.

COUNTIES ARE NOT SUBORDINATE COPIES OF CITIES.

CITIES ARE NOT SUBORDINATE COPIES OF CIVIC ORGANIZATIONS.

Each entity is independently stored.

Relationships connect them.

---

# 81. EXAMPLE

DATABASE:

Person:
Pam Deig

Position:
Executive Director

Organization:
White County Housing Authority

Jurisdiction:
White County

Municipality:
Carmi

Additional Position:
City of Carmi

The database stores these as connected records.

The public website may display them as:

Pam Deig

Current Positions

White County Housing Authority
Executive Director

City of Carmi
[Position]

Connections

White County
Carmi
Housing Authority

Related Articles

Related Documents

Sources

---

# 82. ADMINISTRATOR EXPERIENCE

The administrator should be able to create a person without manually deciding where the person must live in the website hierarchy.

The administrator creates:

PERSON

Then assigns:

POSITIONS

ORGANIZATIONS

JURISDICTIONS

SOURCES

The website determines where that person can be reached through database queries and relationships.

---

# 83. ADDING A NEW ENTITY

Example:

Administrator adds:

Crawford County

The system automatically makes the record available to:

- County directory
- Search
- Relevant navigation
- Related profile queries
- Appropriate sidebars

---

# 84. ADDING A NEW PERSON

Example:

Administrator adds:

Jane Smith

Then adds:

Position:
Director

Organization:
Agency X

Jurisdiction:
White County

The personnel directory automatically includes Jane Smith.

Agency X's personnel list can automatically include Jane Smith.

White County's related personnel list can automatically include Jane Smith.

No separate page editing is required.

---

# 85. FINAL PRINCIPLE

THE PROFILE SYSTEM IS A DATABASE, NOT A COLLECTION OF HARD-WRITTEN ARTICLES.

EVERY ENTITY HAS ITS OWN RECORD.

PEOPLE HAVE THEIR OWN RECORDS.

AGENCIES HAVE THEIR OWN RECORDS.

COUNTIES HAVE THEIR OWN RECORDS.

CITIES HAVE THEIR OWN RECORDS.

VILLAGES HAVE THEIR OWN RECORDS.

CIVIC ORGANIZATIONS HAVE THEIR OWN RECORDS.

FEDERAL AND STATE ENTITIES HAVE THEIR OWN RECORDS.

RELATIONSHIPS CONNECT THE RECORDS.

THE USER MAY ENTER THE SYSTEM THROUGH ANY RELEVANT PATH.

SEARCH CAN FIND ANY PUBLISHED RECORD.

HIERARCHICAL SIDEBARS PROVIDE NAVIGATION.

RELATIONSHIPS PROVIDE CONTEXT.

BREADCRUMBS SHOW THE USER'S CURRENT PATH.

TEMPLATES TURN DATABASE RECORDS INTO PUBLIC PROFILE PAGES.

AI MAY CREATE OR PROPOSE STRUCTURED RECORDS.

ADMINISTRATORS MAY EDIT RECORDS WITHOUT CODING.

WHEN A NEW RECORD IS ADDED, DATABASE-DRIVEN DIRECTORIES, SEARCH RESULTS, SIDEBARS, AND RELATED CONTENT UPDATE AUTOMATICALLY.

THE DATABASE IS THE SOURCE OF TRUTH.

THE PROFILE PAGE IS A VIEW OF THAT DATA.