# APIG-20 — Entity, Relationship, and Data Model Specification

## Status

Active

## Purpose

This specification defines how APIG represents people, organizations, positions, jurisdictions, authorities, events, records, sources, relationships, responsibilities, and other entities within the APIG system.

The fundamental principle is:

ENTITY
→ IDENTITY
→ TYPE
→ RELATIONSHIPS
→ AUTHORITY
→ ACCOUNTABILITY
→ EVENTS
→ SOURCES
→ HISTORY.

---

# 1. Core Principle

APIG must distinguish between an entity and the relationships connecting that entity to other entities.

A relationship does not automatically establish the same type of authority, responsibility, conduct, or accountability as another relationship.

---

# 2. Entity

An entity is a uniquely identifiable person, organization, governmental body, position, place, event, document, system, or other object represented by APIG.

---

# 3. Entity Identity

Each entity should have a stable internal identity.

---

# 4. Entity Identifier

Each entity should have a unique identifier where practical.

---

# 5. Entity Type

Each entity should have a defined type.

Possible types include:

- Person
- Organization
- Government
- Agency
- Board
- Position
- Office
- Jurisdiction
- Event
- Document
- Source
- System
- AI
- Resource
- Project
- Task.

---

# 6. Person

A person represents an identifiable human individual.

---

# 7. Organization

An organization represents a structured group or institution.

---

# 8. Government

A government represents a governmental authority or governmental system.

---

# 9. Agency

An agency represents an organizational body operating under an applicable authority structure.

---

# 10. Board

A board represents a governing or oversight body.

---

# 11. Position

A position represents an organizational role rather than the person currently occupying it.

---

# 12. Office

An office represents an organizational function, location, or administrative unit as appropriate.

---

# 13. Jurisdiction

A jurisdiction represents an area or authority within which specified legal or governmental authority applies.

---

# 14. Event

An event represents something that occurred, was alleged to have occurred, or was formally recorded.

---

# 15. Document

A document represents a discrete informational resource.

---

# 16. Source

A source represents the origin of information.

---

# 17. System

A system represents software, infrastructure, platforms, services, or other operational technology.

---

# 18. AI

An AI entity represents an AI model, AI service, AI agent, or other computational actor.

---

# 19. Resource

A resource represents an information, computational, financial, physical, or other usable resource.

---

# 20. Project

A project represents an organized body of work.

---

# 21. Task

A task represents a discrete requested or required action.

---

# 22. Entity Separation

APIG should avoid combining distinct entities merely because they share:

- A name
- An address
- An organization
- A position
- A jurisdiction
- A source
- A relationship.

---

# 23. Entity Resolution

APIG should determine whether records referring to similar names represent the same entity.

---

# 24. Uncertain Identity

If identity cannot be established with sufficient confidence, APIG should preserve the uncertainty.

---

# 25. Entity Merge

Entities may be merged when sufficient evidence establishes that they represent the same underlying entity.

---

# 26. Entity Split

An incorrectly merged entity must be capable of being separated into distinct entities.

---

# 27. Historical Identity

Historical identities should remain traceable where relevant.

---

# 28. Name Changes

A person's or organization's name may change without creating a new underlying entity.

---

# 29. Position Changes

A person may occupy different positions over time.

---

# 30. Organizational Changes

Organizations may change names, structures, responsibilities, or legal status over time.

---

# 31. Relationship

A relationship describes a connection between two or more entities.

---

# 32. Relationship Direction

Relationships may be directional.

For example:

PERSON
→ OCCUPIES
→ POSITION.

---

# 33. Relationship Type

Every material relationship should have a defined relationship type.

---

# 34. Authority Relationship

Authority relationships describe legally, organizationally, contractually, or otherwise established authority.

---

# 35. Supervisory Relationship

A supervisory relationship indicates actual supervisory responsibility.

---

# 36. Appointment Relationship

An appointment relationship indicates authority to appoint or select another actor for a position.

---

# 37. Governance Relationship

A governance relationship indicates participation in governing or overseeing an organization.

---

# 38. Oversight Relationship

