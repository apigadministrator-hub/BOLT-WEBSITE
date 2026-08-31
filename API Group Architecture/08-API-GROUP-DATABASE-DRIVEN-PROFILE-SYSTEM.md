# 08 — API GROUP DATABASE-DRIVEN PROFILE SYSTEM

## PURPOSE

This document defines the database-driven profile system for the API Group website.

Profiles are the core investigative information system of API Group.

Profiles must not be treated as ordinary hard-written articles.

A profile is a structured database record that is presented through a reusable public-facing template.

The website should generate profile pages from database information.

---

# 1. CORE PRINCIPLE

API Group profiles are DATABASE RECORDS.

They are not manually authored webpages.

The administrator, editor, contributor, or AI system should be able to create or update structured information in the database.

The public website then uses that information to generate the appropriate profile page.

---

# 2. PROFILE TYPES

The system should support multiple profile types.

Initial profile types include:

- Federal
- State
- County
- City
- Village
- Agency
- Personnel
- Civic Organization

Additional profile types may be added later without requiring a redesign of the entire system.

---

# 3. PROFILE TYPES MUST BE CONFIGURABLE

The administrator should be able to create additional profile types through the CMS.

Creating a new profile type should not require coding.

The administrator should be able to define:

- Name
- Description
- Fields
- Relationships
- Display template
- Search behavior
- Navigation behavior
- Sidebar behavior
- Visibility
- Publishing status

---

# 4. PROFILES AND HIERARCHY

The public navigation may organize profiles hierarchically.

However, the database must not make a profile permanently dependent on one location in the hierarchy.

For example:

Pam Deig may be associated with:

- White County
- Carmi
- Housing Authority
- Other organizations
- Multiple positions

The database must represent those relationships independently.

---

# 5. CANONICAL PROFILE IDENTITY

Every profile must have a unique database identity.

Example:

PERSON:
Pam Deig

The same person must not become a different person record simply because the user reaches her through:

- Personnel
- White County
- Carmi
- Housing Authority
- Search
- An article

All references should point to the same canonical profile.

---

# 6. PROFILE RELATIONSHIPS

Profiles should support relationships to other profiles.

Examples:

PERSON → WORKS FOR → AGENCY

PERSON → HOLDS POSITION → POSITION

PERSON → SERVES → COUNTY

PERSON → SERVES → CITY

PERSON → ASSOCIATED WITH → CIVIC ORGANIZATION

AGENCY → LOCATED IN → COUNTY

AGENCY → OPERATES IN → CITY

AGENCY → PART OF → STATE

AGENCY → RELATED TO → FEDERAL PROGRAM

The exact relationship vocabulary should be configurable.

---

# 7. MANY-TO-MANY RELATIONSHIPS

The database must support many-to-many relationships.

A person may have:

- Multiple positions
- Multiple employers
- Multiple organizations
- Multiple jurisdictions
- Multiple civic connections

An agency may have:

- Multiple locations
- Multiple jurisdictions
- Multiple personnel
- Multiple programs
- Multiple parent organizations

The system must not assume one profile can have only one relationship.

---

# 8. TEMPORAL RELATIONSHIPS

Relationships may change over time.

The database should therefore be capable of storing:

- Start date
- End date
- Current status
- Historical status
- Position history

Example:

PERSON
Pam Deig

POSITION:
Executive Director

ORGANIZATION:
Housing Authority

Start:
[date]

End:
[date or current]

A second position can then exist simultaneously or historically.

---

# 9. PROFILE DATA

A profile should contain structured fields appropriate to its type.

Common fields may include:

- Name
- Official name
- Type
- Description
- Status
- Location
- Jurisdiction
- Website
- Contact information
- Parent organization
- Related organizations
- Related personnel
- Sources
- Documents
- Tags
- Notes
- Dates
- Images
- Logo
- External identifiers

Not every profile type needs every field.

---

# 10. PROFILE FIELD DEFINITIONS

Fields should be configurable by the administrator.

Examples:

PERSONNEL

- Full name
- Preferred name
- Photograph
- Current position
- Previous positions
- Agency
- County
- City
- Village
- Civic connections
- Biography
- Sources
- Documents

AGENCY

- Official name
- Agency type
- Jurisdiction
- Address
- Website
- Parent organization
- Personnel
- Programs
- Records
- Sources

---

# 11. REQUIRED AND OPTIONAL FIELDS

Each profile type should allow fields to be designated:

- Required
- Optional
- Repeatable
- Searchable
- Public
- Internal

The CMS should enforce required fields before publishing where appropriate.

---

# 12. REPEATABLE FIELDS

Certain information must be repeatable.

Examples:

A person may have multiple:

- Positions
- Organizations
- Addresses
- Sources
- Documents
- Phone numbers
- Websites
- Jurisdictions

