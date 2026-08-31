# APIG-09 — Position and Office Specification

## Status

Active

## Purpose

This specification defines how APIG represents governmental, organizational, administrative, and other formal positions or offices.

A position is a structural entity that may be occupied by one or more people over time.

The central principle is:

PERSON ≠ POSITION

A person occupies a position.

The position exists independently of the person currently occupying it.

---

# 1. Position as a Persistent Entity

A position should have a stable identity independent of its current occupant.

Example:

Housing Authority Executive Director Position

may be occupied by:

Person A
→ 2020–2024

Person B
→ 2024–present

The position remains the same structural entity unless the position itself is created, abolished, or materially changed.

---

# 2. Office vs Position

APIG should distinguish between:

- Office
- Position
- Person
- Organization

An office may represent the institutional role.

A position may represent a specific seat or role within that office.

A person occupies the position.

---

# 3. Position Identity

A position record may contain:

- Position ID
- Official title
- Common title
- Organization
- Department
- Office
- Jurisdiction
- Position type
- Status
- Authority
- Source
- Verification status

---

# 4. Official Title

The official title should be preserved when available.

Examples:

- Executive Director
- County Commissioner
- Sheriff
- Clerk
- Board Chair
- Director of Public Works

APIG should preserve source terminology.

---

# 5. Common or Display Title

A simplified display title may be used when appropriate.

The official title should remain available as the authoritative name.

---

# 6. Position ID

Every persistent position should have a unique internal Position ID.

The ID must not depend solely on the title.

Two organizations may both have:

Executive Director

These are different positions if they belong to different organizational entities.

---

# 7. Position and Organization

A position normally belongs to an organization, agency, board, department, or office.

Example:

Executive Director Position
→ belongs to
→ Housing Authority

The organization relationship should be explicit.

---

# 8. Position and Jurisdiction

A position may operate within a jurisdiction.

Example:

County Commissioner
→ associated with
→ County

This does not mean every employee of a county organization is necessarily an elected county official.

Jurisdictional relationships must be separately defined.

---

# 9. Position Holder

A position may have:

- Current holder
- Former holder
- Acting holder
- Interim holder
- Multiple holders where legally or structurally appropriate
- No current holder

The system must support vacant positions.

---

# 10. Current Holder

A current holder relationship should include:

- Person
- Position
- Start date where known
- Source
- Verification status

---

# 11. Former Holder

Historical holders should remain connected to the position.

Example:

Position
→ Formerly held by
→ Person A

This relationship should include dates where available.

---

# 12. Acting Holder

Acting or interim occupants must be distinguishable from permanent occupants.

Possible statuses:

- Permanent
- Acting
- Interim
- Temporary
- Unknown

---

# 13. Vacancy

A position may be vacant.

Vacancy should not be represented by inventing an occupant.

Example:

Executive Director
→ Current holder: Vacant

---

# 14. Multiple Occupants

Some positions may legally or structurally have multiple occupants.

Examples may include:

- Board seats
- Commissioner positions
- Multi-member bodies
- Co-director positions

The position model must support this where appropriate.

---

# 15. Position Creation

A position may be created by:

- Statute
- Ordinance
- Charter
- Resolution
- Board action
- Administrative action
- Other authoritative instrument

The creating source should be recorded.

---

# 16. Position Abolition

A position may be abolished.

The historical position record should remain.

The position should be marked inactive rather than deleted where historical records depend on it.

---

# 17. Position Modification

A position may change over time.

Changes may include:

- Title
- Authority
- Duties
- Reporting relationship
- Appointment method
- Compensation structure where relevant
- Organizational placement

Historical versions should be preserved where practical.

---

# 18. Position Authority

Authority should be associated with the position where possible.

Examples:

County Board Chair
→ possesses appointment authority

Executive Director
→ possesses supervisory authority

Board Commissioner
→ possesses governing authority

The individual occupying the position exercises that authority by virtue of the position.

---

# 19. Position Authority Source

Authority associated with a position should be traceable to its source.

Potential sources include:

- Statute
- Ordinance
- Charter
- Bylaws
- Resolution
- Policy
- Administrative rule
- Official organizational documentation

---

# 20. Appointment Authority

A position may have an appointing authority.

Example:

County Board Chair
→ appoints
→ Housing Authority Commissioner Position

The relationship should be represented explicitly.

---

# 21. Removal Authority

