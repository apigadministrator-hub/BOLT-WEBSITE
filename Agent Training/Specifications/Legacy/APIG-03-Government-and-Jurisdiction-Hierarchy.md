# APIG-03 — Government and Jurisdiction Hierarchy

## Status

Active

## Purpose

This specification defines how APIG represents geographic jurisdictions, governmental structures, municipalities, agencies, offices, departments, positions, and the relationships between them.

The objective is to allow a user or AI to move from a broad geographic area to increasingly specific governmental information while preserving the actual structure of the government being documented.

APIG must represent government as it actually exists, not merely as a simplified template.

---

# 1. Core Geographic Hierarchy

APIG's general geographic navigation model is:

State
→ County
→ Municipality
→ Agency / Organization
→ Position
→ Person

This is the default navigation model.

It is not an assumption that every jurisdiction will contain every level.

Actual governmental structures may differ.

---

# 2. State

A state is a top-level geographic and governmental jurisdiction within the APIG geographic model.

A state record may include:

- Official name
- Common name
- Abbreviation
- State government
- Counties
- Municipalities
- State agencies
- State-level elected offices
- State-level appointed offices
- Documents
- Sources
- Historical information

A state should serve as a major starting point for geographic navigation.

---

# 3. County

A county is a geographic and governmental subdivision of a state.

A county record may include:

- Official name
- State
- County government
- Municipalities
- Towns
- Villages
- Townships where applicable
- County agencies
- County offices
- County boards
- County commissions
- Elected officials
- Appointed officials
- Documents
- Meetings
- Sources
- Related organizations

A county should be connected to its parent state.

Example:

Indiana
→ Wayne County

---

# 4. Municipality

A municipality is a local governmental jurisdiction such as:

- City
- Town
- Village
- Borough
- Other locally recognized governmental unit

The exact classification should reflect the jurisdiction's actual legal or governmental designation.

A municipality should be connected to its relevant county or counties when applicable.

Example:

Indiana
→ Wayne County
→ City of Richmond

---

# 5. Jurisdictional Boundaries

Geographic relationships must not be assumed to be perfectly nested.

A governmental entity may:

- Cross county boundaries
- Serve multiple municipalities
- Serve an entire county
- Serve multiple counties
- Operate across a region
- Have authority over a special district
- Have jurisdiction that differs from geographic boundaries

APIG should therefore distinguish:

Where an entity is located

from:

Where an entity operates or has authority.

---

# 6. Government Organization

A government may contain multiple organizations, offices, departments, agencies, boards, commissions, and other bodies.

For example:

County Government
→ Sheriff's Department
→ Coroner's Office
→ County Clerk
→ County Treasurer
→ County Auditor
→ County Assessor
→ County Commissioners
→ County Council

This is an example only.

The actual governmental structure must be established from authoritative sources.

---

# 7. Government Organization Types

APIG should support classification of governmental entities.

Possible types include:

- State government
- County government
- City government
- Town government
- Village government
- Township government
- Department
- Agency
- Office
- Board
- Commission
- Authority
- District
- Court
- Law enforcement agency
- Special-purpose governmental body
- Other

The classification should be based on the entity's actual status.

---

# 8. County Government

County government should be represented as an organization rather than merely as a label attached to the county.

This allows the county government to have:

- Leadership
- Departments
- Offices
- Positions
- Employees
- Elected officials
- Appointed officials
- Meetings
- Documents
- Policies
- Related organizations

Example:

Wayne County
→ Wayne County Government

---

# 9. City Government

City government should likewise be represented as an organization.

Example:

Wayne County
→ City of Richmond
→ City Government

City government may contain:

- Mayor
- City Council
- Departments
- Police Department
- Boards
- Commissions
- Offices
- Staff
- Other governmental bodies

The actual structure should be documented rather than assumed.

---

# 10. Village and Town Government

Where villages, towns, or other local governmental units exist, APIG should represent them separately.

Example:

County
→ Town
→ Town Government
→ Department
→ Position
→ Person

