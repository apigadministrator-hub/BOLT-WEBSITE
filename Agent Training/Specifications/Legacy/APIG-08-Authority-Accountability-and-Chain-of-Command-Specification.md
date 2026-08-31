# APIG-08 — Authority, Accountability, and Chain-of-Command Specification

## Status

Active

## Purpose

This specification defines how APIG represents authority, appointment power, supervision, oversight, reporting relationships, accountability relationships, and chains of command.

Authority is a first-class component of the APIG information architecture.

APIG must allow users and AI systems to navigate authority relationships:

- Upward
- Downward
- Laterally where appropriate
- Across organizational boundaries where legally or administratively appropriate

The system must distinguish authority from organizational membership, physical location, employment, and personal responsibility.

---

# 1. Core Principle

APIG must represent not only:

WHO
→ belongs to
→ WHAT organization

but also:

WHO
→ has authority over
→ WHOM

and:

WHAT POSITION
→ possesses
→ WHAT AUTHORITY

and:

WHAT AUTHORITY
→ applies to
→ WHAT ORGANIZATION, POSITION, PERSON, OR JURISDICTION

---

# 2. Authority Is Not a Single Relationship

APIG must not represent all authority using one generic "reports to" relationship.

Different forms of authority have different meanings.

At minimum, APIG should support:

- Supervisory authority
- Appointment authority
- Removal authority
- Governing authority
- Oversight authority
- Reporting authority
- Instructional authority
- Delegated authority
- Jurisdictional authority
- Administrative authority
- Regulatory authority
- Legal authority
- Financial authority
- Approval authority

Additional authority types may be added as APIG develops.

---

# 3. Authority Belongs to Positions as Well as People

Where possible, authority should be attached to the position or organizational role rather than permanently to the individual occupying it.

Example:

County Board Chair
→ has appointment authority over
→ Housing Authority Commissioners

When the Chair changes, the authority relationship may continue because the position remains.

The person occupying the position is a separate entity.

---

# 4. Person-to-Authority Relationship

A person may exercise authority because they occupy a position.

Example:

Person A
→ occupies
→ County Board Chair

County Board Chair
→ appoints
→ Housing Authority Commissioners

The authority belongs primarily to the position.

The person inherits the authority through occupying that position.

---

# 5. Position-to-Position Authority

APIG should support direct authority relationships between positions.

Example:

Executive Director
→ supervises
→ Maintenance Staff Position

This allows the chain of command to remain stable when individual employees change.

---

# 6. Person-to-Person Authority

APIG may display the resulting person-to-person relationship.

Example:

Person A
→ Executive Director
→ supervises
→ Person B
→ Maintenance Employee

This relationship should be derived from the underlying position and organizational structure whenever possible.

---

# 7. Organization-to-Organization Authority

Organizations may possess authority over other organizations.

Examples:

County Board
→ appoints
→ Housing Authority Board

State Agency
→ regulates
→ Local Agency

Government Department
→ oversees
→ Division

The specific authority type must be identified.

---

# 8. Jurisdictional Authority

Jurisdictional authority describes where legal governmental authority applies.

Example:

County Government
→ jurisdiction over
→ County

Jurisdictional authority must remain distinct from organizational supervision.

---

# 9. Appointment Authority

Appointment authority identifies who has the power to appoint an individual or board to a position.

Example:

County Board Chair
→ appointing authority
→ Housing Authority Commissioners

The system should record:

- Appointing authority
- Appointed position
- Appointment type
- Effective date
- Source
- Verification status

---

# 10. Removal Authority

Where documented, APIG may represent authority to remove a person from a position.

Example:

Authority
→ removal authority
→ Position

Removal authority must not be assumed merely because someone has appointment authority.

The actual governing rules should establish the relationship.

---

# 11. Supervisory Authority

Supervisory authority identifies the formal chain of command.

Example:

Executive Director
→ directly supervises
→ Maintenance Employee

A supervisor may be responsible for:

- Directing work
- Evaluating performance
- Addressing workplace concerns
- Enforcing organizational policies
- Taking or recommending personnel action

The exact powers depend on the organization.

---

# 12. Direct Supervisor

APIG should identify the immediate supervisor where documented.

Example:

Maintenance Employee
→ direct supervisor
→ Executive Director

The system should not insert intermediate supervisors merely because they provide instructions or coordinate work.

---

# 13. Instructional Authority

A person may have authority to give instructions without being the formal supervisor.

Example:

Office staff
→ provides work instruction
→ Maintenance staff

This does not automatically create:

Office staff
→ supervises
→ Maintenance staff

The system must distinguish instruction from supervision.

---

# 14. Governing Authority

A governing body may exercise authority over an organization.

Example:

Housing Authority Board
→ governs
→ Housing Authority

The governing body may establish policies, approve actions, appoint leadership, or exercise other powers according to its governing documents.

---

# 15. Oversight Authority

Oversight authority is broader than direct supervision.

Example:

Housing Authority Board
→ oversees
→ Executive Director

The Board may oversee the Executive Director without performing the Executive Director's daily supervisory functions.

---

# 16. Higher-Level Oversight

A higher authority may have oversight without being directly involved in day-to-day operations.

Example:

County Board Chair
→ appointing/oversight relationship
→ Housing Authority Board

The Chair should not automatically be represented as the direct supervisor of Housing Authority staff.

---

# 17. Reporting Authority

A person or organization may be required to report to another authority.

Example:

Executive Director
→ reports to
→ Housing Authority Board

Reporting does not necessarily mean direct supervision.

---

# 18. Delegated Authority

Authority may be delegated.

Example:

Board
→ delegates authority
→ Executive Director

Delegated authority should identify:

- Original authority
- Recipient
- Scope
- Effective period
- Conditions
- Source

---

# 19. Limits on Delegated Authority

Delegated authority may be limited.

Examples:

- Financial limit
- Geographic limit
- Subject-matter limit
- Time limit
- Approval requirement

APIG should preserve documented limitations.

---

# 20. Approval Authority

A person or organization may possess authority to approve:

- Budgets
- Contracts
- Policies
- Personnel actions
- Purchases
- Projects
- Other matters

Approval authority should be represented separately from supervision.

---

# 21. Financial Authority

Financial authority may include:

- Budget approval
- Spending authority
- Contract approval
- Purchasing authority
- Disbursement authority

The exact scope should be sourced.

---

# 22. Legal Authority

Legal authority describes authority granted by:

- Statute
- Ordinance
- Regulation
- Charter
- Resolution
- Court order
- Other legal instrument

Legal authority should be connected to the source establishing it.

---

# 23. Regulatory Authority

An agency may regulate another entity without supervising its employees.

Example:

State Agency
→ regulates
→ Local Utility

This is regulatory authority, not employment supervision.

---

# 24. Administrative Authority

Administrative authority may include authority to:

- Implement policies
- Manage operations
- Approve procedures
- Assign work
- Manage staff

The specific authority must be documented.

---

# 25. Authority Source

Every significant authority relationship should have an authoritative source where available.

Potential sources include:

- Statute
- Ordinance
- Charter
- Resolution
- Bylaws
- Policy
- Administrative rule
- Official organizational documents
- Government website
- Appointment records
- Meeting minutes

---

# 26. Authority Verification

Authority relationships should support verification states.

Possible states include:

- Verified
- Partially Verified
- Proposed
- Conflicting
- Historical
- Unknown

AI-generated authority relationships should remain distinguishable from verified relationships.

---

# 27. Effective Dates

Authority relationships may change over time.

APIG should support:

- Start date
- End date
- Effective date
- Expiration date where applicable

---

# 28. Historical Authority

Historical authority structures should remain available.

Example:

Person A
→ formerly held
→ County Board Chair

Person A's historical authority relationships may remain visible as historical relationships.

---

# 29. Authority Changes

Authority may change because of:

- New legislation
- Ordinance
- Charter amendment
- Reorganization
- Policy change
- Appointment
- Resignation
- Election
- Administrative action

Changes should be historically preserved.

---

# 30. Chain of Command

APIG must support a formal chain of command.

Example:

County Board Chair
↓ appointing/oversight authority
Housing Authority Board
↓ governing/oversight authority
Executive Director
↓ direct supervisory authority
Maintenance Staff

The exact relationship between each level must be explicitly classified.

---

# 31. Chain-of-Command Navigation

Users should be able to navigate downward from an authority.

Example:

County Board Chair
→ Housing Authority
→ Commissioners
→ Executive Director
→ Employees

Users should also be able to navigate upward.

Example:

Maintenance Employee
→ Executive Director
→ Housing Authority Board
→ County Board Chair

---

# 32. Downstream Navigation

An authority profile should provide access to relevant downstream entities.

For example:

County Board Chair
→ Housing Authority
→ Board
→ Executive Director
→ Staff

This does not mean every downstream person is directly supervised by the Chair.

The interface must display the type of relationship.

---

# 33. Upstream Navigation

A person or organization profile should identify relevant upstream authority.

Example:

Maintenance Employee
→ supervised by
→ Executive Director
→ overseen by
→ Housing Authority Board
→ appointing authority
→ County Board Chair

---

# 34. Multiple Authority Paths

A person may be subject to multiple authority relationships.

Example:

Employee
→ supervised by
→ Executive Director

Employee
→ governed by
→ Board policies

Organization
→ overseen by
→ County Board

These paths should remain distinct.

---

# 35. Authority Is Not Automatically Responsibility

Possessing authority over a person does not mean an authority figure personally caused that person's actions.

APIG must preserve this distinction.

Example:

Maintenance Employee
→ receives DUI

This does not mean:

Executive Director
→ received DUI

or:

Housing Authority Board
→ received DUI

or:

County Board Chair
→ received DUI

The event remains associated with the person who actually experienced or committed the documented conduct.

---

# 36. Downstream Accountability References

APIG may connect a documented event to relevant upstream authority relationships.

Example:

Maintenance Employee
→ documented DUI

The system may allow navigation to:

Maintenance Employee
→ direct supervisor
→ Executive Director

and:

Executive Director
→ governing authority
→ Housing Authority Board

and:

Housing Authority Board
→ appointing authority
→ County Board Chair

These are accountability or oversight relationships.

They are not accusations against the upstream individuals.

---

# 37. Event Propagation Rules

Events must not automatically propagate as allegations.

A downstream event may generate:

- Relevant oversight reference
- Personnel-management reference
- Organizational concern
- Audit/review reference
- News reference
- Meeting reference

It must not automatically generate:

- Misconduct allegation against supervisor
- Misconduct allegation against board
- Misconduct allegation against appointing authority
- Personal liability
- Legal responsibility

Those require separate evidence.

---

# 38. Event Relevance

The relevance of a downstream event may differ by authority level.

Example:

Maintenance Employee DUI
→ High personnel relevance
→ Executive Director

Maintenance Employee DUI
→ Organizational oversight relevance
→ Housing Authority Board

Maintenance Employee DUI
→ Higher-level appointment/oversight relevance
→ County Board Chair

The system should not imply that these levels have identical responsibilities.

---

# 39. Direct vs Indirect Accountability

APIG should distinguish:

Direct accountability

from:

Indirect or institutional accountability.

Example:

Executive Director
→ direct personnel responsibility

Board
→ organizational oversight

County Board Chair
→ appointment authority

These relationships should remain distinct.

---

# 40. No Automatic Guilt or Liability

APIG must never infer guilt, liability, negligence, or wrongdoing solely from an authority relationship.

The existence of an authority relationship is a structural fact.

Legal or ethical responsibility requires separate evidence and appropriate characterization.

---

# 41. Due Process

When displaying allegations or misconduct-related information, APIG should distinguish:

- Allegation
- Complaint
- Investigation
- Arrest
- Charge
- Conviction
- Finding
- Discipline
- Dismissal
- Exoneration
- Unknown outcome

A reported event must not automatically be represented as proven misconduct.

---

# 42. Source Attribution for Events

Events connected to authority chains must remain linked to their sources.

Example:

Maintenance Employee
→ documented event
→ Source

The upstream authority relationship is separately sourced.

The system must not combine those facts into a new unsupported claim.

---

# 43. Authority Graph

The APIG data model should support an authority graph.

Nodes may include:

- Jurisdiction
- Organization
- Agency
- Board
- Department
- Office
- Position
- Person

Edges may include:

- Appoints
- Removes
- Supervises
- Oversees
- Governs
- Reports to
- Instructs
- Regulates
- Approves
- Delegates
- Has jurisdiction over

---

# 44. Authority Graph vs Organizational Tree

The organizational tree answers:

"How is this organization structured?"

The authority graph answers:

"Who has what authority over whom?"

These are related but not identical.

APIG should preserve both.

---

# 45. Multiple Chains

A single organization may have multiple authority chains.

Example:

Personnel chain:
Executive Director
→ Staff

Governance chain:
Board
→ Executive Director

Appointment chain:
County Board Chair
→ Commissioners

Regulatory chain:
State Agency
→ Housing Authority

The interface should allow users to understand which chain they are following.

---

# 46. Chain-of-Command Display

The website should visually distinguish relationship types.

Examples:

**Direct Supervisor**

**Appointing Authority**

**Governing Authority**

**Oversight Authority**

**Reporting Authority**

**Instructional Authority**

**Regulatory Authority**

The user should not have to infer the relationship from position titles alone.

---

# 47. Authority Breadcrumbs

Example:

County Board Chair
→ Appoints
→ Housing Authority Board
→ Governs
→ Housing Authority
→ Executive Director
→ Supervises
→ Maintenance Employee

The relationship verbs should remain visible.

---

# 48. Authority Profile View

A person's profile may contain an authority section showing:

- Authority they possess
- Positions through which they possess it
- Organizations affected
- People directly supervised
- People indirectly connected through oversight
- Appointing powers
- Reporting relationships

---

# 49. Downstream Profile View

A person's profile may also show:

- Direct supervisor
- Governing body
- Appointing authority
- Oversight authority
- Relevant organizational chain

This allows users to navigate upward.

---

# 50. Organization Authority View

An organization page may show:

- Governing authority
- Appointing authority
- Executive leadership
- Supervisory structure
- Regulatory relationships
- Reporting relationships
- Downstream departments
- Downstream positions
- Downstream people

---

# 51. Position Authority View

A position page should show:

- Authority possessed
- Authority source
- Appointing authority
- Supervisory relationships
- Reporting relationships
- Organizations governed
- People supervised
- Limits on authority

---

# 52. Authority Search

Users should eventually be able to search questions such as:

"Who appoints the Housing Authority board?"

"Who supervises the Executive Director?"

"Who does the Executive Director report to?"

"Who oversees this agency?"

"Who has authority to remove this official?"

"Who is downstream from this authority?"

---

# 53. AI Authority Questions

AI should recognize authority questions.

Examples:

"Who is in charge?"

"Who reports to her?"

"Who appointed them?"

"Who can remove them?"

"Who supervises this employee?"

"Who oversees this agency?"

"Who has ultimate appointment authority?"

These questions should route to the Authority & Accountability specification.

---

# 54. AI Must Not Assume Authority

AI must not infer authority solely from:

- Job title
- Seniority
- Organizational proximity
- Political status
- Physical location
- Informal influence

Authority must be established from the organizational structure or authoritative sources.

---

# 55. Informal Influence

Informal influence is not automatically formal authority.

Examples:

- Political influence
- Personal relationships
- Seniority
- Reputation
- Community influence

These should not be represented as formal authority unless supported by evidence.

---

# 56. Authority Conflicts