The CMS should provide an easy way to add another instance.

---

# 13. PROFILE IMAGES

Profiles should support images.

Personnel profiles may include:

- Headshot
- Official photograph
- Other verified photographs

Agency profiles may include:

- Agency logo
- Building photograph
- Official seal

Civic profiles may include:

- Organization logo
- Relevant photograph

Images should be stored as media records and referenced by profiles.

---

# 14. PROFILE MEDIA

Media should not be permanently embedded into a single article.

A media item should have its own identity where appropriate.

This allows the same image to be associated with multiple records.

---

# 15. SOURCES

Profiles should support source records.

Sources may include:

- Official websites
- Public records
- Government documents
- Meeting records
- News articles
- Public databases
- Contributor submissions
- Other verified sources

The system should preserve source information rather than treating profile text as unsupported facts.

---

# 16. PROVENANCE

Where practical, individual pieces of profile information should be traceable to their source.

Example:

Position:
Executive Director

Source:
Official agency document

Date verified:
[date]

This is particularly important for investigative research.

---

# 17. AI-GENERATED PROFILE DATA

AI should be able to assist in creating and updating profiles.

AI may:

- Create a new profile
- Add a person
- Add an agency
- Add a county
- Add a city
- Add a village
- Add a civic organization
- Add relationships
- Update fields
- Suggest relationships
- Extract information from documents
- Identify possible duplicate profiles

AI must operate against structured database records.

---

# 18. AI MUST NOT CREATE ISOLATED PAGES

When AI creates a new profile, it should create or update the corresponding database record.

It should not simply generate a standalone HTML page.

Example:

New county:
Edgar County

AI adds:

PROFILE TYPE:
County

NAME:
Edgar County

STATE:
Illinois

The public website then automatically recognizes the new profile.

---

# 19. AUTOMATIC DIRECTORY UPDATES

When a new database entity is created and published, relevant directories should update automatically.

Example:

Existing counties:

White County
Vermilion County
Vigo County

Administrator adds:

Edgar County

The County directory automatically becomes:

White County
Vermilion County
Vigo County
Edgar County

No manual sidebar editing should be required.

---

# 20. AUTOMATIC SIDEBAR UPDATES

Database-driven sidebar lists must update automatically.

If the sidebar displays counties, the list should be generated from the County database.

If another county is published, it automatically appears.

The same principle applies to:

- Agencies
- Personnel
- Cities
- Villages
- Civic organizations
- Other database entities

---

# 21. PROFILE SEARCH

All profiles should be searchable.

Search should be capable of locating a profile without requiring the user to navigate through the hierarchy.

Example:

Search:
Pam Deig

Result:
Pam Deig — Personnel Profile

Search:
Housing Authority

Result:
Housing Authority — Agency Profile

---

# 22. PROFILE FILTERING

Search and directory pages should support appropriate filters.

Examples:

PERSONNEL:

- County
- City
- Agency
- Position
- Civic connection

AGENCIES:

- Federal
- State
- County
- City
- Village
- Civic
- Jurisdiction

The available filters should be generated from the database where practical.

---

# 23. PROFILE TEMPLATES

Each profile type should have one or more reusable templates.

The administrator should be able to select the appropriate template.

Example:

Personnel Profile Template

- Name
- Photograph
- Current positions
- Organizations
- Jurisdictions
- Connections
- Sources
- Related articles

Agency Profile Template

- Name
- Logo
- Agency type
- Jurisdiction
- Description
- Personnel
- Related agencies
- Documents
- Sources

---

# 24. TEMPLATE FLEXIBILITY

Templates must not permanently determine the database structure.

The database stores the information.

The template determines how that information is displayed.

This separation is essential.

---

# 25. PROFILE PAGE LAYOUT

A profile page may contain:

LEFT SIDEBAR:
Navigation

MAIN CONTENT:
Profile

RIGHT SIDEBAR:
Connections and related information

The administrator should be able to configure whether each sidebar appears.

---

# 26. PERSONNEL PROFILE LAYOUT

Personnel profiles may use a more compact structure than agency profiles.

Possible layout:

PHOTO

NAME

CURRENT POSITION

ORGANIZATION

JURISDICTION

ABOUT

POSITIONS

ORGANIZATIONS

JURISDICTIONS

CONNECTIONS

SOURCES

RELATED ARTICLES

---

# 27. CONNECTIONS

Connections are a major feature of personnel profiles.

A personnel profile should be able to display connected entities.

Example:

Pam Deig

CONNECTED TO:

Housing Authority
White County
City of Carmi
Other organizations
Related personnel

Connections may appear in a right sidebar or within the main profile.

---

# 28. CONNECTIONS MUST BE DATABASE-DRIVEN

Connections must not be manually typed into each profile page.

If:

Pam Deig

is connected to:

Housing Authority