An oversight relationship indicates responsibility to review, monitor, evaluate, or supervise an entity or function according to the applicable authority.

---

# 39. Accountability Relationship

An accountability relationship indicates that an actor or authority has defined responsibility concerning another entity, function, or outcome.

---

# 40. Reporting Relationship

A reporting relationship indicates that one position or actor reports to another.

---

# 41. Membership Relationship

A membership relationship indicates participation in an organization, board, committee, or other body.

---

# 42. Employment Relationship

An employment relationship indicates an employment connection.

---

# 43. Contractual Relationship

A contractual relationship indicates an applicable contractual connection.

---

# 44. Ownership Relationship

An ownership relationship indicates an ownership interest where applicable.

---

# 45. Affiliation Relationship

An affiliation relationship indicates an association that does not necessarily imply authority.

---

# 46. Representation Relationship

A representation relationship indicates that one actor represents another entity or organization.

---

# 47. Delegation Relationship

A delegation relationship indicates that authority or responsibility has been delegated.

---

# 48. Delegation Limits

Delegation does not necessarily transfer all authority belonging to the delegating actor.

---

# 49. Authority Scope

Every material authority relationship should have a defined scope where practical.

---

# 50. Authority Duration

Authority relationships may have effective dates and expiration dates.

---

# 51. Effective Date

Material relationships should identify when they became effective where known.

---

# 52. End Date

Material relationships should identify when they ended where known.

---

# 53. Historical Relationships

Ended relationships should remain historically traceable when relevant.

---

# 54. Current Relationships

Current relationships should be distinguishable from historical relationships.

---

# 55. Proposed Relationships

Proposed relationships should be distinguishable from established relationships.

---

# 56. Relationship Evidence

Material relationships should be supported by appropriate source evidence.

---

# 57. Relationship Provenance

APIG should preserve the source establishing an important relationship.

---

# 58. Relationship Verification

Material relationships should have an appropriate verification status.

---

# 59. Relationship Uncertainty

Uncertain relationships should not be represented as established facts.

---

# 60. Relationship Attributes

Relationships may include:

- Source
- Authority
- Scope
- Effective date
- End date
- Verification status
- Confidence
- Jurisdiction
- Conditions.

---

# 61. Chain of Command

APIG should represent actual chains of command.

---

# 62. Chain of Command Direction

A chain of command should identify:

UPSTREAM AUTHORITY
→ SUPERVISOR
→ SUBORDINATE
→ FUNCTION.

---

# 63. No Assumed Supervision

APIG must not infer supervisory authority solely from organizational proximity or job title.

---

# 64. Staff Relationships

Staff members may work together without one staff member supervising another.

---

# 65. Instruction Does Not Equal Supervision

Giving or receiving instructions does not automatically establish a supervisory relationship.

---

# 66. Executive Director

Where the governing structure establishes an executive director as the supervisor of staff, the data model should represent that relationship explicitly.

---

# 67. Board Oversight

Board members may have governance or oversight relationships without being direct supervisors of individual staff members.

---

# 68. Appointing Authority

An appointing authority may have authority to appoint members of another governing body without directly supervising every person downstream from that body.

---

# 69. Oversight Chain

APIG may represent an oversight chain such as:

APPOINTING AUTHORITY
→ GOVERNING BOARD
→ EXECUTIVE DIRECTOR
→ STAFF.

---

# 70. Oversight Is Not Direct Conduct

An event involving a downstream person does not automatically become conduct of every upstream authority.

---

# 71. Downstream Accountability

A downstream event may create an accountability or oversight relationship to upstream authorities when the governing structure makes such evaluation relevant.

---

# 72. No Automatic Guilt

Upstream accountability must never be represented as proof that an upstream person personally committed the downstream conduct.

---

# 73. Direct Conduct Link

An event involving personal conduct should link directly to the person who engaged in that conduct.

---

# 74. Oversight Link

The same event may have separate links to relevant supervisors, governing bodies, or authorities for oversight purposes.

---

# 75. Downstream Navigation

APIG should allow authorized users to navigate from an upstream authority through relevant organizational relationships to downstream entities and records.