A position may have authority to remove another position holder where legally or administratively established.

Removal authority must not be inferred solely from appointment authority.

---

# 22. Supervisory Authority

A position may supervise another position.

Example:

Executive Director Position
→ directly supervises
→ Maintenance Staff Position

This is the formal supervisory relationship.

---

# 23. Instructional Relationships

A position may provide instructions without formally supervising another position.

Example:

Office Staff Position
→ instructs regarding a task
→ Maintenance Staff Position

This does not establish:

Office Staff Position
→ supervises
→ Maintenance Staff Position

unless formal authority establishes that relationship.

---

# 24. Reporting Relationship

A position may report to another position.

Example:

Executive Director
→ reports to
→ Housing Authority Board

Reporting is distinct from supervision.

---

# 25. Governing Relationship

A governing body or position may govern an organization or another position.

Example:

Housing Authority Board
→ governs
→ Housing Authority

The exact scope should be sourced.

---

# 26. Oversight Relationship

A position or body may have oversight authority without directly supervising the affected person.

Example:

Housing Authority Board
→ oversees
→ Executive Director

Oversight should not automatically be represented as direct supervision.

---

# 27. Delegated Authority

Authority belonging to a position may be delegated.

Example:

Board
→ delegates authority
→ Executive Director

The delegation should identify:

- Source authority
- Recipient
- Scope
- Conditions
- Effective dates
- Source

---

# 28. Authority Limits

Position authority may have limitations.

Examples:

- Monetary limits
- Geographic limits
- Subject-matter limits
- Approval requirements
- Time limits
- Statutory restrictions

These should be preserved when documented.

---

# 29. Position Responsibilities

A position may have defined responsibilities.

Examples:

Executive Director:

- Manage operations
- Supervise staff
- Implement board policies

Responsibilities should be distinguished from actual authority.

A person being expected to perform a task does not automatically establish legal authority to perform every related action.

---

# 30. Position Duties

Duties describe expected functions.

Duties may come from:

- Job descriptions
- Statutes
- Ordinances
- Policies
- Contracts
- Bylaws
- Official organizational documents

---

# 31. Authority vs Duty

APIG must distinguish:

Duty:
"What this position is expected to do."

Authority:
"What this position has the power to do."

Responsibility:
"What this position is accountable for."

These concepts may overlap but are not identical.

---

# 32. Position Accountability

A position may have accountability relationships.

Example:

Executive Director
→ accountable to
→ Housing Authority Board

Accountability should identify the nature of the relationship.

---

# 33. Position Succession

When a person leaves a position and another person takes over, APIG should preserve the succession history.

Example:

Executive Director Position

Person A
→ 2020–2024

Person B
→ 2024–present

---

# 34. Position Timeline

A position timeline may include:

- Creation
- Title changes
- Authority changes
- Organizational changes
- Occupants
- Vacancies
- Abolition

This creates a historical record of the position itself.

---

# 35. Position Events

Events may be associated with positions.

Examples:

- Appointment
- Election
- Resignation
- Removal
- Vacancy
- Reorganization
- Authority change

Events should remain distinct from the people involved.

---

# 36. Person Event vs Position Event

If a person resigns:

Person
→ resignation event

The position may simultaneously have:

Position
→ vacancy event

These are related but distinct records.

---

# 37. Position and Documents

Documents may establish or describe positions.

Examples:

- Job description
- Statute
- Ordinance
- Resolution
- Bylaws
- Appointment document
- Personnel policy

The document should be linked to the position.

---

# 38. Position and Meetings

Meetings may:

- Establish positions
- Fill positions
- Remove occupants
- Change authority
- Modify duties
- Modify organizational structure

Meeting records should be linked to the relevant position or event.

---

# 39. Position and News

News may reference:

- Position
- Position holder
- Appointment
- Resignation
- Controversy
- Organizational changes

News should identify the actual subject.

---

# 40. Position and Authority Graph

Positions are nodes within the APIG authority graph.

Example:

County Board Chair Position
↓ appoints
Housing Authority Commissioner Position
↓ governs
Housing Authority
↓ employs
Executive Director Position
↓ supervises
Maintenance Staff Position

The relationship type must remain explicit.

---

# 41. Authority Inheritance Through Occupancy

When a person occupies a position, the person may exercise the authority associated with that position.

Example:

Person A
→ occupies
→ Executive Director Position

