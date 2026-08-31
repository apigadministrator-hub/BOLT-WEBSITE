# APIG-11 — Entity, Relationship, and Data Model Specification

## Status

Active

## Purpose

This specification defines the foundational entity and relationship model for APIG.

APIG must represent real-world people, organizations, governments, jurisdictions, positions, offices, events, documents, sources, and relationships as distinct entities.

The purpose of this specification is to prevent APIG from collapsing fundamentally different things into a single record or relationship.

---

# 1. Core Principle

APIG must distinguish:

- Entity
- Attribute
- Relationship
- Event
- Source
- Claim
- Document
- Authority
- Jurisdiction

These are related concepts but must not be treated as interchangeable.

---

# 2. Entity

An entity is a persistent object that APIG can identify independently.

Examples:

- Person
- Organization
- Government
- Agency
- Board
- Jurisdiction
- Position
- Office
- Document
- Source
- Event

---

# 3. Entity Identity

Each persistent entity should have a unique internal identifier.

Example:

PERSON-000001
ORG-000001
POSITION-000001
EVENT-000001

Identifiers should remain stable even when names change.

---

# 4. Names

An entity may have:

- Official name
- Common name
- Former name
- Abbreviation
- Alias
- Display name

Historical names should be preserved where appropriate.

---

# 5. Entity vs Name

A name is an attribute of an entity.

A name change does not necessarily create a new entity.

Example:

Organization
→ Former name: ABC Housing Authority
→ Current name: XYZ Housing Authority

The organization may remain the same entity.

---

# 6. Entity Types

APIG should maintain explicit entity types.

At minimum:

- Person
- Government
- Jurisdiction
- Organization
- Agency
- Board
- Department
- Office
- Position
- Event
- Document
- Source
- Claim

Additional types may be added.

---

# 7. Person Entity

A person represents an identifiable individual.

The person entity is distinct from:

- Position
- Organization
- Employment
- Event
- Source

---

# 8. Organization Entity

An organization represents a persistent institutional entity.

Examples:

- Government agency
- Housing authority
- Corporation
- Nonprofit
- Department
- Association
- Board

---

# 9. Jurisdiction Entity

A jurisdiction represents a defined area or legal sphere of authority.

It is distinct from the organization exercising authority within that jurisdiction.

---

# 10. Position Entity

A position represents a persistent institutional role.

A position is distinct from the person occupying it.

---

# 11. Office Entity

An office represents an institutional office where that concept is useful or legally established.

An office may contain one or more positions.

---

# 12. Event Entity

An event represents something that happened or is documented as having happened.

Examples:

- Appointment
- Election
- Resignation
- Meeting action
- Arrest
- Charge
- Conviction
- Policy change
- Organizational change

---

# 13. Document Entity

A document represents a discrete documentary object.

Examples:

- Resolution
- Ordinance
- Meeting minutes
- Report
- Filing
- Policy
- Job description

---

# 14. Source Entity

A source represents the origin or publication through which information is obtained.

A document may itself be a source.

A news organization may be a source.

The source model must allow these distinctions.

---

# 15. Claim Entity

A claim represents a factual proposition that can be supported, contradicted, or qualified by sources.

---

# 16. Relationship

A relationship connects two or more entities.

Examples:

Person
→ occupies
→ Position

Position
→ belongs to
→ Organization

Organization
→ operates within
→ Jurisdiction

Position
→ reports to
→ Position

Person
→ related to
→ Person

---

# 17. Relationship Type

Every important relationship must have an explicit type.

Examples:

- Occupies
- Works for
- Supervises
- Reports to
- Appoints
- Governs
- Oversees
- Regulates
- Owns
- Operates
- Located in
- Created by
- Supported by
- Participated in
- Related to

---

# 18. Relationship Direction

Relationships should preserve direction where direction changes meaning.

Example:

Person A
→ supervises
→ Person B

is not equivalent to:

Person B
→ supervises
→ Person A

---

# 19. Relationship Symmetry

Some relationships may be symmetrical.

Example:

Person A
↔ spouse of
↔ Person B

Other relationships are directional.

Example:

Person A
→ appoints
→ Person B

The data model must preserve the distinction.

---

# 20. Relationship Attributes

A relationship may have its own attributes.

Examples:

- Start date
- End date
- Source
- Verification status
- Scope
- Authority type
- Confidence
- Effective period

A relationship is therefore not merely a text label between two records.

---

# 21. Temporal Relationships

Relationships may change over time.

Example:

Person A
→ occupies
→ Position
→ 2020–2024

