# APIG-28 — Data Architecture and Relationships Specification

## Status

Active

## Purpose

This specification defines how APIG represents people, organizations, positions, jurisdictions, events, records, authorities, relationships, and other entities so that information can be connected and navigated without confusing one relationship with another.

The fundamental principle is:

ENTITY
→ IDENTITY
→ ATTRIBUTES
→ RELATIONSHIPS
→ AUTHORITY
→ JURISDICTION
→ EVENTS
→ RECORDS
→ NAVIGATION.

---

# 1. Core Principle

APIG should represent important information as connected entities and relationships rather than isolated documents whenever doing so improves understanding, accountability, navigation, or continuity.

---

# 2. Entity

An entity is a person, organization, position, jurisdiction, event, record, system, resource, or other identifiable object represented within APIG.

---

# 3. Entity Identity

Each material entity should have a stable identity that distinguishes it from other entities.

---

# 4. Entity Identifier

Material entities should have an identifier where practical.

---

# 5. Person

A person is an identifiable human individual.

---

# 6. Organization

An organization is an identifiable institutional or operational body.

---

# 7. Position

A position represents an organizational role or office independent of the particular person occupying it.

---

# 8. Person Versus Position

APIG must distinguish the person from the position that person occupies.

---

# 9. Position History

A person's occupancy of a position may change over time.

---

# 10. Organization History

An organization's structure may change over time.

---

# 11. Jurisdiction

A jurisdiction defines the governmental, legal, geographic, administrative, or other applicable scope of authority.

---

# 12. Authority

Authority identifies the power or responsibility applicable to an actor, position, organization, or jurisdiction.

---

# 13. Relationship

A relationship describes a meaningful connection between two or more entities.

---

# 14. Relationship Type

Relationships must identify their type where the distinction affects interpretation.

---

# 15. Direct Relationship

A direct relationship exists explicitly between two entities.

---

# 16. Indirect Relationship

An indirect relationship may be established through one or more intermediate entities.

---

# 17. Organizational Relationship

An organizational relationship connects people, positions, and organizations.

---

# 18. Supervisory Relationship

A supervisory relationship identifies who supervises whom.

---

# 19. Oversight Relationship

An oversight relationship identifies an entity that has oversight responsibility.

---

# 20. Appointment Relationship

An appointment relationship identifies authority to appoint or select another person or body.

---

# 21. Reporting Relationship

A reporting relationship identifies where an individual or position reports.

---

# 22. Advisory Relationship

An advisory relationship identifies a relationship in which one entity provides advice without necessarily exercising supervisory authority.

---

# 23. Instruction Relationship

An instruction relationship identifies authority or responsibility to provide operational instructions.

---

# 24. Instruction Does Not Equal Supervision

The ability to give an instruction does not automatically establish a supervisory relationship.

---

# 25. Oversight Does Not Equal Supervision

Oversight authority does not automatically establish direct supervisory authority.

---

# 26. Appointment Does Not Equal Supervision

Appointment authority does not automatically establish direct supervision.

---

# 27. Governance Relationship

A governance relationship identifies formal organizational or institutional authority.

---

# 28. Jurisdictional Relationship

A jurisdictional relationship identifies the jurisdiction applicable to an entity, event, or record.

---

# 29. Membership Relationship

A membership relationship identifies participation in an organization, board, committee, or other body.

---

# 30. Employment Relationship

An employment relationship identifies an individual's employment relationship with an organization.

---

# 31. Contractual Relationship

A contractual relationship identifies an agreement between parties.

---

# 32. Ownership Relationship

An ownership relationship identifies an ownership interest where applicable.

---

# 33. Custodial Relationship

A custodial relationship identifies responsibility for maintaining a resource or record.

---

# 34. Record Relationship

A record relationship connects a record to the entities it concerns.

---

# 35. Event Relationship

An event relationship connects an event to relevant people, organizations, positions, jurisdictions, and records.

---

# 36. Evidence Relationship

An evidence relationship connects evidence to the event, allegation, finding, or decision it supports.

---

# 37. Source Relationship

A source relationship identifies the origin of information.

---

# 38. Task Relationship

A task relationship connects a task to the responsible person, AI, system, resource, or organization.

---

# 39. Resource Relationship

A resource relationship connects a person, task, system, or organization to a resource.

---

# 40. AI Relationship

