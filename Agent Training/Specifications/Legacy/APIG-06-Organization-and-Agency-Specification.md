# APIG-06 — Organization and Agency Specification

## Status

Active

## Purpose

This specification defines how APIG represents organizations and the relationships between organizations, jurisdictions, agencies, offices, positions, people, documents, meetings, news, and other entities.

APIG must be capable of representing both governmental and nongovernmental organizations.

Examples include:

- State agencies
- County agencies
- City departments
- Government offices
- Sheriff's departments
- Police departments
- Courts
- Boards
- Commissions
- Authorities
- Special districts
- Nonprofit organizations
- Civic organizations
- Churches
- Rotary clubs
- Community organizations
- Social organizations
- Professional organizations
- Other public-interest organizations

The system must distinguish the type of organization rather than forcing every organization into a governmental classification.

---

# 1. Core Organization Model

An organization is a distinct entity.

An organization is not the same thing as:

- A jurisdiction
- A person
- A position
- A building
- A document
- A news article

The general relationship is:

JURISDICTION
→ ORGANIZATION
→ OFFICE / DEPARTMENT / DIVISION
→ POSITION
→ PERSON

However, organizations may also operate across multiple jurisdictions or outside governmental jurisdictional boundaries.

---

# 2. Organization ID

Every organization should have a unique internal APIG identifier.

The identifier should remain stable even when:

- Leadership changes.
- Staff changes.
- The organization changes location.
- The organization changes its public-facing name.
- Departments are reorganized.
- Officers change.
- A website changes.

The identifier should not depend solely on the organization's name.

---

# 3. Organization Name

APIG should preserve the organization's official name where available.

The system may also preserve:

- Common name
- Short name
- Abbreviation
- Former name
- Alternate name
- Public-facing name

The official name should be preferred for authoritative records.

---

# 4. Organization Type

Organizations should be classified.

Possible types include:

- State government
- County government
- Municipal government
- Township government
- Government agency
- Government office
- Department
- Division
- Board
- Commission
- Authority
- Court
- Law enforcement agency
- Special district
- Nonprofit
- Civic organization
- Religious organization
- Social organization
- Professional organization
- Community organization
- Political organization
- Educational organization
- Business
- Media organization
- Other
- Unknown

The classification must reflect the organization's actual status.

---

# 5. Government Organization

Government organizations may include:

- State agencies
- County offices
- City departments
- Courts
- Sheriff's departments
- Police departments
- Boards
- Commissions
- Authorities
- Special districts

Government organizations should connect to their appropriate jurisdiction.

---

# 6. Nongovernmental Organization

APIG should also support organizations outside government.

Examples:

- Churches
- Rotary clubs
- Nonprofits
- Civic groups
- Neighborhood associations
- Charities
- Community organizations
- Professional associations
- Social organizations

These organizations should be represented separately from government agencies.

---

# 7. Organization and Jurisdiction

An organization may:

- Be located in a jurisdiction.
- Serve a jurisdiction.
- Govern a jurisdiction.
- Operate within a jurisdiction.
- Have jurisdiction over an area.
- Serve multiple jurisdictions.

These relationships must remain distinct.

---

# 8. Geographic Location

An organization may have a physical location.

The record may include:

- Street address
- City
- County
- State
- ZIP code
- Mailing address
- Primary office
- Additional locations

Only appropriate public information should be published.

---

# 9. Jurisdiction vs Location

Physical location does not necessarily establish governmental jurisdiction.

Example:

A regional agency may have an office in Richmond but serve multiple counties.

Therefore:

Located in

and:

Serves

should be represented as separate relationships.

---

# 10. Parent Organizations

An organization may belong to another organization.

Examples:

State Government
→ Department of Transportation

County Government
→ Sheriff's Department

City Government
→ Police Department

Rotary International
→ Local Rotary Club

The relationship should reflect the actual organizational structure.

---

# 11. Child Organizations

An organization may contain:

- Departments
- Offices
- Divisions
- Units
- Committees
- Branches
- Chapters

Each should be represented separately when appropriate.

---

# 12. Departments

Departments are organizational units.

Example:

City Government
→ Public Works Department

A department may contain:

- Director
- Deputy Director
- Staff
- Divisions
- Programs

---

# 13. Offices

An office may be an organizational unit or governmental office.

Examples:

- County Clerk's Office
- Coroner's Office
- Treasurer's Office
- Mayor's Office

The system should distinguish an office from a position where appropriate.

---

# 14. Divisions

Departments and agencies may contain divisions.

Example:

Sheriff's Department
→ Corrections Division

or:

Police Department
→ Investigations Division

The actual structure must be documented.

---

# 15. Units and Sections

Organizations may contain smaller units.

Examples:

- Patrol Division
- Records Unit
- Investigations Unit
- Communications Unit
- Administrative Section

These may be represented when relevant and sufficiently documented.

---

# 16. Boards

Boards are organizational entities.

A board may contain:

- Chair
- Vice Chair
- Members
- Staff
- Ex officio members

The board itself is distinct from the individuals who serve on it.

---

# 17. Commissions

Commissions should be represented as organizations or organizational bodies.

A commission may contain:

- Commissioners
- Chair
- Vice Chair
- Staff
- Appointed members
- Ex officio members

---

# 18. Authorities

Authorities should be represented as distinct organizations.

Examples:

- Housing authority
- Airport authority
- Redevelopment authority
- Transit authority

An authority may have:

- Board
- Executive Director
- Staff
- Departments
- Programs

---

# 19. Special Districts

Special districts should be represented independently.

Examples:

- School district
- Fire district
- Library district
- Water district
- Drainage district
- Sewer district

The organization should connect to every jurisdiction it serves where that information is known.

---

# 20. Law Enforcement Organizations

Law enforcement agencies should be classified appropriately.

Examples:

- Sheriff's Department
- Police Department
- State Police
- Campus Police
- Special law enforcement agency

The system should not merge different law enforcement agencies merely because they perform similar functions.

---

# 21. Sheriff's Department

A sheriff's department is an organization.

It may contain:

- Sheriff
- Chief Deputy
- Deputies
- Corrections
- Civil Division
- Administrative staff
- Other divisions

The actual structure should be based on evidence.

---

# 22. Police Department

A police department is an organization.

It may contain:

- Police Chief
- Deputy Chief
- Command staff
- Officers
- Detectives
- Administrative staff
- Divisions

Again, the actual structure must be documented.

---

# 23. Courts

Courts may be represented as organizations or governmental bodies according to their legal structure.

A court may connect to:

- Judges
- Clerks
- Prosecutors
- Public defenders
- Documents
- Hearings
- Cases

A courthouse building is not automatically the same entity as the court.

---

# 24. Nongovernmental Organizations

APIG may represent nongovernmental organizations where they are relevant to public-interest research.

Examples include:

- Nonprofits
- Charities
- Civic groups
- Churches
- Rotary clubs
- Neighborhood associations
- Community organizations
- Professional organizations

The organization type should be recorded.

---

# 25. Churches and Religious Organizations

Religious organizations may be represented where relevant to APIG's mission.

Examples:

Church
→ Pastor
→ Staff
→ Board
→ Members

Religious organizations should be classified as organizations rather than governmental bodies.

APIG should avoid making assumptions about religious affiliation of individual people.

---

# 26. Rotary Clubs

Rotary clubs may be represented as civic or social organizations.

Example:

Rotary Club
→ President
→ Officers
→ Members

Membership and leadership should be represented separately.

A person's membership should not automatically imply that they hold an officer position.

---

# 27. Civic Organizations

Civic organizations may include:

- Neighborhood groups
- Community associations
- Advocacy organizations
- Service clubs
- Civic clubs
- Volunteer organizations

The system should represent them as organizations where they are relevant.

---

# 28. Social Organizations

Social organizations may include:

- Clubs
- Associations
- Community groups
- Social clubs
- Other membership organizations

The organization should be classified according to its documented purpose.

---

# 29. Nonprofit Organizations

Nonprofits may be represented where relevant.

Where available, APIG may record:

- Legal name
- Public name
- Organization type
- Mission
- Location
- Officers
- Directors
- Board members
- Public filings
- Sources