---

# 76. Upstream Navigation

APIG should allow authorized users to navigate from a downstream entity toward relevant upstream authorities.

---

# 77. Relationship-Aware Navigation

Navigation should identify the relationship type at each step.

---

# 78. Example

A user viewing an appointing authority may be able to navigate:

COUNTY BOARD CHAIRPERSON
→ APPOINTMENT AUTHORITY
→ HOUSING AUTHORITY BOARD
→ GOVERNANCE
→ EXECUTIVE DIRECTOR
→ SUPERVISION
→ STAFF.

---

# 79. Event Navigation

Where appropriate, users may then navigate from a downstream staff member to relevant documented events.

---

# 80. Accountability Navigation

The interface should distinguish:

DIRECT CONDUCT
from
SUPERVISORY ACCOUNTABILITY
from
GOVERNANCE OVERSIGHT
from
APPOINTMENT AUTHORITY.

---

# 81. Relationship Semantics

The meaning of every relationship must be explicit.

---

# 82. No Generic Relationship

APIG should avoid using an undefined generic relationship when a more precise relationship can be established.

---

# 83. Multiple Relationships

Two entities may have multiple simultaneous relationships.

---

# 84. Relationship Independence

One relationship should not automatically imply another.

For example:

APPOINTS
does not automatically mean
SUPERVISES.

---

# 85. Relationship Inheritance

Authority should not automatically propagate through every downstream entity.

---

# 86. Explicit Propagation

Any propagation of accountability, authority, or responsibility must follow defined rules.

---

# 87. Authority Propagation

Authority propagation should occur only when supported by the governing structure.

---

# 88. Accountability Propagation

Accountability propagation should identify the type and basis of accountability.

---

# 89. Conduct Propagation

Personal conduct must never be automatically propagated upstream.

---

# 90. Event Propagation

Events may be visible through relevant relationship paths without changing the identity of the actor involved.

---

# 91. Relationship Graph

APIG may represent entities and relationships as a graph.

---

# 92. Graph Nodes

Entities may function as graph nodes.

---

# 93. Graph Edges

Relationships may function as graph edges.

---

# 94. Edge Attributes

Graph edges should preserve relationship attributes where necessary.

---

# 95. Temporal Graph

The relationship graph should support historical changes.

---

# 96. Jurisdictional Graph

Entities may be connected to applicable jurisdictions.

---

# 97. Organizational Graph

Organizations may contain positions, offices, departments, boards, and personnel relationships.

---

# 98. Authority Graph

Authority relationships may be represented separately from organizational membership.

---

# 99. Accountability Graph

Accountability relationships may be represented separately from direct supervision.

---

# 100. Source Graph

Sources may be connected to the entities and relationships they establish.

---

# 101. Evidence Graph

Evidence may be connected to claims, events, and relationships.

---

# 102. Event Graph

Events may connect:

ACTOR
→ EVENT
→ ORGANIZATION
→ JURISDICTION
→ SOURCE
→ ACCOUNTABILITY RELATIONSHIPS.

---

# 103. Person Profile

A person profile may contain:

- Identity
- Current positions
- Historical positions
- Organizations
- Authority relationships
- Accountability relationships
- Documented events
- Sources
- Relevant history.

---

# 104. Organization Profile

An organization profile may contain:

- Identity
- Jurisdiction
- Governing authority
- Board
- Officers
- Staff
- Positions
- Policies
- Events
- Sources
- Historical structure.

---

# 105. Position Profile

A position profile may contain:

- Position name
- Organization
- Authority
- Responsibilities
- Supervisor
- Subordinates
- Appointment method
- Jurisdiction
- Current occupant
- Historical occupants.

---

# 106. Jurisdiction Profile

A jurisdiction profile may contain:

- Name
- Type
- Geographic scope
- Legal authority
- Governmental authority
- Parent jurisdiction
- Subordinate jurisdictions
- Relevant sources.

---

# 107. Event Profile

An event profile may contain:

- Event type
- Date
- Location
- Actors
- Organizations
- Claims
- Evidence
- Sources
- Verification status
- Accountability relationships.