An AI relationship identifies an AI model, AI provider, AI agent, or AI system participating in an APIG process.

---

# 41. AI Provider Relationship

The AI provider supplying a model or service must remain distinguishable from the APIG authority using that service.

---

# 42. AI Model Relationship

An AI model must remain distinguishable from the provider operating or supplying it.

---

# 43. AI Agent Relationship

An AI agent is a configured operational actor that may use an AI model and authorized tools.

---

# 44. AI Session Relationship

An AI session represents a particular operational interaction.

---

# 45. Tool Relationship

A tool relationship identifies systems or services an AI may use.

---

# 46. Resource Relationship

The AI should be able to determine what resources are relevant to a task through documented relationships and hierarchy.

---

# 47. Entity Attributes

Entities may contain attributes such as:

- Name
- Identifier
- Type
- Status
- Location
- Date
- Authority
- Jurisdiction
- Organization
- Position.

---

# 48. Relationship Attributes

Relationships may contain attributes such as:

- Relationship type
- Effective date
- End date
- Authority
- Source
- Status
- Evidence.

---

# 49. Effective Date

A relationship may have an effective date.

---

# 50. End Date

A relationship may have an end date.

---

# 51. Historical Relationship

A relationship that existed in the past should remain distinguishable from a current relationship.

---

# 52. Current Relationship

A current relationship is one that is presently applicable.

---

# 53. Future Relationship

A future relationship may be recorded before it becomes effective.

---

# 54. Relationship Status

Relationships may be:

- Proposed
- Active
- Suspended
- Ended
- Superseded
- Disputed.

---

# 55. Disputed Relationship

A disputed relationship should not automatically be treated as established fact.

---

# 56. Relationship Source

Material relationships should have a source where practical.

---

# 57. Relationship Evidence

Material relationships may require supporting evidence.

---

# 58. Relationship Confidence

Where appropriate, APIG may represent the confidence or verification status of a relationship.

---

# 59. Verified Relationship

A verified relationship has been established through appropriate evidence or authority.

---

# 60. Unverified Relationship

An unverified relationship may exist as a proposed or reported relationship without being established as fact.

---

# 61. Alleged Relationship

An alleged relationship must remain distinguishable from a verified relationship.

---

# 62. Relationship Inference

AI systems may infer relationships for analysis but must distinguish inferred relationships from documented relationships.

---

# 63. No Fabricated Relationships

An AI must not invent organizational, supervisory, legal, or jurisdictional relationships.

---

# 64. Relationship Validation

Material relationships should be validated against authoritative sources where practical.

---

# 65. Authority Source

Authority relationships should be supported by the applicable governing source where practical.

---

# 66. Organizational Source

Organizational relationships should be supported by appropriate organizational records.

---

# 67. Jurisdictional Source

Jurisdictional relationships should be supported by applicable law, regulation, policy, charter, ordinance, or other authoritative source where appropriate.

---

# 68. Chain of Command

A chain of command represents supervisory or organizational authority relationships.

---

# 69. Chain of Command Navigation

Authorized users should be able to navigate through applicable chains of command.

---

# 70. Authority Chain

An authority chain may include:

PERSON
→ POSITION
→ SUPERVISOR
→ ORGANIZATION
→ OVERSIGHT BODY
→ APPOINTING AUTHORITY
→ JURISDICTION.

---

# 71. Chain of Command Distinction

Not every organizational connection is a chain-of-command relationship.

---

# 72. Downstream

Downstream entities are entities connected below an authority within a defined organizational or authority relationship.

---

# 73. Upstream

Upstream entities are entities connected above an actor within a defined organizational or authority relationship.

---

# 74. Lateral Relationship

A lateral relationship connects entities at comparable organizational levels without establishing supervision.

---

# 75. Peer Relationship

A peer relationship identifies comparable positions or actors without establishing supervisory authority.

---

# 76. Staff Relationship

Staff may have operational relationships with other staff without those relationships automatically creating supervisory authority.

---

# 77. Staff Instructions

A staff member may provide operational instructions without becoming the supervisor of the recipient.

---

# 78. Executive Relationship

An executive may have supervisory authority over staff according to the organization's established structure.

---

# 79. Board Relationship

A board may have governance or oversight authority without directly supervising every employee of the organization.

---

# 80. Appointing Authority

An appointing authority may have authority to appoint members of a board, commission, or other body.

