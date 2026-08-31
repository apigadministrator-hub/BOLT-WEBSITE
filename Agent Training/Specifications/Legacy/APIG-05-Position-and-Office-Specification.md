# APIG-05 — Position and Office Specification

## Status

Active

## Purpose

This specification defines how APIG represents governmental and organizational offices and positions.

The central principle is:

POSITION ≠ PERSON

An office or position may exist independently of the individual who occupies it.

A person may occupy a position temporarily, leave it, return to it, or move to another position.

APIG must preserve the identity and history of the position independently from the people who hold it.

---

# 1. Core Model

The general relationship is:

PERSON
→ holds
→ POSITION

POSITION
→ belongs to
→ ORGANIZATION

ORGANIZATION
→ operates within / serves
→ JURISDICTION

The position is the persistent structural entity.

The person is the occupant.

---

# 2. Office

An office is an established governmental or organizational function.

Examples:

- Office of the Mayor
- County Clerk's Office
- Sheriff's Office
- Treasurer's Office
- Coroner's Office

An office may contain one or more positions.

---

# 3. Position

A position is a specific role that can be occupied by a person.

Examples:

- Mayor
- Sheriff
- County Clerk
- County Treasurer
- Police Chief
- Executive Director
- Board Member

A position may exist even when it is vacant.

---

# 4. Office vs Position

APIG should distinguish:

OFFICE

from:

POSITION

Example:

County Clerk's Office
→ County Clerk

The office is the organizational or governmental unit.

The County Clerk is the position.

The person occupying the position is a separate entity.

---

# 5. Position Record

A position record may include:

- Position ID
- Position name
- Official title
- Organization
- Office
- Department
- Jurisdiction
- Position type
- Election status
- Appointment status
- Employment status
- Term information
- Current occupant
- Historical occupants
- Vacancy status
- Source
- Verification status
- Effective dates
- Notes

---

# 6. Position ID

Every position should have a unique internal APIG identifier.

The Position ID should remain stable when:

- A person leaves.
- A new person is elected.
- A new person is appointed.
- The position becomes vacant.
- The position changes occupant.

If the position itself is abolished and later recreated, the system should determine whether it represents the same historical position or a new position based on evidence.

---

# 7. Position Name

The system should preserve the official title where available.

Example:

Wayne County Sheriff

The display name may be shortened in some interfaces, but the underlying record should preserve the official designation.

---

# 8. Position Type

A position may be classified as:

- Elected
- Appointed
- Hired
- Contract
- Volunteer
- Ex officio
- Board membership
- Commission membership
- Other
- Unknown

The classification must be evidence-based.

---

# 9. Elected Position

An elected position is filled through an election.

Examples may include:

- Mayor
- Sheriff
- County Commissioner
- County Clerk
- Treasurer
- City Council Member

Not every jurisdiction uses the same elected offices.

APIG must not assume that an office is elected without evidence.

---

# 10. Appointed Position

An appointed position is filled through an appointment process.

The position record may identify:

- Appointing authority
- Appointment date
- Term
- Appointee
- Appointment source

Examples may include:

- Department Director
- Board Member
- Commission Member
- Executive Director

---

# 11. Employment Position

A position may be filled through ordinary employment.

Examples:

- Administrative Assistant
- Deputy
- Analyst
- Clerk
- Department Employee
- Staff Member

Employment positions may not have formal governmental terms.

---

# 12. Board Position

Board positions should be represented independently.

Example:

Housing Authority
→ Board of Commissioners
→ Commissioner

The Commissioner position is distinct from the person serving as Commissioner.

---

# 13. Commission Position

Commission membership should likewise be represented as a position.

Example:

Planning Commission
→ Commissioner

Where applicable, APIG should record:

- Appointment authority
- Term
- Start date
- End date
- Current occupant
- Source

---

# 14. Multiple Positions

A person may occupy multiple positions simultaneously.

Example:

Person
→ City Council Member

and:

Person
→ Regional Planning Commission Member