The system should not force a town into a city classification merely for convenience.

---

# 11. Law Enforcement

Law enforcement should be represented as an organizational category.

A user navigating law enforcement should be able to distinguish between different types of law enforcement agencies.

For example:

Law Enforcement
→ Sheriff's Department

or:

Law Enforcement
→ Police Department

The exact hierarchy depends upon the jurisdiction.

---

# 12. Sheriff's Department

A sheriff's department should be represented as its own agency or organization.

Where applicable, the structure may include:

Sheriff's Department
→ Sheriff
→ Chief Deputy
→ Command Staff
→ Deputies
→ Civil Division
→ Corrections
→ Other divisions

The actual structure should be determined from authoritative sources.

The system must not assume that every sheriff's department has the same internal structure.

---

# 13. Police Department

A police department should be represented independently from a sheriff's department.

Example:

City
→ Police Department
→ Police Chief
→ Command Staff
→ Officers

Different police departments may use different organizational structures.

APIG should preserve the actual structure documented by the agency.

---

# 14. Coroner's Office

A coroner's office should be represented as an identifiable governmental office or agency when applicable.

Example:

County
→ County Government
→ Coroner's Office
→ Coroner
→ Staff

The position of Coroner should be separately represented from the person occupying it.

---

# 15. Clerk Offices

Clerk offices may exist at different governmental levels.

Examples include:

- County Clerk
- City Clerk
- Town Clerk
- Court Clerk
- Township Clerk

APIG should distinguish these offices rather than assuming that all "clerks" belong to the same organization.

Example:

County
→ County Government
→ County Clerk's Office
→ County Clerk

and:

City
→ City Government
→ City Clerk's Office
→ City Clerk

---

# 16. Courthouse and Judicial Functions

Courthouse-related information may involve multiple distinct governmental entities.

A courthouse building is not necessarily the same thing as:

- County government
- Court
- Clerk's office
- Prosecutor's office
- Sheriff's department
- Other offices located in the courthouse

APIG should distinguish physical location from governmental organization.

Where appropriate, courthouse-related organizations should be connected through their actual governmental relationships.

---

# 17. Courts

Courts should be represented as governmental or judicial organizations according to their actual legal structure.

A court may connect to:

- Judges
- Clerks
- Prosecutors
- Public defenders
- Documents
- Hearings
- Cases
- Orders
- Jurisdiction

Court information should not automatically be merged into county government simply because the court is physically located in the county courthouse.

---

# 18. Elected Offices

An elected office must be identified as an elected position.

Examples may include:

- Sheriff
- County Clerk
- County Treasurer
- County Auditor
- County Assessor
- County Commissioner
- Mayor
- City Council Member
- Other elected positions

The exact elected offices vary by jurisdiction.

APIG should establish the classification from authoritative documentation.

---

# 19. Appointed Positions

An appointed position should be identified as appointed when the source establishes that fact.

The record should distinguish:

- Position
- Appointing authority
- Person appointed
- Appointment date
- Term
- Source

This allows APIG to represent the difference between an elected official and an appointed official.

---

# 20. Employment Positions

Not every position is elected or appointed.

Some positions are filled through employment.

Examples:

- Administrative staff
- Clerks
- Deputies
- Department employees
- Directors
- Assistants

Where known, APIG may identify the position as:

- Elected
- Appointed
- Hired
- Contracted
- Volunteer
- Ex officio
- Unknown

---

# 21. Boards and Commissions

Government boards and commissions should be represented as organizations or governmental bodies.

A board may contain:

- Chair
- Vice Chair
- Members
- Officers
- Staff
- Appointed members
- Elected members
- Ex officio members

The specific structure must be based on the organization's governing documents.

---

# 22. Authorities

Government authorities should be represented as distinct organizational entities.

Examples may include:

- Housing authority
- Redevelopment authority
- Airport authority
- Public transportation authority
- Other special-purpose authority

A housing authority may have a structure such as:

Housing Authority
→ Board of Commissioners
→ Resident Commissioner
→ Executive Director
→ Staff

If a Resident Commissioner position is elected, appointed, or otherwise selected through a particular process, that distinction should be recorded.

---

# 23. Special Districts

Special districts may cross ordinary municipal or county boundaries.

Examples include:

- School districts
- Fire districts
- Drainage districts
- Library districts
- Water districts
- Sewer districts
- Other special-purpose districts

APIG should represent the district independently and connect it to the geographic areas it serves.

---

# 24. Township Government

Where township government exists, it should be represented as its own governmental entity.

A township should not automatically be treated as a municipality.

Its relationship to counties, cities, towns, villages, and other governmental units should be represented according to the actual jurisdictional structure.

---

# 25. Multiple Jurisdictions

An organization may serve more than one jurisdiction.

Example:

Regional Agency
→ serves
→ County A

Regional Agency
→ serves
→ County B

APIG must allow multiple jurisdiction relationships.

The organization should not be duplicated merely because it serves multiple areas.

---

# 26. Location vs Jurisdiction

APIG should distinguish:

Physical location

from:

Governmental jurisdiction.

Example:

An agency may have an office located in City A while exercising authority over County A, County B, and County C.

The database should preserve both facts.

---

# 27. Organizational Hierarchy

The hierarchy should allow:

Parent organization
→ Child organization
→ Department
→ Division
→ Position
→ Person

Not every level is required.

The hierarchy should reflect the documented organization.

---

# 28. Positions Belong to Organizations

A position should normally be connected to the organization responsible for that position.

Example:

Sheriff
→ belongs to
→ Sheriff's Department

County Clerk
→ belongs to
→ County Government / Clerk's Office

Mayor
→ belongs to
→ City Government

This permits navigation between the position and organization.

---

# 29. People Occupy Positions

People should be connected to positions through explicit relationships.

Example:

Jane Doe
→ holds
→ County Clerk

The position remains even if Jane Doe leaves office.

A later person can then be connected to the same position.

---

# 30. Terms of Office

Where applicable, APIG should record:

- Start date
- End date
- Term length
- Election date
- Appointment date
- Resignation date
- Removal date
- Vacancy date
- Succession information

The exact fields will be defined in the person and position specifications.

---

# 31. Vacancies

A position may exist even when no person currently occupies it.

Therefore:

Position ≠ Person.

If the position exists but its current holder cannot be established, APIG should preserve the position and identify the occupant as:

Unknown

or another appropriate status.

---

# 32. Unknown Officeholders

If a governmental position is known to exist but the current officeholder cannot be verified:

Position:

County Coroner

Officeholder:

Unknown

The AI must not invent a name merely because the position is expected to have an occupant.

---

# 33. Source Hierarchy

Government hierarchy should preferably be established using authoritative sources.

Potential sources include:

1. Official government websites
2. Government organizational documents
3. Statutes and ordinances
4. Official meeting minutes
5. Official agendas
6. Official reports
7. Government directories
8. Election records
9. Public records
10. Reliable secondary sources

Secondary sources may assist discovery, but authoritative sources should be preferred for final verification.

---

# 34. Meeting Minutes as Evidence

Meeting minutes may establish:

- Who attended
- Who held a position
- Who was appointed
- Who resigned
- Who voted
- What organization acted
- What action occurred
- When an event occurred

When minutes are used to establish a fact, APIG should preserve the specific meeting and document used.

Where practical, the record should identify the relevant meeting date and document.

---

# 35. News Sources as Evidence

News articles may provide useful evidence regarding:

- Appointments
- Elections
- Resignations
- Organizational changes
- Public events
- Public statements
- Historical events

News should not automatically override an official source.

Conflicting information should be documented rather than silently resolved.

---

# 36. Hierarchy Discovery

AI may be used to discover governmental structures.

An AI may:

- Search official websites
- Identify agencies
- Identify offices
- Identify positions
- Identify officeholders
- Extract organizational relationships
- Locate documents
- Compare sources
- Identify missing information