Person B
→ occupies
→ Position
→ 2024–present

APIG must preserve historical relationships.

---

# 22. Relationship History

When a relationship ends, the historical relationship should normally remain available.

It should be marked:

- Historical
- Ended
- Superseded
- Inactive

rather than simply deleted.

---

# 23. Relationship Source

Important relationships should have provenance.

Example:

Person
→ occupies
→ Position

Source:
Official appointment record

---

# 24. Relationship Verification

Relationships should support verification states.

Examples:

- Verified
- Partially Verified
- Unverified
- Conflicting
- Proposed
- Historical
- Unknown

---

# 25. Relationship Conflicts

Conflicting relationships must be preserved for review.

Example:

Source A:
Person A supervises Person B.

Source B:
Person C supervises Person B.

APIG should flag the conflict rather than silently selecting one.

---

# 26. Multiple Relationships

Two entities may have multiple simultaneous relationships.

Example:

Person A
→ works for
→ Organization B

Person A
→ serves on
→ Board C

Person A
→ reports to
→ Person D

These relationships should remain distinct.

---

# 27. Relationship Context

A relationship may require context.

Example:

Person A
→ advises
→ Organization B

This does not necessarily mean:

Person A
→ supervises
→ Organization B.

Relationship semantics must remain explicit.

---

# 28. Authority Relationships

Authority relationships are a specialized class of relationships.

Examples:

- Supervises
- Appoints
- Removes
- Governs
- Oversees
- Reports to
- Delegates
- Approves
- Regulates
- Has jurisdiction over

Authority relationships should use the authority specification.

---

# 29. Organizational Relationships

Organizational relationships include:

- Parent organization
- Subsidiary
- Department
- Division
- Branch
- Affiliate
- Contractor
- Partner

These must not automatically imply authority.

---

# 30. Employment Relationships

Employment should be represented separately from organizational membership where necessary.

Example:

Person
→ employed by
→ Organization

This does not automatically establish:

Person
→ supervised by
→ Organization leader.

The actual supervisory relationship must be separately established.

---

# 31. Membership Relationships

Membership may include:

- Board membership
- Committee membership
- Organizational membership
- Association membership

Membership does not automatically establish supervisory authority.

---

# 32. Appointment Relationships

Appointment should be represented explicitly.

Example:

Authority
→ appoints
→ Person

or:

Authority
→ appoints
→ Position

The appropriate structure depends on the governing rules.

---

# 33. Occupancy Relationships

The core person-position relationship is:

Person
→ occupies
→ Position

This relationship should include effective dates.

---

# 34. Position Relationships

Positions may relate to one another.

Examples:

Position A
→ supervises
→ Position B

Position A
→ reports to
→ Position C

Position A
→ appointed by
→ Position D

---

# 35. Organization-Position Relationships

An organization may contain:

- Offices
- Departments
- Positions
- Boards

These relationships should be explicit.

---

# 36. Jurisdiction Relationships

An organization may operate within a jurisdiction.

A jurisdiction may contain:

- Governments
- Municipalities
- Agencies
- Districts
- Geographic areas

Jurisdiction must not be confused with organization.

---

# 37. Event Relationships

Events should connect to their actual subjects.

Example:

Person
→ involved in
→ Event

Organization
→ affected by
→ Event

Position
→ changed by
→ Event

---

# 38. Event Participants

An event may have multiple participants.

Each participant relationship should identify the person's role where appropriate.

Examples:

- Subject
- Victim
- Defendant
- Plaintiff
- Official
- Witness
- Speaker
- Appointee
- Decision-maker

---

# 39. Event Subject

The system must identify the actual subject of an event whenever possible.

This is particularly important for allegations, misconduct, legal matters, and disciplinary events.

---

# 40. Event Attribution

APIG must not automatically attribute an event to everyone connected to the subject.

Example:

Employee
→ misconduct event

does not automatically create:

Supervisor
→ misconduct event

Board
→ misconduct event

Appointing Authority
→ misconduct event

---

# 41. Event Context Through Authority

An event may be navigable through the authority structure.

Example:

Employee
→ Event

Employee
→ supervised by
→ Executive Director

Executive Director
→ overseen by
→ Board

Board
→ appointed by
→ County Authority

The event remains associated with the employee.

The authority relationships provide context.

---

# 42. Document Relationships

Documents may:

- Establish
- Describe
- Modify
- Contradict
- Support
- Reference
- Supersede

entities or relationships.

---

# 43. Source Relationships

Sources may:

- Support claims
- Contradict claims
- Establish relationships
- Describe events
- Provide context
- Supersede earlier sources