---

# 108. Source Profile

A source profile may contain:

- Source identity
- Source type
- Publisher
- Date
- Location
- Provenance
- Verification status
- Related claims
- Related entities.

---

# 109. AI Profile

An AI profile may contain:

- Model identity
- Provider
- Capabilities
- Authorized functions
- Restrictions
- Resource access
- Current assignment
- Operational history.

---

# 110. Task Profile

A task profile may contain:

- Task identity
- Requester
- Authority
- Priority
- Assigned AI
- Required resources
- Status
- Inputs
- Outputs
- Verification
- Audit history.

---

# 111. Entity History

Material changes to entities should remain historically traceable where practical.

---

# 112. Relationship History

Material relationship changes should remain historically traceable where practical.

---

# 113. Position Occupancy

The system should distinguish the position from the person occupying the position.

---

# 114. Vacancy

A position may exist without a current occupant.

---

# 115. Acting Positions

A person may temporarily occupy or act in a position.

---

# 116. Temporary Authority

Temporary authority should be represented with appropriate scope and duration.

---

# 117. Delegated Authority

Delegated authority should identify:

- Delegator
- Delegate
- Scope
- Conditions
- Effective period
- Source.

---

# 118. Revoked Authority

Revoked authority should remain historically identifiable.

---

# 119. Expired Authority

Expired authority must not continue to authorize current actions.

---

# 120. Conflicting Authorities

Where multiple authorities appear to conflict, the system should preserve the conflict until appropriately resolved.

---

# 121. Authority Resolution

Authority conflicts should be resolved according to applicable law, governance, jurisdiction, and APIG authority rules.

---

# 122. Jurisdictional Conflict

Entities may be subject to multiple jurisdictions.

---

# 123. Jurisdictional Scope

A jurisdictional relationship should specify what authority it represents where necessary.

---

# 124. Cross-Jurisdictional Entities

An organization or person may have relationships with multiple jurisdictions.

---

# 125. Jurisdiction Does Not Equal Ownership

A jurisdictional relationship does not automatically establish ownership.

---

# 126. Jurisdiction Does Not Equal Supervision

Jurisdictional authority does not automatically establish organizational supervision.

---

# 127. Organization Does Not Equal Government

An organization operating within a government jurisdiction is not automatically itself a governmental entity.

---

# 128. Board Does Not Equal Staff

A governing board and its staff should remain distinct entities.

---

# 129. Staff Does Not Equal Board

Employment by an organization does not automatically establish membership on its governing board.

---

# 130. Office Does Not Equal Person

An office should remain distinct from the individual occupying it.

---

# 131. Position Does Not Equal Person

A position should remain distinct from its current occupant.

---

# 132. Event Does Not Equal Person

An event must not be treated as an attribute of a person without an explicit relationship.

---

# 133. Claim Does Not Equal Fact

Claims and verified facts must remain distinct.

---

# 134. Source Does Not Equal Fact

A source containing a statement does not automatically establish that statement as fact.

---

# 135. AI Output Does Not Equal Fact

AI output must not automatically become a verified entity attribute.

---

# 136. Attribute

An attribute is a property associated with an entity.

---

# 137. Attribute Provenance

Material attributes should have source provenance where practical.

---

# 138. Attribute History

Material changes to important attributes should be historically traceable.

---

# 139. Derived Attributes

Derived attributes should be distinguishable from directly sourced attributes.

---

# 140. Computed Relationships

Computed relationships should be distinguishable from explicitly established relationships.

---

# 141. Inference

Inferences should be identified as inferences where material.

---

# 142. No Hidden Inference

The system should not silently convert uncertain inference into established relationship data.

---

# 143. Data Normalization

Repeated information should be represented through shared entities and relationships where practical.

---

# 144. Referential Integrity

References between records should remain valid and attributable.

---

# 145. Broken References

Broken references should be detected where practical.

---

# 146. Deletion

Deleting an entity should not unnecessarily destroy historical relationships or provenance.

---

# 147. Archiving

Archived entities and relationships should remain discoverable where appropriate.

---

# 148. Privacy