Executive Director Position
→ supervises
→ Maintenance Staff Position

Therefore:

Person A
→ supervises
→ Maintenance Staff

The person-to-person relationship should be derived from the position structure where possible.

---

# 42. End of Authority

When a person leaves a position, their authority through that position ends unless another authority relationship exists.

Example:

Person A
→ formerly held
→ Executive Director

Person B
→ currently holds
→ Executive Director

Person A should not continue to appear as the current supervisor merely because they formerly occupied the position.

---

# 43. Temporary Authority

Temporary authority may exist.

Examples:

- Acting director
- Interim chair
- Temporary appointment
- Emergency delegation

Temporary authority should have effective dates and source evidence.

---

# 44. Shared Authority

Some positions or bodies may exercise authority collectively.

Examples:

- County Board
- Commission
- Board of Directors
- Council

APIG should distinguish:

Individual authority

from:

Collective authority.

---

# 45. Collective Decision-Making

A board may have authority that can only be exercised collectively.

A single board member should not automatically inherit the entire board's authority.

Example:

Board
→ collectively approves
→ policy

does not necessarily mean:

Individual Commissioner
→ independently approves
→ policy

---

# 46. Chair Authority

A chairperson may have additional authority beyond ordinary board membership.

Examples may include:

- Presiding over meetings
- Appointing committees
- Making appointments
- Signing documents
- Exercising tie-breaking authority

Only documented powers should be represented.

---

# 47. Chair vs Board Authority

APIG must distinguish:

Board authority

from:

Chair authority.

The Chair may possess powers that individual members do not.

The Chair should not automatically inherit every power of the full board.

---

# 48. Appointment Chain

The system should support chains such as:

County Board Chair Position
→ appoints
→ Housing Authority Commissioner Position
→ governs
→ Housing Authority
→ appoints/oversees
→ Executive Director Position
→ supervises
→ Staff Positions

The exact relationships must be sourced.

---

# 49. Authority Navigation

Users should be able to open a position and navigate:

UPWARD

Position
→ Supervisor
→ Governing Authority
→ Appointing Authority

DOWNWARD

Position
→ Direct Reports
→ Departments
→ Staff Positions

SIDEWAYS

Position
→ Related Positions
→ Board Members
→ Committees
→ Equivalent Positions

---

# 50. Position Profile

A position page may contain:

- Official title
- Organization
- Jurisdiction
- Current holder
- Former holders
- Duties
- Responsibilities
- Authority
- Supervisor
- Reports to
- Appointing authority
- Governing authority
- Oversight relationships
- Source documents
- Meetings
- News
- Historical timeline

---

# 51. Person-to-Position Navigation

A person profile should link to:

Current position
→ Position profile

Former position
→ Position profile

The position profile should provide the broader institutional context.

---

# 52. Organization-to-Position Navigation

An organization page should provide:

Organization
→ Offices
→ Positions
→ Current occupants

Users should be able to navigate from the organization to individual positions.

---

# 53. Position-to-Person Navigation

A position page should show:

Current holder

and:

Historical holders

where appropriate.

---

# 54. Position Search

Users should be able to search for:

- Position title
- Organization
- Jurisdiction
- Current holder
- Former holder
- Authority type

---

# 55. AI Position Questions

AI should recognize questions such as:

"Who holds this position?"

"Who supervises this position?"

"Who appoints this person?"

"What authority does this office have?"

"Who reports to this position?"

"What are the duties of this office?"

"Who previously held this position?"

"What happens when the position becomes vacant?"

These questions should route to the position and authority specifications.

---

# 56. AI Must Not Infer Authority From Titles

AI must not assume that:

Director
→ supervises everyone in the organization.

Chair
→ controls the entire organization.

Commissioner
→ acts independently of the board.

Authority must be established from authoritative sources.

---

# 57. Position Naming Collisions

Identical position titles may exist in different organizations.

Example:

Executive Director
→ Housing Authority

Executive Director
→ Community Foundation

These must remain separate positions.

---

# 58. Position Consolidation

Two position records should only be consolidated when evidence establishes that they represent the same structural position.

---

# 59. Position Split

If a position's structure changes substantially, APIG may need to create a new position record while preserving the historical record.

---

# 60. Historical Position Accuracy

Historical authority should be represented according to the rules that applied during the relevant period.

Current authority should not automatically be projected backward into historical periods.