If sources conflict about authority, APIG should preserve the conflict.

Example:

Source A:
County Board Chair appoints commissioners.

Source B:
County Board appoints commissioners collectively.

The system should flag the issue for review rather than silently choosing one.

---

# 57. Authority Changes

When authority changes, APIG should preserve:

- Previous authority
- New authority
- Effective date
- Source
- Reason for change where documented

---

# 58. Administrative Review

Administrators should be able to review:

- Authority relationships
- Supervisory chains
- Appointment powers
- Oversight relationships
- Delegations
- Conflicts
- AI-generated relationships
- Historical authority

---

# 59. Audit Trail

Changes to authority relationships should be auditable.

The system should eventually record:

- Previous relationship
- New relationship
- Date
- Source
- User or AI responsible
- Approval status

---

# 60. Authority Data Quality

A strong authority relationship should establish:

- Source entity
- Target entity
- Authority type
- Scope
- Effective period
- Source evidence
- Verification status

---

# 61. Unknown Authority

Unknown authority must remain unknown.

Examples:

Removal authority:
Unknown

Direct supervisor:
Unknown

Appointment authority:
Unknown

The system must not invent authority relationships.

---

# 62. Authority and Privacy

Authority navigation must not become an excuse to expose unnecessary private information.

Public professional relationships may be represented where appropriate.

Private information should remain subject to APIG privacy and security rules.

---

# 63. Authority and News

News events may be connected to the authority graph.

Example:

Employee
→ documented event
→ Organization
→ Executive Director
→ Board
→ Appointing Authority

The news record should remain attached to its actual subject.

The authority graph provides context and navigation.

---

# 64. Authority and Documents

Documents may establish authority.

Examples:

- Appointment resolution
- Organizational bylaws
- Statute
- Ordinance
- Personnel policy
- Board resolution
- Delegation document

These documents should be connected to the authority relationships they establish.

---

# 65. Authority and Meetings

Meetings may establish or change authority.

Examples:

- Appointment
- Removal
- Election of officers
- Delegation
- Policy adoption
- Organizational restructuring

Meeting records should be connected to the relevant authority relationships.

---

# 66. Authority and Government Hierarchy

Government hierarchy establishes jurisdictional and governmental structure.

This specification establishes the authority relationships operating within and between those structures.

Both systems must remain interconnected.

---

# 67. Authority and Organization Specification

The organization specification establishes organizational entities.

This specification establishes authority relationships involving those entities.

Neither specification should replace the other.

---

# 68. Authority and Person Specification

The person specification establishes people.

This specification establishes authority relationships involving people through their positions and organizational roles.

---

# 69. Authority and Position Specification

The position specification should establish:

- Position identity
- Position purpose
- Position holder
- Authority associated with the position

This specification establishes how that authority connects to other entities.

---

# 70. Authority Propagation Principle

APIG may propagate **navigation and relevance** through an authority chain.

APIG must not propagate **accusations, guilt, misconduct, or personal liability** merely because an authority relationship exists.

This distinction is fundamental.

---

# 71. Example Authority Chain

Example:

County Board Chair
↓ appointing authority
Housing Authority Commissioners
↓ governing authority
Housing Authority
↓ reporting relationship
Executive Director
↓ direct supervisory authority
Maintenance Employee

If the Maintenance Employee has a documented misconduct-related event:

Maintenance Employee
→ Event

The system may allow navigation:

Event
→ Maintenance Employee
→ Executive Director
→ Housing Authority Board
→ County Board Chair

Each relationship remains explicitly labeled.

---

# 72. Example of Non-Propagation

If the Executive Director has a documented event:

Executive Director
→ Event

The system may allow navigation upward:

Executive Director
→ Housing Authority Board
→ County Board Chair

The event must not automatically appear as an event belonging to:

- Board members
- County Board Chair
- Office staff
- Maintenance staff

The event remains associated with the Executive Director.

---

# 73. Example of Non-Supervisory Instruction

If office staff instruct maintenance staff to:

"Repair the HVAC unit."

That does not establish:

Office Staff
→ Supervisor
→ Maintenance Staff

unless the organization formally establishes that supervisory authority.

The system should preserve the instructional relationship separately.

---

# 74. Authority Chain Integrity

Every authority chain should be composed of explicit relationships.

The system should never create a chain merely because:

A is senior to B.

or:

A works in the same organization as B.

or:

A has a higher-ranking title.

---

# 75. Chain Traversal

The database and website should eventually support controlled traversal such as:

UPSTREAM

Person
→ Supervisor
→ Governing Authority
→ Appointing Authority

DOWNSTREAM

Authority
→ Organization
→ Department
→ Position
→ Person

The traversal should identify the relationship type at every step.

---

# 76. Maximum Relevance

Not every downstream entity will be equally relevant to every upstream authority.

The system should therefore distinguish:

- Direct authority
- Primary oversight
- Secondary oversight
- Appointment authority
- Institutional authority
- Indirect relevance

Where practical, relevance should be determined from the actual authority relationship.

---

# 77. No Blanket Responsibility

APIG must never use phrases such as:

"The Chair is responsible for the employee's DUI"

unless there is independent evidence establishing that exact claim.

Instead, APIG may accurately state:

"The Chair has appointment/oversight authority over the board governing the agency in which the employee works."

The wording must preserve factual distinctions.

---

# 78. Accountability Context

The purpose of the authority graph is to provide accountability context.

Users should be able to answer:

- Who supervised this person?
- Who appointed their supervisor?
- Who governs the organization?
- Who has oversight?
- Who can take action?
- Who receives reports?
- What authority exists at each level?

---

# 79. AI Resource Routing

When an AI receives a task involving:

- Chain of command
- Appointment
- Supervision
- Oversight
- Authority
- Reporting
- Delegation
- Accountability
- Downstream navigation
- Upstream navigation

it should consult this specification.

The APIG root resource document should identify this file as the authoritative resource for these questions.

---

# 80. Core Authority Principles

1. Authority is a first-class APIG relationship.
2. Authority types must be distinguished.
3. Authority generally belongs to positions or organizational roles.
4. People exercise authority through their positions.
5. Appointment authority is distinct from supervision.
6. Supervision is distinct from oversight.
7. Instruction is distinct from supervision.
8. Governance is distinct from employment.
9. Jurisdiction is distinct from organizational supervision.
10. Authority must be supported by evidence.
11. Authority may change over time.
12. Historical authority should be preserved.
13. Users must be able to navigate authority chains upward and downward.
14. Downstream events may provide relevant oversight context.
15. Downstream events must not automatically become allegations against upstream authorities.
16. Authority does not automatically establish guilt, liability, negligence, or misconduct.
17. Unknown authority must remain unknown.
18. AI must not invent authority relationships.

---

# 81. Summary

APIG's authority model connects:

JURISDICTION
→ ORGANIZATION
→ POSITION
→ PERSON

with explicit authority relationships such as:

APPOINTS
SUPERVISES
GOVERNS
OVERSEES
REPORTS TO
INSTRUCTS
REGULATES
APPROVES
DELEGATES
HAS JURISDICTION OVER

This creates a navigable authority graph.

The graph allows users to move from:

Person
→ Position
→ Supervisor
→ Governing Authority
→ Appointing Authority

and from:

Authority
→ Organization
→ Department
→ Position
→ Person

The graph also allows relevant events, documents, meetings, and news to be discovered through the authority structure without incorrectly transferring the underlying conduct from one person to another.

This is a core component of APIG's website architecture and AI operating framework.

---

# 82. Relationship to Other Specifications

This specification depends upon and connects with:

- Government and jurisdiction hierarchy
- Organization and agency specification
- Person identity and relationship specification
- Position and office specification
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

The APIG root resource document should identify this specification as the primary resource for authority, accountability, supervision, appointment, oversight, and chain-of-command questions.

---

# 83. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-08