Entity and relationship data remains subject to APIG privacy and security requirements.

---

# 149. Restricted Relationships

Some relationships may be restricted even when the entities themselves are public.

---

# 150. Public Relationships

Public relationships may be displayed when supported by appropriate evidence and authority.

---

# 151. Sensitive Relationships

Sensitive relationships require appropriate access controls.

---

# 152. Relationship Visibility

Visibility may differ according to:

- Public access
- Contributor access
- Administrative access
- Principal access
- System access.

---

# 153. Identity Security

Identity information must be protected according to its sensitivity.

---

# 154. Entity Impersonation

APIG must prevent unverified actors from assuming another entity's identity.

---

# 155. Identity Verification

High-impact entity associations require appropriate verification.

---

# 156. Entity Provenance

The source establishing an entity's identity should be preserved where appropriate.

---

# 157. Entity Confidence

Identity confidence may be represented separately from verification status.

---

# 158. Duplicate Prevention

APIG should reduce accidental creation of duplicate entities.

---

# 159. Duplicate Resolution

Potential duplicate entities should be reviewable.

---

# 160. Relationship Validation

Material relationships should be validated against appropriate sources.

---

# 161. Relationship Contradictions

Contradictory relationship records should be detected and preserved for resolution.

---

# 162. Relationship Effective Periods

Two apparently conflicting relationships may both be correct if they apply during different periods.

---

# 163. Organizational Succession

When a person leaves a position, the position remains distinct from the successor.

---

# 164. Historical Accountability

Historical accountability should be evaluated according to the authority relationship existing when the relevant event occurred.

---

# 165. Current Accountability

Current accountability should be evaluated according to the authority relationship currently in effect.

---

# 166. Event-Time Relationships

Where an event is evaluated, APIG should use the relevant relationships that existed at the time of the event where appropriate.

---

# 167. Retroactive Relationship Changes

A later organizational change should not automatically rewrite historical authority relationships.

---

# 168. Historical Reconstruction

APIG should support reconstruction of relevant organizational structures at a particular point in time where sufficient data exists.

---

# 169. Chain-of-Command Reconstruction

The system should be able to reconstruct relevant chains of command for historical events where practical.

---

# 170. Accountability Reconstruction

The system should be able to determine which authorities had relevant oversight responsibilities at the time of an event.

---

# 171. Navigation

The user interface should allow users to move through relationships without losing the relationship type or context.

---

# 172. Breadcrumbs

Relationship navigation may use breadcrumbs or equivalent context indicators.

---

# 173. Relationship Labels

Links should identify what the relationship means.

---

# 174. No Ambiguous Links

A link labeled only "related" should not replace a known specific relationship type.

---

# 175. Search

Users should be able to search for entities and relationships.

---

# 176. Relationship Filtering

Users should be able to filter relationships by type where appropriate.

---

# 177. Time Filtering

Users should be able to filter relationships by historical period where appropriate.

---

# 178. Jurisdiction Filtering

Users should be able to filter relationships by jurisdiction where appropriate.

---

# 179. Authority Filtering

Users should be able to identify relationships involving authority.

---

# 180. Accountability Filtering

Users should be able to identify relationships involving accountability.

---

# 181. Event Filtering

Users should be able to identify events connected to an entity through defined relationship types.

---

# 182. Source Filtering

Users should be able to identify the sources establishing relationships.

---

# 183. Evidence Filtering

Users should be able to identify supporting evidence where access is authorized.

---

# 184. AI Use

AI systems should use the entity and relationship model rather than inventing relationship meanings.

---

# 185. AI Relationship Interpretation

AI should identify the relationship type before drawing conclusions about authority or accountability.

---

# 186. AI Entity Resolution

AI may assist with entity resolution but should not silently merge uncertain entities.

---

# 187. AI Relationship Discovery

AI may identify potential relationships for review.

---

# 188. AI Relationship Verification

Material AI-discovered relationships should be verified before becoming authoritative records.

---

# 189. AI Data Migration

AI systems transferring APIG data must preserve entity identifiers and relationship semantics.

---

# 190. AI Provider Replacement