---

# 81. Appointing Authority Navigation

Where applicable, users should be able to navigate from an appointing authority to the body or positions it appoints.

---

# 82. Board-to-Organization Relationship

A board may have governance, oversight, or appointment relationships with an organization.

---

# 83. Board-to-Staff Relationship

A board's relationship to staff must be represented according to the actual authority structure rather than automatically treating the board as each employee's direct supervisor.

---

# 84. County-to-Agency Relationship

A county or other governmental body may have legal, administrative, appointment, funding, oversight, or other relationships with an agency.

---

# 85. Governmental Relationship

Governmental relationships must identify their actual type.

---

# 86. Jurisdictional Scope

An entity may be subject to more than one jurisdiction.

---

# 87. Primary Jurisdiction

Where appropriate, a record may identify its primary jurisdiction.

---

# 88. Concurrent Jurisdiction

Multiple jurisdictions may apply simultaneously.

---

# 89. Jurisdiction Conflict

Conflicting jurisdictional claims must be identified rather than silently resolved by the AI.

---

# 90. Jurisdiction Determination

The AI should use applicable governing sources when determining jurisdiction.

---

# 91. Jurisdictional Uncertainty

If jurisdiction cannot be established reliably, the AI should identify the uncertainty.

---

# 92. Event

An event is an occurrence that can be documented and associated with relevant entities.

---

# 93. Event Date

An event should have a date when known.

---

# 94. Event Time

An event may include a time when relevant and known.

---

# 95. Event Location

An event may include a location when relevant.

---

# 96. Event Participants

Events may be connected to people, organizations, positions, or systems involved.

---

# 97. Event Classification

Events may be classified according to their purpose and sensitivity.

---

# 98. Accountability Event

An accountability event is an event relevant to responsibility, oversight, supervision, governance, performance, compliance, or other APIG accountability functions.

---

# 99. Conduct

Conduct represents an action or behavior attributable to an identified actor where established.

---

# 100. Attribution

Conduct should be attributed only when supported by sufficient information.

---

# 101. No Automatic Attribution

A relationship to an actor does not automatically establish that actor's responsibility for another person's conduct.

---

# 102. Direct Conduct

Direct conduct is conduct performed by the identified actor.

---

# 103. Supervisory Responsibility

Supervisory responsibility identifies a supervisor's organizational responsibility without automatically establishing that the supervisor caused the subordinate's conduct.

---

# 104. Oversight Responsibility

Oversight responsibility identifies an oversight role without automatically establishing direct control over an event.

---

# 105. Appointment Responsibility

Appointment authority identifies appointment power without automatically establishing responsibility for every action of an appointee.

---

# 106. Jurisdictional Responsibility

Jurisdiction identifies the applicable governmental or legal scope without automatically establishing personal responsibility.

---

# 107. Accountability Relationship

An accountability relationship should specify the basis for the relationship.

---

# 108. Accountability Navigation

Users should be able to navigate from an accountability event to relevant:

- Person
- Position
- Supervisor
- Organization
- Oversight authority
- Appointing authority
- Jurisdiction
- Records
- Evidence.

---

# 109. Downstream Accountability Navigation

Where an authority has legitimate oversight relationships, an authorized user may navigate downward to relevant organizations, positions, events, and records.

---

# 110. Upstream Accountability Navigation

Where an event concerns a subordinate actor, an authorized user may navigate upward to relevant supervisors, oversight authorities, appointing authorities, and jurisdictions.

---

# 111. Accountability Does Not Equal Liability

A navigable relationship does not by itself establish legal liability, fault, negligence, misconduct, or causation.

---

# 112. Causation

Causation is a separate determination requiring appropriate evidence.

---

# 113. Fault

Fault is a separate determination requiring appropriate evidence and applicable standards.

---

# 114. Legal Liability

Legal liability is a separate determination requiring applicable law and appropriate analysis.

---

# 115. Performance Concern

A conduct event may be linked to a performance concern without automatically establishing misconduct.

---

# 116. Agency Concern

An event may be relevant to an organization's operations without establishing wrongdoing by the organization.

---

# 117. Oversight Event

An event may be relevant to an oversight authority because it occurred within an organization under that authority's oversight.

---

# 118. Watch Relationship

A person or body may have oversight responsibility for an organization during a relevant period.

---