the website should retrieve that relationship from the database.

If another relationship is added, the profile should automatically display it according to the selected template.

---

# 29. PROFILE CARDS

Profiles may be represented as cards when appropriate.

Cards should be used for:

- Small directories
- Featured profiles
- Category landing pages
- Discovery pages

Cards may include:

- Image
- Name
- Type
- Location
- Short description
- Key relationship
- Link

---

# 30. LARGE DIRECTORIES

Cards should not be mandatory.

Large personnel directories may require a compact list.

Possible presentation:

PHOTO | NAME | POSITION | ORGANIZATION | LOCATION

The administrator should be able to select the presentation template.

---

# 31. PROFILE LISTS

A profile list should be generated from database queries.

Example:

Query:

Profile Type = Personnel
State = Illinois
Published = Yes

The page displays every matching personnel record.

There should be no hard-coded maximum.

---

# 32. PROFILE SORTING

Directories should support configurable sorting.

Possible options:

- Alphabetical
- Recently added
- Recently updated
- Most relevant
- Jurisdiction
- Organization
- Position

The administrator should be able to configure the default sort order.

---

# 33. PROFILE STATUS

Profiles should support publication states.

Examples:

- Draft
- Review
- Published
- Unpublished
- Archived

Only profiles marked Published should normally appear publicly.

---

# 34. PROFILE REVIEW

AI-generated or contributor-submitted information should be capable of entering a review state before publication.

This allows an editor to verify information before it becomes public.

---

# 35. DUPLICATE DETECTION

The system should attempt to detect possible duplicate profiles.

Example:

Pam Deig

Possible duplicate:

Pamela Deig

The CMS should warn the administrator rather than automatically creating two separate identities.

---

# 36. MERGING PROFILES

Authorized administrators should be able to merge duplicate profiles.

When profiles are merged:

- Relationships should be preserved
- Sources should be preserved
- Documents should be preserved
- References should be updated
- The canonical profile should remain intact

---

# 37. PROFILE HISTORY

The system should preserve a history of important changes.

Where practical, the administrator should be able to see:

- Who changed the record
- What changed
- When it changed
- Previous value
- New value

---

# 38. AI AND HUMAN EDITORS

AI and human editors should work on the same underlying database.

AI should not create a separate parallel information system.

Human editors should be able to inspect, correct, approve, or reject AI-generated information.

---

# 39. CONTRIBUTOR INFORMATION

Contributors and partners are important entities in the API Group ecosystem.

Examples include:

- Village Voice
- Edgar County Watchdogs
- Other contributors
- Research partners
- Community organizations
- Media organizations

These entities should be representable in the database.

They should not be treated as informal notes.

---

# 40. CONTRIBUTOR PROFILES

Contributor organizations may have profiles containing:

- Organization name
- Logo
- Website
- Description
- Contact information
- Areas of interest
- Related personnel
- Contributions
- Sources
- Articles

---

# 41. ARTICLE-TO-PROFILE CONNECTIONS

Library articles may reference profiles.

For example:

An article may reference:

White County
Pam Deig
Housing Authority
Carmi

Those references should link to their canonical database profiles.

---

# 42. PROFILE-TO-ARTICLE CONNECTIONS

Profiles may also display related articles.

Example:

Pam Deig

Related Articles:

Article A
Article B
Article C

These relationships should be generated automatically where possible.

---

# 43. PROFILE-TO-DOCUMENT CONNECTIONS

Profiles may also be connected to documents.

Examples:

Agency profile
→ Meeting minutes
→ FOIA documents
→ Annual reports
→ Contracts
→ Public records

Documents should remain independently stored and identifiable.

---

# 44. PROFILE TAXONOMY

Profile type and jurisdiction should be separate concepts.

For example:

PROFILE TYPE:
Agency

JURISDICTION:
State

Another:

PROFILE TYPE:
Agency

JURISDICTION:
County

Another:

PROFILE TYPE:
Personnel

JURISDICTION:
City

This prevents the database from becoming unnecessarily rigid.

---

# 45. JURISDICTIONS

The system should support jurisdiction records.

Initial jurisdiction hierarchy may include:

Federal
State
County
City
Village

Civic entities may intersect with these jurisdictions without necessarily being subordinate to them.

---

# 46. CIVIC ENTITIES

Civic organizations should not automatically be forced into the same government hierarchy.

They may connect to:

- People
- Agencies
- Counties
- Cities
- Villages
- State entities
- Federal programs
- Other civic organizations

Their relationships should be represented explicitly.

---

# 47. NO FIXED HIERARCHY LIMIT

The database must not assume that relationships can only be:

Category
→ Subcategory
→ Record

The system should support deeper structures and cross-connections.

---

# 48. NAVIGATION IS A VIEW OF THE DATABASE

The public sidebar is not the database.

The breadcrumb is not the database.