The system should not assume nonprofit status without evidence.

---

# 30. Professional Organizations

Professional organizations may include:

- Bar associations
- Medical associations
- Trade organizations
- Professional societies
- Chambers
- Other professional groups

Membership relationships should be distinguished from leadership positions.

---

# 31. Membership

A person may be a member of an organization.

Example:

John Smith
→ Member of
→ Rotary Club

Membership is distinct from employment.

---

# 32. Employment

A person may be employed by an organization.

Example:

John Smith
→ Employee of
→ County Government

Employment should be represented separately from membership.

---

# 33. Leadership

A person may hold a leadership position in an organization.

Example:

John Smith
→ President
→ Rotary Club

This should be represented through the position model.

---

# 34. Organization Officers

Organizations may have officers such as:

- President
- Vice President
- Secretary
- Treasurer
- Chair
- Vice Chair
- Director

The organization officer position should be separate from the person occupying it.

---

# 35. Organization Board

An organization may have a board.

Example:

Nonprofit
→ Board of Directors
→ Chair
→ Treasurer
→ Members

The board and its members should be separately represented where appropriate.

---

# 36. Organization Committees

Organizations may contain committees.

Examples:

- Finance Committee
- Executive Committee
- Membership Committee
- Planning Committee

Committee membership may be represented as a relationship.

---

# 37. Chapters and Branches

An organization may contain local chapters or branches.

Example:

National Organization
→ State Chapter
→ County Chapter
→ Local Chapter

The exact relationship should be documented.

---

# 38. Organization Relationships

Organizations may have relationships including:

- Parent of
- Child of
- Branch of
- Chapter of
- Member of
- Partner of
- Serves
- Located in
- Operates in
- Governs
- Oversees
- Reports to
- Funded by
- Created by
- Established by
- Formerly known as
- Merged with
- Replaced by

Relationships must be supported by evidence where they represent factual claims.

---

# 39. Organization History

Organizations may change over time.

They may be:

- Created
- Renamed
- Reorganized
- Merged
- Split
- Abolished
- Replaced
- Converted
- Expanded
- Reduced

Historical information should be preserved.

---

# 40. Organization Name Changes

When an organization changes names, APIG should preserve:

- Current name
- Former name
- Effective date
- Source

Search should remain capable of finding the organization under historical names.

---

# 41. Mergers

When organizations merge, APIG should preserve the historical organizations.

Example:

Organization A
+

Organization B

→

Organization C

The system should not erase Organizations A and B.

---

# 42. Organizational Splits

An organization may split into multiple organizations.

Example:

Department A

→ Division B

→ Division C

Historical relationships should be preserved.

---

# 43. Abolished Organizations

When an organization is abolished, the historical record should remain.

The organization should be marked inactive or abolished rather than deleted.

---

# 44. Organization Status

Possible organization statuses include:

- Active
- Inactive
- Proposed
- Historical
- Abolished
- Merged
- Unknown
- Under Review

The status should be supported by evidence.

---

# 45. Organization Sources

Important organization facts should be traceable to sources.

Potential sources include:

- Official website
- Government records
- Charter
- Ordinance
- Statute
- Articles of incorporation
- Public filings
- Meeting minutes
- Annual reports
- Official directories
- Reliable news

---

# 46. Organization Verification

Organization records should support verification states.

Possible states include:

- Verified
- Partially Verified
- Unverified
- Conflicting
- Proposed
- Historical
- Unknown

---

# 47. Current Organization Verification

An organization may have existed historically but no longer exist.

Therefore, APIG should distinguish:

Historically verified

from:

Currently active and verified.

---

# 48. AI Organization Discovery

AI may discover organizations by reviewing:

- Government websites
- Public filings
- Meeting minutes
- News
- Organizational directories
- Official documents
- Other permitted sources

Discovery does not automatically equal verification.

---

# 49. AI Must Not Invent Organizations

AI must not create an organization simply because:

- A similar organization exists elsewhere.
- A jurisdiction normally has such an organization.
- A search result suggests it.
- The organization seems logically necessary.

The organization must be established from evidence.