---

# 61. Position and Legal Change

If legislation or another authoritative action changes a position's powers, APIG should preserve:

- Previous authority
- New authority
- Effective date
- Source

---

# 62. Position and Accountability Events

Events involving a position holder may be navigated through the position's authority structure.

Example:

Maintenance Employee
→ documented event

User may navigate:

Maintenance Employee
→ Executive Director
→ Housing Authority Board
→ County Board Chair

The event remains associated with the actual subject.

---

# 63. No Automatic Event Attribution

A position holder's event must not automatically become an event attributed to:

- Their supervisor
- Their governing board
- Their appointing authority
- Their organization
- Their jurisdiction

The authority chain provides context, not automatic attribution.

---

# 64. Oversight Context

Where relevant, a position profile may show downstream events within its oversight structure.

Example:

County Board Chair
→ Housing Authority
→ Staff
→ documented event

The interface may provide a link to the downstream event with its relationship context.

---

# 65. No Presumption of Misconduct

APIG must distinguish between:

- Documented event
- Allegation
- Finding
- Discipline
- Criminal charge
- Conviction
- Exoneration
- Unknown outcome

The position structure must not change the legal characterization of an event.

---

# 66. Vacancy and Authority

When a position is vacant, APIG should determine whether authority:

- Transfers automatically
- Goes to an acting official
- Goes to another position
- Becomes temporarily unavailable
- Remains with the governing body

The system must use the governing rules rather than assumptions.

---

# 67. Delegation and Vacancy

If authority is delegated during a vacancy, APIG should preserve the delegation separately from the underlying position.

---

# 68. Position Data Quality

A strong position record should establish:

- Identity
- Organization
- Jurisdiction where relevant
- Current status
- Current holder
- Historical holders
- Duties
- Authority
- Reporting structure
- Appointment structure
- Sources
- Verification status

---

# 69. Unknown Information

Unknown information must remain unknown.

Examples:

Current holder:
Unknown

Appointing authority:
Unknown

Direct supervisor:
Unknown

Authority scope:
Unknown

The system must not invent missing information.

---

# 70. Administrative Review

Administrators should be able to review:

- Position records
- Position holders
- Authority relationships
- Historical occupants
- Conflicts
- Vacancies
- AI-generated suggestions
- Source evidence

---

# 71. Audit Trail

Changes to position records should be auditable.

The system should eventually record:

- Previous value
- New value
- Date
- Source
- User or AI responsible
- Approval status

---

# 72. Core Position Principles

1. A position is distinct from the person occupying it.
2. Positions persist through changes in personnel.
3. Authority should generally attach to positions.
4. Duties are distinct from authority.
5. Accountability is distinct from authority.
6. Supervision is distinct from instruction.
7. Oversight is distinct from supervision.
8. Appointment authority is distinct from removal authority.
9. Collective authority is distinct from individual authority.
10. Chair authority is distinct from full board authority.
11. Historical authority must be preserved.
12. Vacancies must be supported.
13. Temporary authority must be represented explicitly.
14. Authority must be supported by evidence.
15. Users must be able to navigate positions through the authority graph.
16. Events involving position holders must not automatically propagate as misconduct or liability to other positions.
17. Unknown information must remain unknown.
18. AI must not infer authority merely from titles.

---

# 73. Summary

APIG treats positions as persistent structural entities within government and organizational systems.

The basic relationship is:

PERSON
→ OCCUPIES
→ POSITION

A position may have:

- Authority
- Duties
- Responsibilities
- Supervisors
- Reports
- Appointing authorities
- Governing authorities
- Oversight relationships
- Historical occupants

The position connects people to the institutional structure without confusing the individual with the office.

This allows APIG to maintain accurate historical records while supporting navigation through authority and accountability chains.

---

# 74. Relationship to Other Specifications

This specification connects directly with:

- Government and jurisdiction hierarchy
- Organization and agency specification
- Person identity and relationship specification
- Authority, accountability, and chain-of-command specification
- Source and provenance specification
- Document specification
- Meeting specification
- News specification
- User account specification
- Authentication and authorization specification
- Database specification
- Website interface specification
- AI operations specification
- Privacy and security specification

The APIG root resource document should identify this specification as the primary resource for questions concerning positions, offices, officeholders, duties, position authority, position history, vacancies, and position-based relationships.

---

# 75. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-09