---

# 44. Claim Relationships

Claims may:

- Describe entities
- Describe events
- Establish relationships
- Be supported by sources
- Be contradicted by sources
- Be superseded by later information

---

# 45. Entity Merging

Two records should only be merged when evidence establishes that they represent the same entity.

AI must not merge records solely because names appear similar.

---

# 46. Entity Splitting

An entity may need to be split when a single record incorrectly combines distinct entities.

Examples:

- Two people with the same name
- Two organizations with similar names
- Two positions with identical titles

---

# 47. Identity Resolution

Identity resolution should use multiple attributes where available.

Examples:

Person:

- Name
- Date of birth where legally appropriate
- Position
- Organization
- Geographic association
- Official identifier

Identity resolution must comply with privacy rules.

---

# 48. Ambiguous Identity

If identity cannot be reliably resolved, APIG should preserve ambiguity.

Example:

John Smith
→ possible match
→ Person A

rather than incorrectly asserting:

John Smith
→ Person A

---

# 49. Entity Aliases

Aliases may be stored.

Examples:

- Former organizational names
- Acronyms
- Nicknames
- Alternate spellings

Aliases should not automatically create separate entities.

---

# 50. Entity Lifecycle

Entities may have statuses:

- Active
- Inactive
- Historical
- Dissolved
- Merged
- Split
- Unknown

---

# 51. Entity Creation

Entities may be created from:

- Government records
- Official documents
- Public databases
- Reliable reporting
- Verified submissions

AI may propose entities, but proposals should remain distinguishable until verified.

---

# 52. Entity Deletion

Historical entities should not be deleted merely because they are no longer active.

Where possible, mark them inactive or historical.

---

# 53. Relationship Deletion

Historical relationships should generally be preserved.

If a relationship was entered incorrectly, the correction should be auditable.

---

# 54. Corrections

Corrections should preserve:

- Previous value
- Corrected value
- Source
- Date
- Reason
- User or AI making the correction

---

# 55. Data Provenance

Entities and relationships should maintain provenance where appropriate.

The provenance model is defined by the Source and Provenance Specification.

---

# 56. Data Confidence

APIG may maintain confidence indicators.

Confidence should describe data quality or identity certainty.

It must not be represented as legal certainty.

---

# 57. Unknown Values

Unknown information must remain explicitly unknown.

Examples:

Unknown supervisor

Unknown appointment authority

Unknown position holder

Unknown event outcome

The system must not fill gaps with assumptions.

---

# 58. Derived Relationships

Some relationships may be derived from other verified relationships.

Example:

Person
→ occupies
→ Executive Director Position

Executive Director Position
→ supervises
→ Maintenance Position

Therefore:

Person
→ supervises
→ Maintenance Position

Derived relationships should be identifiable as derived.

---

# 59. Relationship Inference

AI may suggest inferred relationships.

Inferred relationships must be distinguishable from verified relationships.

---

# 60. No Unsupported Inference

APIG must not infer relationships merely from:

- Job title
- Seniority
- Physical proximity
- Shared organization
- Shared surname
- Political affiliation
- Public reputation

---

# 61. Graph Model

The APIG data model should support graph-like traversal.

Example:

Person
→ occupies
→ Position
→ belongs to
→ Organization
→ operates within
→ Jurisdiction

and:

Person
→ event
→ Source

and:

Position
→ supervises
→ Position

---

# 62. Graph Traversal

The system should support controlled traversal:

- Upward
- Downward
- Lateral
- Historical
- Source-based
- Authority-based

Traversal should preserve relationship labels.

---

# 63. Upward Traversal

Example:

Employee
→ Supervisor
→ Executive Director
→ Board
→ Appointing Authority

---

# 64. Downward Traversal

Example:

County Board Chair
→ Housing Authority Board
→ Executive Director
→ Staff Positions
→ Staff

---

# 65. Lateral Traversal

Example:

Board Member
→ Other Board Members
→ Committees
→ Related Organizations

Lateral relationships should not automatically imply authority.

---

# 66. Historical Traversal

Users should be able to navigate relationships as they existed during a specified period.

---

# 67. Source Traversal

Users should be able to move:

Entity
→ Relationship
→ Source

and:

Source
→ Supported Claims
→ Entities

---

# 68. Event Traversal

Users should be able to move:

Person
→ Events

Organization
→ Events

Position
→ Events

Event
→ Participants

Event
→ Sources

---

# 69. Data Model and Website

The website should be built around entity relationships rather than isolated pages.

A profile should function as an entry point into the larger APIG graph.