AI-discovered hierarchy should remain appropriately marked until the required verification process is completed.

---

# 37. Administrator Approval

If APIG requires administrator approval before newly discovered information becomes authoritative:

AI discovery should create a proposed record rather than silently publishing the information.

Example:

AI discovers:

Wayne County Coroner → Person X

The system records:

- Position
- Proposed person
- Source
- Discovery date
- Verification status

The administrator may then approve or reject the proposed relationship.

---

# 38. Geographic Navigation

The public interface should allow users to navigate geographically.

A general flow may be:

Home
→ States
→ State
→ Counties
→ County
→ Municipalities
→ Municipality
→ Agencies
→ Position
→ Person

The exact interface may use maps, lists, search, or combinations of these methods.

---

# 39. State Map

A state-selection interface may allow the user to view a map of the United States.

The user may select a state.

After selecting a state, the interface may present a state-specific map showing its counties.

The map should identify counties clearly enough that users can select the desired county.

Interactive mapping requirements belong to the website implementation specification.

---

# 40. County Map

A county-selection interface may display the selected state's counties.

The user should be able to identify counties by:

- Name
- Map location
- Hover interaction
- Search
- List

Mobile users should have an alternative to hover-based interaction because hover does not exist on most touch devices.

---

# 41. Search Alternative

Maps should never be the only way to navigate.

Users may not know the geographic location of the county they want.

Users should therefore be able to search by:

- State
- County
- City
- Agency
- Organization
- Person

A user should not need to know a ZIP code to locate a jurisdiction.

---

# 42. Navigation Breadcrumb

When navigating through the hierarchy, the user should be able to see their current location.

Example:

Home
→ Indiana
→ Wayne County
→ Richmond
→ Police Department
→ Police Chief
→ Person

Each previous level should be available as a navigation destination.

---

# 43. Direct Search

A user should also be able to bypass geographic navigation.

For example:

Search:
"Wayne County Coroner"

or:

Search:
"John Smith"

The search system should return the relevant entity and its relationships.

---

# 44. Multiple Entry Points

APIG should support several entry points into the same information network.

A user may begin with:

- State
- County
- City
- Agency
- Organization
- Person
- Position
- Document
- News article
- Search

The resulting records should connect to the same underlying entities.

---

# 45. No Duplicate Entity When Avoidable

If the same organization is discovered from multiple sources, APIG should not automatically create multiple organizations.

The system should attempt to identify whether the records represent the same entity.

Likewise, multiple references to the same person should be connected to one person entity when identity can be established.

Identity resolution rules will be defined in later specifications.

---

# 46. Historical Government Structures

Government structures change.

Departments may be:

- Created
- Abolished
- Renamed
- Merged
- Split
- Transferred
- Reorganized

APIG should preserve these changes historically.

The current hierarchy should not erase the previous hierarchy.

---

# 47. Name Changes

Organizations and positions may change names.

APIG should preserve:

- Current name
- Previous name
- Effective date
- Source

A historical search should remain capable of finding the entity under its previous name.

---

# 48. Government Hierarchy Is Evidence-Based

The AI must not assume:

- Every county has the same offices.
- Every city has the same departments.
- Every sheriff's department has the same divisions.
- Every housing authority has the same board structure.
- Every elected position exists in every jurisdiction.
- Every organization follows the same hierarchy.

The actual documented structure controls.

---

# 49. Core Hierarchy Model

The general APIG model is:

STATE
  |
  +-- COUNTY
        |
        +-- MUNICIPALITY
        |
        +-- COUNTY GOVERNMENT
        |      |
        |      +-- AGENCY
        |      |     |
        |      |     +-- POSITION
        |      |           |
        |      |           +-- PERSON
        |      |
        |      +-- OFFICE
        |      |
        |      +-- BOARD
        |            |
        |            +-- POSITION
        |
        +-- SPECIAL DISTRICT
        |
        +-- OTHER ORGANIZATION