The category structure is not the database.

They are views into the database.

The same profile can therefore appear in multiple navigation contexts without duplication.

---

# 49. DATABASE FIRST

When designing new functionality, the development team should ask:

"What database relationship does this represent?"

before asking:

"What page should this become?"

The page is the presentation.

The database is the underlying system.

---

# 50. PUBLIC PAGE GENERATION

A public profile page should be generated approximately as:

PROFILE RECORD
+
PROFILE TEMPLATE
+
RELATIONSHIPS
+
MEDIA
+
SOURCES
+
NAVIGATION CONTEXT
=
PUBLIC PROFILE PAGE

---

# 51. NEW RECORD WORKFLOW

Example:

Administrator notices that a county is missing.

Administrator opens CMS.

Selects:

New Profile

Selects:

County

Enters:

Edgar County

Selects:

Illinois

Saves.

The system creates the database record.

After publication:

Edgar County automatically appears in relevant:

- County directories
- Sidebars
- Search results
- Breadcrumb destinations
- Related navigation

No developer intervention is required.

---

# 52. NEW PERSON WORKFLOW

Example:

Administrator enters:

Pam Deig

The CMS creates a Personnel profile.

Administrator adds:

Position:
Executive Director

Organization:
Housing Authority

Jurisdiction:
White County

City:
Carmi

The system creates the relationships.

The public profile then displays the appropriate information automatically.

---

# 53. MULTIPLE POSITIONS

A person may hold multiple positions.

Example:

Pam Deig

Position 1:
Executive Director
Housing Authority

Position 2:
City position
Carmi

The profile should display both relationships.

Neither position should overwrite the other.

---

# 54. CROSS-JURISDICTION PERSONNEL

Personnel may cross jurisdictions.

A person can simultaneously have relationships to:

County
City
Village
State
Federal
Civic

The database must support this naturally.

---

# 55. PROFILE API / DATA ACCESS

The system should be designed so that profile data can eventually be accessed by:

- Website templates
- Search
- AI
- Internal tools
- APIs
- Future applications

The database should therefore remain structured and normalized rather than storing everything as one large block of text.

---

# 56. ADMINISTRATOR EXPERIENCE

The administrator should not need coding knowledge.

The CMS should allow the administrator to:

- Create profiles
- Edit profiles
- Add fields
- Add relationships
- Upload images
- Attach documents
- Add sources
- Approve AI-generated information
- Publish profiles
- Unpublish profiles
- Configure templates
- Configure directories
- Configure sidebars

---

# 57. EDITOR EXPERIENCE

Editors should be able to update individual pieces of profile information without rebuilding the entire page.

Changing:

Position

should update the profile automatically.

Adding:

Agency

should update relevant connections automatically.

Adding:

County

should update relevant navigation automatically.

---

# 58. AI IMPORTANCE

The profile system must be designed from the beginning with AI-assisted data entry in mind.

AI should be able to transform source information into structured records.

Example:

Source document
↓
AI extraction
↓
Candidate profile data
↓
Human review
↓
Database
↓
Public profile
↓
Automatic directories and navigation

---

# 59. AI MUST PRESERVE STRUCTURE

AI should not flatten structured relationships into prose.

Instead of:

"Pam Deig is the executive director of the Housing Authority and is also connected to Carmi and White County."

The system should preserve:

PERSON:
Pam Deig

POSITION:
Executive Director

ORGANIZATION:
Housing Authority

COUNTY:
White County

CITY:
Carmi

This allows the information to be searched, filtered, connected, and reused.

---

# 60. FINAL PRINCIPLE

THE API GROUP PROFILE SYSTEM IS A DATABASE-FIRST SYSTEM.

THE PROFILE PAGE IS A TEMPLATE.

THE SIDEBAR IS A VIEW.

THE BREADCRUMB IS A PATH.

THE SEARCH IS A QUERY.

THE CONNECTIONS ARE DATABASE RELATIONSHIPS.

THE ARTICLE IS CONTENT.

THE SOURCE IS PROVENANCE.

THE AI IS AN ASSISTANT FOR CREATING AND MAINTAINING STRUCTURED INFORMATION.

THE HUMAN ADMINISTRATOR REMAINS IN CONTROL OF PUBLICATION.

THE SYSTEM MUST NEVER REQUIRE A DEVELOPER TO ADD A NEW COUNTY, CITY, VILLAGE, AGENCY, PERSON, OR CIVIC ORGANIZATION.

WHEN A NEW RECORD IS ADDED TO THE DATABASE, EVERY APPROPRIATE PUBLIC DIRECTORY, SIDEBAR, SEARCH RESULT, PROFILE CONNECTION, AND NAVIGATION VIEW SHOULD BE CAPABLE OF REFLECTING THAT NEW RECORD AUTOMATICALLY.