---

# 70. Profile Navigation

A person profile may provide links to:

- Positions
- Organizations
- Supervisors
- Appointing authorities
- Subordinates where appropriate
- Events
- Documents
- Sources
- Historical relationships

---

# 71. Organization Navigation

An organization profile may provide links to:

- Jurisdiction
- Parent organization
- Departments
- Boards
- Positions
- People
- Events
- Documents
- Sources
- Authority relationships

---

# 72. Position Navigation

A position profile may provide links to:

- Current holder
- Former holders
- Supervisor
- Reports
- Appointing authority
- Governing body
- Authority sources
- Events
- Documents

---

# 73. Jurisdiction Navigation

A jurisdiction profile may provide links to:

- Government
- Agencies
- Organizations
- Geographic areas
- Officials
- Legal authority
- Sources

---

# 74. Source Navigation

A source profile may provide links to:

- Claims
- Entities
- Events
- Relationships
- Documents

---

# 75. Document Navigation

A document profile may provide links to:

- Source
- Author
- Organization
- Jurisdiction
- Events
- Claims
- Entities
- Relationships established by the document

---

# 76. AI Query Routing

AI should determine which entity and relationship types are relevant to a question.

Example:

"Who supervises this person?"

→ Person
→ Position
→ Authority relationship

"Who appointed the board?"

→ Board
→ Position
→ Appointment relationship
→ Source

"What happened?"

→ Event
→ Person/Organization
→ Source

---

# 77. AI Must Preserve Entity Boundaries

AI must not collapse:

Person
into Position

Position
into Organization

Organization
into Jurisdiction

Source
into Event

Claim
into Fact

These distinctions are foundational.

---

# 78. Data Model and Accountability

Accountability navigation depends on explicit relationships.

Example:

Event
→ Subject
→ Person
→ Occupies
→ Position
→ Supervised by
→ Position
→ Governed by
→ Board
→ Appointed by
→ Authority

Each edge must remain distinguishable.

---

# 79. Data Model and Legal Characterization

The data model must preserve the distinction between:

- Allegation
- Investigation
- Charge
- Arrest
- Conviction
- Finding
- Discipline
- Exoneration
- Unknown outcome

Relationships must not change the legal status of an event.

---

# 80. Data Model and Privacy

The existence of a relationship does not automatically authorize disclosure of every associated attribute.

Access control must operate independently of relationship existence.

---

# 81. Data Model and Security

The data model should support authorization at appropriate levels.

Examples:

- Public
- Internal
- Restricted
- Administrative
- Sensitive

Security rules are defined separately.

---

# 82. Data Model and Auditability

Changes to entities and relationships should be auditable.

The system should preserve:

- Previous value
- New value
- Date
- Source
- Actor
- Verification status

---

# 83. Data Integrity

The system should enforce:

- Unique identifiers
- Valid relationship types
- Valid entity references
- Temporal consistency
- Source references
- Referential integrity

---

# 84. Referential Integrity

A relationship should not reference a nonexistent entity.

Example:

Person A
→ occupies
→ Position B

Position B must exist as an entity.

---

# 85. Relationship Validation

The system should detect impossible or contradictory combinations where practical.

Examples:

- Person simultaneously occupying mutually exclusive positions
- Relationship ending before it begins
- Position reporting to itself
- Organization contained within itself
- Event occurring before the relevant person existed

Exceptions may exist and should be reviewable rather than silently rejected where historical or unusual circumstances apply.

---

# 86. Temporal Integrity

Dates should be validated where possible.

Examples:

Appointment date
≤ Position occupancy start

Relationship end
≥ Relationship start

Event date
within the relevant historical period

---

# 87. Entity Versioning

Where important attributes change, APIG should preserve historical versions.

---

# 88. Schema Evolution

The data model must be capable of adding:

- New entity types
- New relationship types
- New attributes
- New source types
- New event types

without destroying historical data.

---

# 89. Extensibility

APIG should favor extensible relationships rather than hard-coding every possible relationship into separate systems.

---

# 90. Relationship Ontology

APIG should maintain a controlled vocabulary of relationship types.

This prevents:

"supervises"

"boss of"

"manages"

"reports under"

from being treated as unrelated concepts when they describe the same formal relationship.

---

# 91. Relationship Semantics

Each relationship type should have a defined meaning.

Example:

SUPERVISES

Definition:
Formal direct supervisory authority over another position or person.

Example:

INSTRUCTS

Definition:
Authority or role allowing a person to provide task-level direction without necessarily establishing formal supervision.

---

# 92. Relationship Hierarchy