Each relationship should be represented separately.

---

# 15. One Position, Multiple Historical Occupants

A position may have many occupants over time.

Example:

County Sheriff

2018–2022
→ Person A

2022–2026
→ Person B

2026–2030
→ Person C

The position remains the same conceptual entity.

---

# 16. Position History

APIG should preserve the historical history of a position.

Historical information may include:

- Previous occupants
- Terms
- Elections
- Appointments
- Vacancies
- Resignations
- Removals
- Position renaming
- Organizational changes

---

# 17. Current Occupant

A position may have a current occupant.

The relationship should include:

- Person
- Position
- Start date
- End date if known
- Verification status
- Source

The current occupant should not be assumed merely because the person was previously documented in the position.

---

# 18. Vacancy

A position may exist without a current occupant.

Possible status:

Position:
Active

Occupant:
Vacant

or:

Occupant:
Unknown / Needs Verification

Vacancy and unknown status should be distinguishable when the evidence permits.

---

# 19. Vacancy vs Unknown

These are different conditions.

Vacant:

Evidence establishes that nobody currently occupies the position.

Unknown:

APIG does not have sufficient evidence to determine the current occupant.

The system must not treat unknown as vacant.

---

# 20. Term

Positions may have defined terms.

A term may include:

- Start date
- End date
- Length
- Election cycle
- Appointment period
- Renewal provisions

Not every position has a fixed term.

---

# 21. Term Expiration

When a term expires, APIG should determine whether:

- The person left the position.
- The person was reelected.
- The person was reappointed.
- The position became vacant.
- The person remains temporarily in the position under applicable rules.

The system must rely on evidence rather than automatically assuming departure.

---

# 22. Resignation

A resignation should be represented as a historical event affecting the person's relationship to the position.

Where documented, record:

- Person
- Position
- Resignation date
- Effective date
- Source
- Successor status

---

# 23. Removal

A removal from office should be represented separately from resignation.

Where documented, record:

- Person
- Position
- Removal authority
- Effective date
- Source

The system should not characterize a departure as removal without evidence.

---

# 24. Succession

A position may transfer from one person to another.

APIG should preserve the sequence.

Example:

Position
→ Person A
→ Person B
→ Person C

Each relationship should have its own dates and sources.

---

# 25. Acting Positions

A person may temporarily serve in an acting capacity.

Examples:

- Acting Sheriff
- Interim Mayor
- Acting Director
- Interim Executive Director

The system should distinguish:

Permanent holder

from:

Acting holder

when the source establishes the distinction.

---

# 26. Interim Positions

An interim appointment should be represented as a temporary relationship when supported by evidence.

Example:

Position:
Executive Director

Permanent status:
Vacant

Interim holder:
Person A

The interim relationship should have appropriate dates.

---

# 27. Deputy and Assistant Positions

Positions such as:

- Deputy
- Assistant
- Chief Deputy
- Deputy Director
- Assistant Director

should be represented as distinct positions when they constitute identifiable roles.

They should not automatically be merged with the primary position.

---

# 28. Staff Positions

Staff positions may be represented where they are publicly documented and relevant to APIG's mission.

Examples:

- Chief of Staff
- Administrative Director
- Office Manager
- Clerk
- Public Information Officer

The level of detail should correspond to the available evidence and project scope.

---

# 29. Department Positions

A department may contain multiple positions.

Example:

Police Department
→ Police Chief
→ Deputy Chief
→ Captain
→ Lieutenant
→ Sergeant
→ Officer

This is illustrative only.

APIG must document the actual structure of each organization.

---

# 30. Position Reporting Relationships

Where documented, APIG may represent:

Position A
→ reports to
→ Position B

Example:

Deputy Director
→ reports to
→ Director

Reporting relationships must be based on organizational evidence.

---

# 31. Supervisory Relationships

Where documented:

Position A
→ supervises
→ Position B

The system should distinguish supervisory relationships from general organizational membership.

---

# 32. Position Authority