This diagram is conceptual.

Actual relationships may differ.

---

# 50. Required Relationship Types

The architecture should support relationships including:

- Located in
- Part of
- Serves
- Governs
- Has jurisdiction over
- Contains
- Operates within
- Reports to
- Oversees
- Holds position
- Formerly held
- Appointed to
- Elected to
- Member of
- Serves on
- Related to

The detailed relationship schema belongs to later specifications.

---

# 51. Hierarchy and Data Quality

A hierarchy record should be considered stronger when:

- The organization is clearly identified.
- The jurisdiction is clearly identified.
- The relationship is documented.
- The source is authoritative.
- The date is known.
- Conflicting information has been addressed.
- Verification status is recorded.

The absence of one of these does not necessarily invalidate the record, but uncertainty should be represented.

---

# 52. Administrator Review

Administrators should be able to review:

- Newly discovered organizations
- Newly discovered positions
- Proposed person relationships
- Organizational hierarchy changes
- Source evidence
- Conflicting records
- Unverified records

Approval should be capable of being recorded.

---

# 53. Expansion by County

APIG may initially be developed county by county.

The system should support this development strategy.

A county can be developed as a complete unit containing:

- Government
- Agencies
- Municipalities
- Organizations
- Positions
- People
- Documents
- Meetings
- Sources

Once the structure is proven, the same architecture can be applied to additional counties.

The architecture should not require a separate software system for each county.

---

# 54. Expansion by State

After county-level systems are established, APIG should be capable of expanding to additional states.

The same general model should remain usable while allowing state-specific governmental structures.

---

# 55. AI Propagation

Eventually, AI may be used to propagate the APIG hierarchy into additional jurisdictions.

Potential workflow:

Established model
→ AI discovers new jurisdiction
→ AI discovers organizations
→ AI discovers positions
→ AI discovers people
→ AI attaches sources
→ AI identifies relationships
→ AI assigns verification state
→ Administrator reviews where required
→ Approved records become authoritative

The AI should use the established architecture rather than inventing a new structure for each county.

---

# 56. Mobile Considerations

All hierarchy functions must remain usable on mobile devices.

A mobile user should be able to:

- Select a state
- Select a county
- Select a municipality
- Select an agency
- View positions
- View people
- Search directly
- Navigate backward
- View source information

Hover-only interfaces must have touch-compatible alternatives.

---

# 57. Administrative and Public Views

The public hierarchy may show only approved information.

The administrative hierarchy may additionally show:

- Proposed records
- Unverified records
- Source conflicts
- Pending approvals
- AI-generated suggestions
- Internal notes

The public and administrative views should use the same underlying entities where practical.

---

# 58. Summary

APIG's governmental hierarchy is a connected model of:

State
→ County
→ Municipality
→ Government / Organization
→ Agency / Office
→ Position
→ Person

The model is flexible enough to represent:

- Sheriff's departments
- Police departments
- Coroner's offices
- Clerks
- Courts
- Boards
- Commissions
- Housing authorities
- Special districts
- Other governmental bodies

The system must distinguish:

- Jurisdiction
- Organization
- Agency
- Office
- Position
- Person
- Physical location
- Source
- Evidence
- Verification status

The actual structure must be established from evidence.

AI may discover and organize the structure, but it must not invent governmental relationships.

Historical structures should be preserved.

Unknown information should remain explicitly unknown.

The hierarchy should support both geographic navigation and direct search.

The architecture must support incremental county-by-county development and eventual large-scale AI-assisted expansion.

---

# 59. Relationship to Other Specifications

This specification establishes the governmental and geographic hierarchy.

Later specifications should define in greater detail:

- Person identity
- Position records
- Organization records
- Source and provenance
- Documents
- Meetings
- Verification
- Database schema
- Website navigation
- Maps
- Search
- AI operations
- Administrator approval

Those specifications should remain consistent with this hierarchy unless this specification is formally revised.

---

# 60. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-03