# 119. Historical Oversight

Historical oversight relationships should be preserved when relevant to understanding past events.

---

# 120. Temporal Accountability

The authority structure applicable when an event occurred should be considered when analyzing accountability.

---

# 121. Relationship Changes

Changes in authority should not retroactively rewrite historical relationships.

---

# 122. Position Vacancy

A vacant position should remain distinguishable from the person who previously occupied it.

---

# 123. Acting Position

An acting appointment should be represented as a distinct status where appropriate.

---

# 124. Delegated Authority

Delegated authority should be represented separately from permanent authority.

---

# 125. Delegation

A delegation relationship should identify:

- Delegator
- Delegate
- Authority
- Scope
- Effective period.

---

# 126. Delegation Does Not Transfer Everything

A delegation of one authority does not automatically transfer unrelated authority.

---

# 127. Revocation

Delegated authority may be revoked.

---

# 128. Temporary Authority

Temporary authority should have an identifiable duration where practical.

---

# 129. Emergency Authority

Emergency authority should be represented separately from ordinary authority.

---

# 130. Authority Scope

Every authority relationship should be interpreted according to its scope.

---

# 131. Authority Limits

Authority may be limited by:

- Law
- Policy
- Position
- Jurisdiction
- Time
- Resource
- Task.

---

# 132. Authority Conflict

Conflicting authority claims should be identified and escalated when necessary.

---

# 133. Authority Hierarchy

Where multiple authorities apply, APIG should determine the applicable hierarchy according to the relevant governing rules.

---

# 134. No Assumed Supremacy

An AI must not assume that one authority is superior merely because it appears organizationally senior.

---

# 135. Authority Evidence

Material authority claims should be supported by authoritative documentation where practical.

---

# 136. Relationship Graph

APIG may represent entities and relationships as a graph.

---

# 137. Graph Nodes

Graph nodes may represent:

- People
- Organizations
- Positions
- Jurisdictions
- Events
- Records
- Systems
- Resources.

---

# 138. Graph Edges

Graph edges represent defined relationships between nodes.

---

# 139. Typed Edges

Relationships should be typed so that a supervisory relationship is distinguishable from an oversight, appointment, membership, or peer relationship.

---

# 140. Graph Navigation

Authorized users should be able to follow relevant relationship paths.

---

# 141. Path Interpretation

A path through multiple relationships must not be interpreted as a single direct relationship unless the governing rules establish that result.

---

# 142. Relationship Path

For example:

COUNTY CHAIR
→ APPOINTMENT AUTHORITY
→ BOARD
→ GOVERNANCE / OVERSIGHT
→ HOUSING AUTHORITY
→ EXECUTIVE DIRECTOR
→ SUPERVISION
→ STAFF.

---

# 143. Path Preservation

Each relationship in a path should remain individually identifiable.

---

# 144. Path Evidence

Where practical, each material relationship in an authority path should have supporting evidence.

---

# 145. Relationship Visualization

The APIG interface may visually represent authority, organizational, jurisdictional, and accountability relationships.

---

# 146. Visual Distinction

Different relationship types should be visually distinguishable.

---

# 147. Navigation Safety

Visual proximity must not be treated as evidence of authority.

---

# 148. Profile Page

An entity profile may display relevant relationships and connected records.

---

# 149. Person Profile

A person profile may display:

- Current position
- Historical positions
- Supervisory relationships
- Oversight relationships
- Appointment relationships
- Relevant events
- Relevant records.

---

# 150. Position Profile

A position profile may display:

- Organization
- Current occupant
- Historical occupants
- Supervisor
- Subordinates
- Authority
- Jurisdiction.

---

# 151. Organization Profile

An organization profile may display:

- Governing body
- Executive
- Staff
- Jurisdiction
- Oversight authorities
- Appointment authorities
- Relevant records.

---

# 152. Jurisdiction Profile

A jurisdiction profile may display:

- Geographic scope
- Governmental authority
- Applicable governing sources
- Related organizations
- Related positions
- Relevant records.

---

# 153. Event Profile

An event profile may display:

- Date
- Participants
- Organizations
- Positions
- Jurisdictions
- Evidence
- Findings
- Related records.

---

# 154. Record Profile

A record profile may display:

- Record type
- Source
- Date
- Classification
- Related entities
- Version
- Authority
- Status.

---

# 155. Profile Navigation