Where relevant, a position may have documented authority.

Examples:

- Signs documents
- Supervises staff
- Issues permits
- Conducts investigations
- Chairs meetings
- Appoints personnel
- Executes contracts

Authority should be sourced from law, policy, organizational documents, or other reliable evidence.

---

# 33. Legal Authority

Where a position's authority is established by statute, ordinance, charter, regulation, or other legal authority, APIG may connect the position to that source.

Example:

Position
→ authority established by
→ statute

This creates a relationship between the position and its governing authority.

---

# 34. Position Qualifications

Where publicly documented, APIG may record requirements for a position.

Examples:

- Residency
- Professional license
- Education
- Experience
- Certification
- Age requirement
- Other legal qualifications

The system should distinguish requirements from characteristics of the person currently holding the position.

---

# 35. Position Compensation

Compensation may eventually be represented where relevant and legally/publicly available.

Possible information includes:

- Salary
- Salary range
- Per diem
- Stipend
- Benefits
- Compensation schedule

Compensation belongs to the position or employment relationship, not automatically to the person.

---

# 36. Position Contact Information

Where appropriate, official contact information may be associated with a position or office.

Examples:

- Office phone
- Official email
- Office address
- Official contact form

The system should prefer official organizational contact information.

---

# 37. Position Sources

Every significant position fact should be traceable to a source.

Potential sources include:

- Government website
- Organizational chart
- Charter
- Ordinance
- Statute
- Meeting minutes
- Appointment record
- Election record
- Government directory
- Official report

---

# 38. Position Verification

Position records should support verification states.

Possible states include:

- Verified
- Partially Verified
- Unverified
- Conflicting
- Proposed
- Historical
- Abolished
- Unknown

---

# 39. Current Position Verification

The existence of a position may be verified even when its current occupant is not.

Example:

Position:
County Treasurer

Position status:
Verified

Current occupant:
Unknown

These states should remain separate.

---

# 40. Conflicting Position Information

If sources disagree about a position, APIG should preserve the conflict.

Example:

Source A:
Position belongs to Department A.

Source B:
Position belongs to Department B.

The system should flag the conflict for review.

---

# 41. Abolished Positions

When a position is abolished, the historical position record should remain.

The system should preserve:

- Position
- Organization
- Effective abolition date
- Source
- Historical occupants

The position should not simply disappear from historical records.

---

# 42. Renamed Positions

If a position changes its official title, APIG should preserve the historical name.

Example:

Old:
Director of Public Works

New:
Public Works Administrator

The system should determine whether this is:

- The same position with a new name
- A new position
- An organizational restructuring

based on evidence.

---

# 43. Consolidated Positions

Two positions may be combined.

Example:

Treasurer
+

Finance Director

→

Director of Finance and Treasurer

The system should preserve the historical positions and document the consolidation.

---

# 44. Split Positions

One position may later be divided into multiple positions.

The system should preserve the original position and record the resulting positions.

This is important for historical government research.

---

# 45. Position Jurisdiction

A position should be connected to the jurisdiction in which it has authority.

Example:

County Sheriff
→ Wayne County

A regional position may connect to multiple jurisdictions.

---

# 46. Position Organization

Every position should normally connect to an organization.

Example:

Police Chief
→ Richmond Police Department

The organization may itself connect to:

City of Richmond
→ Wayne County
→ Indiana

---

# 47. Position and Physical Location

A position's physical office location may differ from its jurisdiction.

The system should distinguish:

Where the position's office is located

from:

Where the position has authority.

---

# 48. Position Search

Users should be able to search for positions directly.

Examples:

- Sheriff
- County Clerk
- Mayor
- Police Chief
- Executive Director

Search results should identify the relevant jurisdiction and organization so similarly named positions can be distinguished.

---

# 49. Position Navigation

A user viewing a position should be able to navigate to:

- Current occupant
- Historical occupants
- Organization
- Office
- Department
- Jurisdiction
- Documents
- Meetings
- News
- Sources

---