Relationship types may have categories.

Example:

AUTHORITY

- Supervises
- Appoints
- Governs
- Oversees
- Regulates
- Approves

ORGANIZATIONAL

- Contains
- Belongs to
- Operates
- Affiliates

PERSONNEL

- Occupies
- Employs
- Formerly occupied

PROVENANCE

- Supports
- Contradicts
- Establishes
- References

---

# 93. Relationship Discovery

AI may discover potential relationships from sources.

Discovered relationships should initially be marked:

Proposed

until verification requirements are satisfied.

---

# 94. Human Review

Important or ambiguous relationships may require human review.

Examples:

- Authority relationships
- Identity matches
- Legal relationships
- Conflicting organizational structures

---

# 95. Automated Review

AI may periodically identify:

- Missing relationships
- Conflicts
- Stale records
- Duplicate entities
- Broken relationships
- Unsupported claims

AI recommendations should remain distinguishable from verified data.

---

# 96. Master Entity Registry

APIG should maintain a canonical registry of persistent entities.

This registry should allow the system to determine whether two records refer to:

- The same person
- The same organization
- The same position
- The same jurisdiction
- The same event

This is an internal data architecture component, not a manually maintained AI resource-library index.

---

# 97. Canonical Entity IDs

Once an entity receives a canonical ID, other records should reference that ID rather than relying solely on names.

---

# 98. External Identifiers

Where appropriate, APIG may preserve external identifiers.

Examples:

- Government IDs
- Agency IDs
- Court case numbers
- Document numbers

External identifiers should not replace APIG's internal IDs.

---

# 99. Duplicate Detection

The system should identify possible duplicates.

Possible duplicates should be reviewed before merging.

---

# 100. Entity Relationship Summary

The APIG model can be summarized as:

PERSON
→ OCCUPIES
→ POSITION
→ BELONGS TO
→ ORGANIZATION
→ OPERATES WITHIN
→ JURISDICTION

and:

POSITION
→ SUPERVISES
→ POSITION

POSITION
→ APPOINTED BY
→ AUTHORITY

ENTITY
→ PARTICIPATES IN
→ EVENT

CLAIM
→ SUPPORTED BY
→ SOURCE

DOCUMENT
→ ESTABLISHES
→ RELATIONSHIP

---

# 101. Core Data Principles

1. Entities must have persistent identities.
2. Persons must remain distinct from positions.
3. Positions must remain distinct from organizations.
4. Organizations must remain distinct from jurisdictions.
5. Events must remain distinct from sources reporting them.
6. Claims must remain distinct from interpretations.
7. Relationships must have explicit types.
8. Direction must be preserved where meaningful.
9. Historical relationships must be preserved.
10. Important relationships should have provenance.
11. Unknown information must remain unknown.
12. AI-generated relationships must be distinguishable from verified relationships.
13. Authority relationships must be explicitly classified.
14. Events must not automatically propagate through authority chains.
15. Entity merging requires evidence.
16. Data corrections must be auditable.
17. The website should support graph-based navigation.
18. The data model must be extensible.
19. The system should maintain canonical entity identities.
20. The data model is the foundation for APIG's website, AI, search, and accountability systems.

---

# 102. Summary

APIG is fundamentally a structured network of entities and relationships.

The core architecture is:

ENTITY
→ RELATIONSHIP
→ ENTITY

with supporting:

CLAIM
→ SOURCE

and:

EVENT
→ SUBJECT
→ SOURCE

and:

PERSON
→ POSITION
→ ORGANIZATION
→ JURISDICTION

and:

AUTHORITY
→ APPOINTMENT
→ SUPERVISION
→ GOVERNANCE
→ OVERSIGHT

The website should expose this structure through navigable profiles and relationship paths.

The AI should use the same structure when answering questions, performing research, evaluating records, or carrying out system tasks.

The model must preserve factual boundaries so that relationships provide context without creating unsupported claims.

---

# 103. Relationship to Other Specifications

This specification connects directly with:

- Government and jurisdiction hierarchy
- Organization and agency specification
- Person identity and relationship specification
- Authority, accountability, and chain-of-command specification
- Position and office specification
- Source and provenance specification
- Event specification
- Document specification
- Meeting specification
- News specification
- User account specification
- Authentication and authorization specification
- Database specification
- Website interface specification
- AI operations specification
- Privacy and security specification

The APIG root resource document should identify this specification as the primary resource for questions concerning entities, relationships, identifiers, graph traversal, canonical records, relationship types, entity resolution, and the underlying APIG data model.

---

# 104. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-11