Profiles should provide navigation to relevant connected entities when authorized.

---

# 156. Sensitive Record Filtering

Sensitive records should not appear in profiles to users who lack authorization.

---

# 157. Public Profile

A public profile should display only information authorized for public access.

---

# 158. Internal Profile

An internal profile may display additional information according to the user's authority.

---

# 159. AI Profile Access

An AI should see only profile information it is authorized to access.

---

# 160. Search

Users and AI should be able to search entities by appropriate identifiers and attributes.

---

# 161. Entity Search

Entity search should distinguish similarly named entities.

---

# 162. Person Disambiguation

The system should avoid merging two people merely because their names are similar.

---

# 163. Organization Disambiguation

The system should avoid merging organizations merely because their names are similar.

---

# 164. Position Disambiguation

Different positions with similar names should remain distinguishable.

---

# 165. Jurisdiction Disambiguation

Different jurisdictions with similar names should remain distinguishable.

---

# 166. Entity Merge

Entity records should be merged only when identity has been sufficiently established.

---

# 167. Entity Split

A merged entity should be split when evidence shows that it represents multiple distinct entities.

---

# 168. Identity Uncertainty

Identity uncertainty should be explicitly represented.

---

# 169. Alias

An entity may have aliases, former names, abbreviations, or alternate identifiers.

---

# 170. Alias Preservation

Aliases should not replace the canonical identity.

---

# 171. Historical Name

Historical names may be preserved where necessary to interpret historical records.

---

# 172. Relationship Audit

Material relationship changes should be auditable where practical.

---

# 173. Relationship Correction

Incorrect relationships should be corrected without destroying relevant historical evidence where practical.

---

# 174. Relationship Dispute

Disputed relationships should preserve the basis of the dispute where appropriate.

---

# 175. Relationship Expiration

Relationships that naturally expire should have an expiration or end condition where practical.

---

# 176. Automated Relationship Creation

Automated systems may propose relationships but should not create high-impact authoritative relationships without appropriate validation.

---

# 177. AI Relationship Inference

AI may identify possible relationships for review.

---

# 178. AI Relationship Authority

AI inference does not itself establish legal or organizational authority.

---

# 179. Human Validation

High-impact relationship determinations may require human validation.

---

# 180. Relationship Confidence

Where an AI proposes a relationship, confidence or verification status may be recorded.

---

# 181. Source Priority

When sources conflict, the AI should consider source authority, recency, jurisdiction, scope, and reliability.

---

# 182. Source Conflict

Conflicting sources should not be silently reconciled by inventing a result.

---

# 183. Escalation

Material unresolved relationship conflicts should be escalated.

---

# 184. Data Integrity

Entity and relationship data should be protected against unauthorized modification.

---

# 185. Referential Integrity

Relationships should not point to nonexistent entities where practical.

---

# 186. Broken Relationship

Broken relationships should be identified and repaired or removed according to appropriate procedures.

---

# 187. Orphan Record

A record lacking required entity relationships should be identified for review.

---

# 188. Orphan Entity

An entity without expected relationships may require review but should not automatically be deleted.

---

# 189. Data Retention

Entity and relationship history should be retained according to applicable record requirements.

---

# 190. Historical Reconstruction

Where practical, APIG should support reconstruction of the organizational and authority structure applicable at a past time.

---

# 191. Temporal Query

The system may support questions such as:

"Who supervised this person when the event occurred?"

"What authority appointed this board at that time?"

"Which jurisdiction applied when this record was created?"

---

# 192. Current Versus Historical

The current authority structure must not automatically be substituted for the historical structure relevant to an earlier event.

---

# 193. Historical Profile

A profile may allow authorized users to view historical relationships.

---

# 194. Relationship Timeline

Material relationships may be represented chronologically.

---

# 195. Accountability Timeline

Accountability events may be viewed alongside the authority relationships applicable at the time.

---

# 196. Cross-System Identity

Where APIG connects multiple systems, the system should preserve enough information to distinguish the same entity across those systems.

---

# 197. External Identifier

External systems may assign their own identifiers.

---

# 198. Identifier Mapping

APIG may maintain mappings between APIG identifiers and authorized external identifiers.

---

# 199. External Identity Uncertainty

An external identifier must not automatically be assumed to represent the same entity without sufficient evidence.

---

# 200. Core Principles