---

# 50. AI Organization Classification

AI may propose an organization type.

Example:

"Rotary Club"

AI classification:
Civic / Social Organization

The classification should remain reviewable.

---

# 51. AI Organizational Relationships

AI may discover possible relationships.

Example:

County Government
→ Sheriff's Department

If supported by official sources, the relationship may be verified.

If only inferred, it should remain proposed.

---

# 52. Administrator Review

Administrators should be able to review:

- New organizations
- Organization classifications
- Parent/child relationships
- Jurisdiction relationships
- Mergers
- Name changes
- Organizational status
- Conflicting sources
- AI-generated relationships

---

# 53. Organization Search

Users should be able to search directly for organizations.

Examples:

- Wayne County Sheriff's Office
- Richmond Police Department
- Rotary Club
- Housing Authority
- County Health Department

Search should distinguish similarly named organizations using:

- Location
- Jurisdiction
- Organization type
- Parent organization

---

# 54. Organization Navigation

A user viewing an organization should be able to navigate to:

- Parent organization
- Child organizations
- Departments
- Offices
- Positions
- People
- Jurisdictions
- Documents
- Meetings
- News
- Sources

---

# 55. Breadcrumb Navigation

Example:

Home
→ Indiana
→ Wayne County
→ County Government
→ Sheriff's Department

Each prior level should remain selectable.

---

# 56. Person-to-Organization Navigation

A person page should show relevant organizations.

Example:

John Smith
→ Wayne County Sheriff's Office
→ Rotary Club
→ Regional Board

The relationship type should be clear.

Examples:

- Employee
- Member
- Officer
- Board Member
- Director
- Volunteer

---

# 57. Organization-to-Person Navigation

An organization page should show relevant people.

Possible categories include:

- Leadership
- Officers
- Employees
- Board Members
- Commissioners
- Members
- Former Members

The exact categories depend on the organization.

---

# 58. Organization-to-Document Navigation

Organizations may be referenced by:

- Meeting minutes
- Agendas
- Reports
- Budgets
- Policies
- Ordinances
- Public filings
- Other documents

The organization page may provide links to relevant documents.

---

# 59. Organization-to-News Navigation

News may reference organizations.

The organization page may provide relevant news references.

News should remain distinguishable from official documentation.

---

# 60. Organization-to-Meeting Navigation

Meetings may establish organizational information.

Examples:

- Board appointments
- Organizational changes
- Elections of officers
- Policy decisions
- Budget decisions
- Department actions

Meeting records should remain connected to the organization.

---

# 61. Organization Contact Information

Where appropriate, APIG may record public organizational contact information.

Examples:

- Office address
- Phone
- Official email
- Website
- Contact form
- Public social media account

Official contact information should be preferred.

---

# 62. Organization Website

An organization may have one or more official websites.

APIG should distinguish:

- Official website
- Government website
- Parent organization website
- Social media
- Third-party websites

Official sources should be preferred for verification.

---

# 63. Organization Social Media

Where relevant, public organizational social media accounts may be connected to the organization.

The system should distinguish official organizational accounts from unofficial accounts.

---

# 64. Physical Facilities

An organization may occupy one or more physical facilities.

A facility is not necessarily the same entity as the organization.

Example:

County Courthouse
→ contains
→ County Clerk's Office

The courthouse is a physical location.

The Clerk's Office is an organization or office.

These should not be merged.

---

# 65. Multiple Locations

Organizations may have multiple locations.

The system should support:

- Headquarters
- Branch offices
- Satellite offices
- Facilities
- Mailing addresses

---

# 66. Organization Jurisdiction Map

Organizations with geographic service areas may eventually be displayed on maps.

Examples:

- Police jurisdiction
- Fire district
- School district
- Water district
- Regional authority

Mapping must distinguish physical location from service area.

---

# 67. Organization Hierarchy and Breadcrumbs

The organization hierarchy should integrate with the broader APIG hierarchy.

Example:

Indiana
→ Wayne County
→ Richmond
→ City Government
→ Police Department
→ Police Chief
→ Person

Another example:

Indiana
→ Wayne County
→ Civic Organizations
→ Rotary Club
→ President
→ Person

The navigation structure should adapt to the actual organization.

---

# 68. Multiple Entry Points

Users should be able to begin with:

- State
- County
- City
- Agency
- Organization
- Person
- Position
- Document
- News
- Search

All routes should connect to the same underlying organization entities.

---

# 69. No Duplicate Organization

If multiple sources identify the same organization, APIG should attempt to maintain one organization entity.

Potential duplicate records should be flagged for review.

---

# 70. Organization Merge

If two records are proven to represent the same organization, they may be merged.

The merge process should preserve:

- Sources
- Historical names
- Relationships
- Documents
- People
- Audit history

---

# 71. Organization Split

If one organization record is later discovered to represent multiple organizations, the system should support splitting the record.

Historical information and source relationships must be preserved.

---

# 72. Audit Trail

Important organization changes should be auditable.

The system should eventually record:

- Previous value
- New value
- Date
- Source
- User or AI responsible
- Approval status

---

# 73. Public vs Administrative View

Public users may see:

- Organization name
- Type
- Location
- Jurisdiction
- Leadership
- Members where appropriate
- Sources
- Documents
- Meetings
- News

Administrative users may additionally see:

- Proposed organizations
- AI suggestions
- Conflicting sources
- Verification status
- Internal notes
- Pending reviews

---

# 74. Organization Data Quality

A strong organization record should establish:

- Identity
- Organization type
- Jurisdiction or service area
- Location where relevant
- Organizational relationships
- Current status
- Relevant positions
- Relevant people
- Source evidence
- Verification status

---

# 75. Unknown Information

Unknown information should remain unknown.

Examples:

Organization type:
Unknown

Current president:
Unknown

Parent organization:
Unknown

Jurisdiction:
Unknown

The system must not invent missing organizational information.

---

# 76. AI Tasking

When an AI receives a task involving an organization, it should determine what kind of task is being requested.

Examples:

"Who runs this organization?"

"What county does this agency serve?"

"Is this a government agency?"

"Who are the members?"

"When was this organization created?"

"Find the official source."

Different questions may require different resource specifications.

---

# 77. Resource Selection

The AI should consult the appropriate APIG resource specification.

Examples:

Person question
→ Person specification

Position question
→ Position specification

Government hierarchy question
→ Government hierarchy specification

Organization question
→ Organization specification

Source question
→ Source and provenance specification

The APIG root resource document should identify where these resources are stored.

---

# 78. Core Organization Principles

The organization model follows these principles:

1. An organization is a distinct entity.
2. An organization is not a person.
3. An organization is not a position.
4. An organization is not a physical building.
5. Government and nongovernment organizations can coexist in the system.
6. Organizations may belong to larger organizations.
7. Organizations may serve multiple jurisdictions.
8. Physical location and jurisdiction must remain distinct.
9. Historical organizations should be preserved.
10. AI may discover organizations but must not invent them.
11. Significant organizational facts should be traceable to sources.
12. Unknown information should remain unknown.

---

# 79. Summary

APIG's organization model provides a common framework for representing:

- Governments
- Agencies
- Departments
- Offices
- Boards
- Commissions
- Authorities
- Special districts
- Nonprofits
- Churches
- Rotary clubs
- Civic organizations
- Social organizations
- Professional organizations
- Other public-interest organizations

The model connects organizations to:

- Jurisdictions
- Other organizations
- Offices
- Departments
- Positions
- People
- Documents
- Meetings
- News
- Sources

The system must preserve the difference between:

ORGANIZATION
POSITION
PERSON
JURISDICTION
PHYSICAL LOCATION

This distinction is necessary for accurate navigation, historical research, source verification, and AI-assisted data collection.

---

# 80. Relationship to Other Specifications

This specification defines organizations and agencies.

Related specifications should define:

- Government and jurisdiction hierarchy
- Person identity
- Positions and offices
- Sources and provenance
- Documents
- Meetings
- News
- Search
- Database schema
- Website interface
- AI operations
- Privacy and security

Those specifications should remain consistent with this organization model unless formally revised.

---

# 81. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-06