A replacement AI must be able to reconstruct the entity and relationship model from APIG's portable resources.

---

# 191. Portable Entity Model

Entity types, identifiers, relationship types, authority structures, and provenance should use portable representations where practical.

---

# 192. Resource Hierarchy

The APIG resource hierarchy should provide the specifications necessary for another AI to understand the entity and relationship model.

---

# 193. Root Resource Relationship

The APIG root resource document should identify this specification as the primary resource for entities, relationships, organizational structures, authority chains, accountability chains, profiles, graph navigation, and data modeling.

---

# 194. Core Principles

1. Entities must remain distinct from their relationships.
2. Relationships must have explicit meanings.
3. Authority relationships must not be inferred from proximity alone.
4. Appointment does not automatically mean supervision.
5. Governance does not automatically mean direct supervision.
6. Giving instructions does not automatically mean supervision.
7. Direct conduct must remain attached to the actor who performed it.
8. Oversight relationships may be linked to downstream events without assigning the conduct to upstream authorities.
9. Accountability is not the same as guilt.
10. Positions must remain distinct from the people occupying them.
11. Organizations must remain distinct from governments unless established otherwise.
12. Claims must remain distinct from facts.
13. Sources must remain distinct from facts.
14. AI output must remain distinct from verified information.
15. Historical relationships must remain historically traceable.
16. Current relationships must remain distinguishable from historical relationships.
17. Proposed relationships must remain distinguishable from established relationships.
18. Relationship provenance must be preserved.
19. Material relationships should be verifiable.
20. Uncertainty must remain explicit.
21. Entity identity must not be assumed without sufficient evidence.
22. Duplicate entities should be resolvable.
23. Relationship conflicts should be preserved until resolved.
24. Jurisdictional relationships must remain distinct from organizational supervision.
25. Accountability propagation must follow explicit rules.
26. Conduct must never automatically propagate upstream.
27. Authorized users should be able to navigate authority and accountability chains.
28. Relationship types must remain visible during navigation.
29. AI systems must preserve entity and relationship semantics.
30. The APIG data model must remain portable across AI providers and future system implementations.

---

# 195. Entity Relationship Sequence

ENTITY
→ IDENTIFY
→ CLASSIFY
→ VERIFY
→ CONNECT
→ DEFINE RELATIONSHIP
→ ESTABLISH AUTHORITY
→ ESTABLISH ACCOUNTABILITY
→ ATTACH EVENTS
→ ATTACH SOURCES
→ PRESERVE HISTORY.

---

# 196. Authority Chain Sequence

JURISDICTION
→ GOVERNING AUTHORITY
→ APPOINTING AUTHORITY
→ GOVERNING BODY
→ EXECUTIVE AUTHORITY
→ SUPERVISOR
→ SUBORDINATE
→ FUNCTION.

---

# 197. Accountability Chain Sequence

EVENT
→ DIRECT ACTOR
→ DIRECT SUPERVISOR
→ GOVERNING AUTHORITY
→ APPOINTING AUTHORITY
→ JURISDICTION.

Each connection must retain its actual relationship type.

---

# 198. Example Accountability Model

A staff member may be associated with a documented event.

The event may link to:

STAFF MEMBER
→ DIRECT CONDUCT

EXECUTIVE DIRECTOR
→ SUPERVISORY OVERSIGHT

BOARD
→ GOVERNANCE / OVERSIGHT

APPOINTING AUTHORITY
→ APPOINTMENT / GOVERNANCE OVERSIGHT

These relationships must not be collapsed into a claim that every upstream entity committed the staff member's conduct.

---

# 199. Example Navigation Model

PERSON PROFILE
→ CURRENT POSITION
→ ORGANIZATION
→ GOVERNING BODY
→ APPOINTING AUTHORITY
→ JURISDICTION.

The reverse path should also be possible where appropriate:

JURISDICTION
→ APPOINTING AUTHORITY
→ GOVERNING BODY
→ ORGANIZATION
→ EXECUTIVE DIRECTOR
→ STAFF
→ DOCUMENTED EVENTS.

---

# 200. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-20