# 50. Breadcrumb Navigation

Example:

Home
→ Indiana
→ Wayne County
→ Sheriff's Office
→ Sheriff
→ Person

The user should be able to return to any prior level.

---

# 51. Person-to-Position Navigation

A user viewing a person should be able to see:

Current positions

and:

Former positions

Each position should link back to the organization and jurisdiction.

---

# 52. Position-to-Person Navigation

A user viewing a position should be able to see:

Current occupant

and:

Historical occupants

This creates bidirectional navigation.

---

# 53. Position-to-Document Navigation

Documents may establish information about a position.

Examples:

- Job descriptions
- Ordinances
- Appointment records
- Election documents
- Organizational charts
- Meeting minutes

The position page may link to relevant documents.

---

# 54. Position-to-Meeting Navigation

Meetings may document:

- Appointments
- Elections
- Resignations
- Confirmations
- Organizational changes
- Position creation
- Position abolition

The position record may link to relevant meetings.

---

# 55. Position-to-News Navigation

News may document:

- New officeholders
- Resignations
- Elections
- Appointments
- Controversies
- Organizational changes

News references should remain distinguishable from authoritative government sources.

---

# 56. AI Position Discovery

AI may discover positions by reviewing:

- Government websites
- Organizational charts
- Meeting minutes
- Statutes
- Ordinances
- Government directories
- Job descriptions
- Other permitted sources

AI discovery should produce proposed records when verification is required.

---

# 57. AI Must Not Invent Positions

AI must not assume that a position exists simply because another jurisdiction has one.

For example:

The existence of a County Auditor in County A does not establish that County B has a County Auditor.

The actual jurisdiction must be researched.

---

# 58. AI Position Matching

AI may encounter multiple names for the same position.

Example:

"Police Chief"

"Chief of Police"

These may represent the same position, but the system should verify the relationship before treating them as identical.

---

# 59. AI Organizational Inference

AI may infer a possible organizational relationship for investigation.

Example:

"Deputy Director appears to report to Director."

The system should mark the relationship as proposed until supported by evidence.

Inference is not verification.

---

# 60. Administrator Review

Administrators should be able to review:

- New positions
- Position classifications
- Current occupants
- Historical occupants
- Organizational relationships
- Reporting relationships
- Conflicting sources
- AI-generated suggestions
- Proposed changes

---

# 61. Position Audit Trail

Important changes should be auditable.

The system should eventually record:

- Previous value
- New value
- Date
- Source
- User or AI responsible
- Approval status

This is particularly important for changes to current officeholders.

---

# 62. Position Data Quality

A strong position record should establish:

- Position identity
- Organization
- Jurisdiction
- Position type
- Current or historical status
- Occupant relationship
- Dates where applicable
- Source evidence
- Verification status

---

# 63. Unknown Information

Unknown information should remain explicitly unknown.

Examples:

Current occupant:
Unknown

Term expiration:
Unknown

Appointment authority:
Unknown

Position classification:
Unknown

The system must not invent missing information.

---

# 64. Public vs Administrative View

Public users may see:

- Position
- Organization
- Current occupant
- Historical occupants
- Dates
- Sources
- Verification information

Administrative users may additionally see:

- Proposed records
- Conflicting sources
- AI confidence
- Internal notes
- Pending verification
- Change history

---

# 65. Position Record Example

Conceptual example:

POSITION

Position ID:
APIG-POSITION-000001

Official Name:
Wayne County Sheriff

Organization:
Wayne County Sheriff's Office

Jurisdiction:
Wayne County, Indiana

Type:
Elected

Current Occupant:
John Smith

Term:
2026–2030

Status:
Verified

Last Verified:
2026-08-30

Source:
Official county government directory

This example is structural only.

It does not establish that these facts are true about any real person.

---

# 66. Position Relationship Model

The position system should support relationships including:

- Belongs to organization
- Located in jurisdiction
- Has occupant
- Formerly occupied by
- Reports to
- Supervises
- Appointed by
- Elected by
- Established by
- Defined by
- Abolished by
- Renamed as
- Replaced by
- Consolidated with
- Split into
- Related to