1. APIG represents important information as entities and relationships.
2. People and positions must remain distinct.
3. Organizations and positions must remain distinct.
4. Relationships must have identifiable types.
5. Supervision, oversight, appointment authority, instruction, and membership are distinct relationships.
6. Giving instructions does not automatically create supervision.
7. Oversight does not automatically create direct supervision.
8. Appointment authority does not automatically create direct supervision.
9. Organizational proximity does not establish authority.
10. Authority must be interpreted according to scope.
11. Jurisdiction must be established from applicable authority.
12. Historical relationships must be preserved where relevant.
13. Current relationships must not overwrite historical relationships.
14. AI inference must remain distinguishable from verified relationships.
15. AI must not fabricate relationships.
16. Material relationships should have supporting sources where practical.
17. Accountability navigation should support both upstream and downstream navigation.
18. A relationship does not automatically establish liability.
19. Direct conduct must remain distinct from supervisory responsibility.
20. Oversight responsibility must remain distinct from direct conduct.
21. Appointment authority must remain distinct from personal responsibility.
22. Jurisdiction must remain distinct from personal responsibility.
23. Graph paths must preserve every relationship type.
24. Visual connections must not be mistaken for authority.
25. Profiles should expose relevant relationships subject to authorization.
26. Sensitive records must remain access-controlled.
27. Identity ambiguity must be preserved rather than guessed.
28. Conflicting sources must be identified.
29. Material relationship changes should be auditable.
30. Historical authority structures should be reconstructable where practical.
31. APIG should support temporal accountability analysis.
32. External identities should be mapped carefully.
33. AI systems may propose relationships but do not create authority merely by inference.
34. High-impact relationships may require validation.
35. Data integrity and referential integrity should be maintained.
36. The relationship structure should support continuity across AI providers and systems.
37. The data architecture should allow users to navigate from a person or authority to relevant organizations, positions, events, and records.
38. The data architecture should preserve the difference between "connected to," "responsible for," "supervises," "oversees," "appointed," and "caused."
39. APIG must never use a relationship graph to manufacture conclusions that the underlying evidence does not establish.
40. The purpose of relationship modeling is accurate navigation, accountability, context, and institutional continuity.

---

# 201. Entity Resolution Sequence

INPUT
→ IDENTIFY ENTITY TYPE
→ SEARCH EXISTING ENTITIES
→ COMPARE IDENTIFIERS
→ COMPARE ATTRIBUTES
→ CHECK SOURCES
→ RESOLVE IDENTITY
→ CREATE OR LINK
→ RECORD CONFIDENCE
→ PRESERVE SOURCE.

---

# 202. Relationship Creation Sequence

IDENTIFY ENTITY A
→ IDENTIFY ENTITY B
→ IDENTIFY RELATIONSHIP TYPE
→ DETERMINE AUTHORITY
→ DETERMINE SCOPE
→ DETERMINE EFFECTIVE PERIOD
→ VERIFY SOURCE
→ CREATE RELATIONSHIP
→ RECORD EVIDENCE
→ MAKE NAVIGABLE.

---

# 203. Accountability Navigation Sequence

EVENT
→ PERSON
→ POSITION
→ SUPERVISOR
→ ORGANIZATION
→ OVERSIGHT AUTHORITY
→ APPOINTING AUTHORITY
→ JURISDICTION
→ RELATED RECORDS
→ RELATED EVIDENCE.

---

# 204. Historical Accountability Sequence

EVENT DATE
→ DETERMINE HISTORICAL POSITION
→ DETERMINE HISTORICAL SUPERVISOR
→ DETERMINE HISTORICAL ORGANIZATION
→ DETERMINE HISTORICAL OVERSIGHT
→ DETERMINE HISTORICAL APPOINTMENT AUTHORITY
→ DETERMINE APPLICABLE JURISDICTION
→ LINK RELEVANT RECORDS
→ PRESERVE HISTORICAL STRUCTURE.

---

# 205. Relationship Conflict Sequence

CONFLICT DETECTED
→ IDENTIFY SOURCES
→ COMPARE AUTHORITY
→ COMPARE DATE
→ COMPARE JURISDICTION
→ IDENTIFY SCOPE
→ DETERMINE WHETHER RESOLVABLE
→ RESOLVE OR ESCALATE
→ DOCUMENT RESULT.

---

# 206. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-28