---

# 67. Position as a Persistent Entity

The position should remain persistent through changes in personnel.

Example:

Sheriff Position
→ Person A
→ Person B
→ Person C

The position itself remains the common entity connecting the historical record.

---

# 68. Separation of Personnel and Structure

APIG should never rewrite the structure merely because personnel change.

If:

Person A
→ Sheriff

and later:

Person B
→ Sheriff

the system should update the occupant relationship.

It should not create a completely new Sheriff position merely because the person changed.

---

# 69. Historical Government Research

The position model should allow researchers to answer:

- Who held this position?
- When did they hold it?
- Who held it before them?
- Who succeeded them?
- When was the position created?
- When was it renamed?
- When was it abolished?
- Which organization controlled it?
- What authority established it?

This historical capability is a core purpose of the model.

---

# 70. Position Timeline

APIG may eventually display a position timeline.

Example:

2010
→ Position created

2010–2014
→ Person A

2014–2018
→ Person B

2018–2022
→ Person C

2022
→ Position renamed

2022–2026
→ Person D

The timeline should be based on documented events.

---

# 71. Currentness

Current position information is time-sensitive.

APIG should support periodic verification of:

- Current occupant
- Current organization
- Current title
- Current term
- Current status

---

# 72. No Assumed Current Holder

A previous officeholder should not automatically be treated as the current officeholder.

If current evidence is unavailable:

Current occupant:
Unknown / Needs Verification

---

# 73. Position-Level Evidence

The system should allow each important relationship to have its own source.

Example:

Position exists
→ Source A

Person holds position
→ Source B

Term ends
→ Source C

Position renamed
→ Source D

This avoids treating one source as proof of every fact.

---

# 74. AI Tasking

When an AI receives a task involving a position, it should identify the task type.

Examples:

"Who is the current sheriff?"

"Who held the sheriff position in 2018?"

"Who appoints the planning commission?"

"When was this position created?"

"What is the authority of this office?"

Different questions may require different sources.

---

# 75. Resource Selection

The AI should consult the appropriate APIG resource specification for the task.

Examples:

Person question
→ Person specification

Position question
→ Position specification

Government hierarchy question
→ Government hierarchy specification

Source question
→ Source and provenance specification

The APIG root resource document should direct the AI to the appropriate resource.

---

# 76. Core Position Principles

The position system follows these principles:

1. A position is not a person.
2. A position may exist without an occupant.
3. A person may hold multiple positions.
4. A position may have multiple historical occupants.
5. Current and historical occupants must be distinguishable.
6. Vacant and unknown are different states.
7. Position structure must be evidence-based.
8. AI may discover positions but must not invent them.
9. Historical position structures should be preserved.
10. Significant position facts should be traceable to sources.

---

# 77. Summary

APIG represents offices and positions as persistent entities within the governmental and organizational hierarchy.

The fundamental structure is:

JURISDICTION
→ ORGANIZATION
→ OFFICE
→ POSITION
→ PERSON

The position remains stable while people move through it.

APIG should support:

- Elected positions
- Appointed positions
- Employment positions
- Board positions
- Commission positions
- Acting positions
- Interim positions
- Vacancies
- Historical occupants
- Position creation
- Position abolition
- Position renaming
- Position consolidation
- Position splitting
- Reporting relationships
- Authority
- Source evidence
- Verification
- Historical timelines
- AI discovery
- Administrative review

The system must never invent a position or assume a person currently occupies a position without sufficient evidence.

---

# 78. Relationship to Other Specifications

This specification defines offices and positions.

Related specifications should define:

- Government and jurisdiction hierarchy
- Person identity
- Organizations
- Sources and provenance
- Documents
- Meetings
- News
- Search
- Database schema
- Website interface
- AI operations
- Privacy and security

Those specifications should remain consistent with this position model unless formally revised.

---

# 79. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-05