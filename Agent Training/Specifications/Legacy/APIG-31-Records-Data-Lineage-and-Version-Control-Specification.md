# APIG-31 — Records, Data Lineage, and Version Control Specification

## Status

Active

## Purpose

This specification defines how APIG creates, organizes, identifies, relates, preserves, updates, versions, and retrieves records and data.

The fundamental principle is:

CREATE
→ IDENTIFY
→ CLASSIFY
→ RELATE
→ VERSION
→ PRESERVE
→ UPDATE
→ AUDIT
→ RETRIEVE.

---

# 1. Core Principle

APIG records must preserve enough information to determine what a record is, where it came from, when it existed, how it changed, and how it relates to other records.

---

# 2. Record

A record is a persistent representation of information relevant to APIG.

---

# 3. Record Identity

Each material record should have a stable identity.

---

# 4. Record Identifier

A record identifier uniquely identifies a record within its applicable system or scope.

---

# 5. Record Type

Records may represent:

- Person
- Organization
- Position
- Event
- Claim
- Evidence
- Finding
- Decision
- Communication
- Instruction
- Source
- Document
- Transaction
- Relationship
- Task
- Audit event
- System event.

---

# 6. Record Metadata

Material records should contain appropriate metadata.

Metadata may include:

- Identifier
- Record type
- Creation date
- Modification date
- Source
- Author
- Owner
- Status
- Version
- Related records
- Jurisdiction
- Classification.

---

# 7. Record Source

The origin of a record should be preserved where practical.

---

# 8. Record Creation

The system should distinguish records created by:

- Human
- AI
- Automated system
- Imported source
- External system.

---

# 9. Record Authorship

Where material, the creator or originating system should be identifiable.

---

# 10. Record Ownership

Ownership and responsibility for a record should be distinguished from authorship.

---

# 11. Record Custodian

A custodian is an actor responsible for maintaining or controlling a record.

---

# 12. Record Authority

The authority to create, modify, approve, publish, or delete a record should be determined separately from record ownership.

---

# 13. Record Status

A record may have statuses such as:

- Draft
- Active
- Archived
- Superseded
- Withdrawn
- Deleted
- Restricted
- Disputed.

---

# 14. Draft Record

A draft is not necessarily an authoritative final record.

---

# 15. Final Record

A final record represents the version designated as authoritative for its applicable purpose.

---

# 16. Superseded Record

A superseded record has been replaced by a later version or decision.

---

# 17. Historical Record

A historical record preserves information concerning a past state.

---

# 18. Historical Preservation

Historical records should not be silently rewritten to reflect current conditions.

---

# 19. Current State

Current-state information should be distinguishable from historical information.

---

# 20. Temporal Validity

Records may have:

- Effective date
- Expiration date
- Event date
- Creation date
- Modification date
- Publication date.

These dates are not necessarily interchangeable.

---

# 21. Event Date

The event date describes when the underlying event occurred.

---

# 22. Record Creation Date

The creation date describes when the record was created.

---

# 23. Publication Date

The publication date describes when information was made available to an audience.

---

# 24. Modification Date

The modification date describes when the record was changed.

---

# 25. Effective Date

The effective date describes when a rule, status, appointment, authority, or other condition becomes applicable.

---

# 26. Expiration Date

The expiration date describes when an applicable condition ceases to apply.

---

# 27. Date Distinction

APIG must not treat these dates as interchangeable without justification.

---

# 28. Version

A version is a distinct state of a record.

---

# 29. Version Number

Material records should use a version identifier where practical.

---

# 30. Version History

Version history should preserve material changes.

---

# 31. Immutable History

Where required, prior authoritative versions should remain preserved rather than being overwritten.

---

# 32. Change

A change is any modification to the content, structure, status, relationship, or metadata of a record.

---

# 33. Material Change

A material change could affect interpretation, authority, accountability, evidence, or decision-making.

---

# 34. Minor Change

A minor change does not materially affect the meaning or function of the record.

---

# 35. Change Classification

Material and minor changes may be treated differently, but material changes must remain traceable.

---

# 36. Change Log

Material record changes should be documented.

---

# 37. Change Author

The actor responsible for a change should be identified where practical.

---

# 38. Change Reason

Material changes should include a reason where practical.

---

# 39. Change Timestamp

Material changes should have a timestamp where practical.

---

# 40. Prior State

Where material, the prior state should remain recoverable.

---

# 41. New State

The resulting state should be identifiable.

---

# 42. Version Comparison

The system should be able to determine what materially changed between versions where practical.

---

# 43. Reversal

A change may be reversed without destroying the history of the original change.

---

# 44. Correction

Corrections should preserve awareness that a prior version existed.

---

# 45. Silent Rewrite

APIG should avoid silently rewriting material historical records.

---

# 46. Data Lineage

Data lineage describes the path by which information originated, moved, transformed, combined, or produced a result.

---

# 47. Lineage Chain

A material data chain may be represented as:

SOURCE
→ RAW DATA
→ TRANSFORMATION
→ DERIVED DATA
→ ANALYSIS
→ FINDING
→ DECISION.

---

# 48. Source Data

Source data is information obtained from an originating source.

---

# 49. Raw Data

Raw data is information retained substantially in the form in which it was received.

---

# 50. Transformed Data

Transformed data has been changed through processing.

---

# 51. Derived Data

Derived data is produced from other data through calculation, interpretation, classification, or other processing.

---

# 52. Derived Data Distinction

Derived data must remain distinguishable from original source data.

---

# 53. Transformation Record

Material transformations should be documented.

---

# 54. Transformation Method

Where material, the method used to transform data should be identifiable.

---

# 55. Transformation Input

Material transformation inputs should be identifiable.

---

# 56. Transformation Output

Material transformation outputs should be identifiable.

---

# 57. Calculation

Material calculations should preserve relevant inputs and methodology.

---

# 58. AI Transformation

AI-generated transformations should remain distinguishable from source information.

---

# 59. AI Summary

An AI summary is a derived representation and should not be treated as identical to the source document.

---

# 60. AI Interpretation

AI interpretation should remain distinguishable from the underlying record.

---

# 61. AI Extraction

Information extracted by AI should be traceable to the source where practical.

---

# 62. OCR Data

OCR-derived text should remain distinguishable from manually verified text.

---

# 63. Translation Data

Translated data should remain distinguishable from the original-language source.

---

# 64. Data Merge

When records are merged, the contributing source records should remain identifiable.

---

# 65. Data Split

When one record is divided into multiple records, the relationship to the original should be preserved.

---

# 66. Record Consolidation

Consolidated records should preserve links to underlying records.

---

# 67. Record Relationship

Records may be connected through explicit relationships.

---

# 68. Relationship Types

Relationships may include:

- Parent
- Child
- Member
- Employer
- Employee
- Supervisor
- Subordinate
- Appointer
- Appointee
- Jurisdiction
- Authority
- Oversight
- Evidence-of
- Supports
- Contradicts
- Derived-from
- Supersedes
- Responds-to
- Related-to.

---

# 69. Relationship Identity

Material relationships should be represented explicitly.

---

# 70. Relationship Source

Material relationships should identify their supporting source where practical.

---

# 71. Relationship Effective Date

Relationships may have effective dates.

---

# 72. Relationship Expiration

Relationships may cease to apply.

---

# 73. Historical Relationships

Past relationships should remain distinguishable from current relationships.

---

# 74. Authority Relationship

Authority relationships should identify the type and scope of authority where practical.

---

# 75. Supervisory Relationship

A supervisory relationship should be distinguished from general organizational association.

---

# 76. Oversight Relationship

An oversight relationship should be distinguished from direct supervision.

---

# 77. Appointment Relationship

An appointment relationship should be distinguished from operational command.

---

# 78. Jurisdictional Relationship

A jurisdictional relationship should identify the relevant jurisdiction and scope.

---

# 79. Relationship Inference

AI may infer a possible relationship, but an inferred relationship should not automatically become an authoritative relationship.

---

# 80. Relationship Verification

Material relationships should be verified against appropriate sources.

---

# 81. Record Linking

Related records should be linkable.

---

# 82. Bidirectional Navigation

Where practical, relationships should permit navigation in both directions.

For example:

PERSON
→ POSITION
→ ORGANIZATION

and:

ORGANIZATION
→ POSITION
→ PERSON.

---

# 83. Chain Navigation

The system should support navigation through relevant organizational, authority, jurisdictional, and accountability relationships.

---

# 84. Downstream Navigation

Where appropriate, a record should permit authorized users to navigate toward downstream entities.

---

# 85. Upstream Navigation

Where appropriate, a record should permit authorized users to navigate toward upstream authorities.

---

# 86. No Automatic Responsibility

A relationship does not automatically establish responsibility for every event involving a connected entity.

---

# 87. Accountability Link

An accountability link should identify the relationship that makes the connection relevant.

---

# 88. Accountability Scope

Accountability relationships should identify whether the relationship concerns:

- Direct action
- Supervision
- Oversight
- Appointment
- Governance
- Jurisdiction
- Resource authority
- Other defined authority.

---

# 89. Evidence Link

Evidence should be linkable to the claim or event it supports.

---

# 90. Contradictory Evidence Link

Evidence that contradicts a claim should also be linkable.

---

# 91. Finding Link

A finding should be linked to the evidence supporting it.

---

# 92. Decision Link

A decision should be linked to the applicable finding, authority, and supporting evidence where practical.

---

# 93. Record Dependency

A record may depend on other records.

---

# 94. Dependency Mapping

Material dependencies should be identifiable.

---

# 95. Broken Dependency

If a source record is removed, changed, or becomes unavailable, dependent records should not silently appear unchanged.

---

# 96. Source Change

When a source changes materially, dependent derived information may require review.

---

# 97. Derived Record Review

Material derived records should be reevaluated when significant source information changes.

---

# 98. Stale Data

Information may become stale.

---

# 99. Staleness

The system should identify when information may no longer represent the current state.

---

# 100. Current Verification

Current status should be verified when the question requires current information.

---

# 101. Historical Verification

Historical status should be verified against records applicable to the relevant historical period.

---

# 102. Record Retrieval

Records should be retrievable by relevant identifiers and relationships.

---

# 103. Search

Authorized users and systems should be able to search records according to applicable access controls.

---

# 104. Relationship Search

Search should support relationships where practical.

---

# 105. Temporal Search

Search should support relevant dates and historical states where practical.

---

# 106. Jurisdictional Search

Search should support relevant jurisdictional relationships where practical.

---

# 107. Authority Search

Search should support relevant authority relationships where practical.

---

# 108. Entity Search

Search should support navigation by person, organization, position, event, and other entities.

---

# 109. Event Search

Events should be searchable by date, entity, jurisdiction, and relevant relationships where practical.

---

# 110. Evidence Search

Evidence should be searchable by source, claim, event, entity, and status where practical.

---

# 111. Record Classification

Records should be classified according to their function and sensitivity.

---

# 112. Access Classification

Examples may include:

- Public
- Internal
- Restricted
- Confidential
- Highly restricted.

Actual classifications must follow applicable APIG rules.

---

# 113. Access Control

Record access must follow applicable authorization rules.

---

# 114. Public Record

A record designated public may be accessible to the public subject to applicable restrictions.

---

# 115. Restricted Record

A restricted record requires authorization for access.

---

# 116. Access Log

Material access to sensitive records should be logged where practical.

---

# 117. Modification Log

Material modification should be logged where practical.

---

# 118. Export

Exported records should preserve relevant identity, source, version, and metadata where practical.

---

# 119. Record Copy

A copy should remain distinguishable from the authoritative original.

---

# 120. Exported Copy

An exported copy should identify its source and version where practical.

---

# 121. Synchronization

When records exist in multiple systems, synchronization should preserve source and version information.

---

# 122. Synchronization Conflict

Conflicting versions should be identified rather than silently overwritten.

---

# 123. Master Record

A system may designate an authoritative record for a particular purpose.

---

# 124. Master Record Scope

A master record is authoritative only within its defined scope.

---

# 125. No Universal Master Record

One record should not automatically be treated as authoritative for every purpose.

---

# 126. Source of Truth

A source of truth must be defined in relation to a particular subject and purpose.

---

# 127. Multiple Sources of Truth

Different systems may be authoritative for different aspects of the same entity.

---

# 128. Record Reconciliation

Conflicting records may require reconciliation.

---

# 129. Reconciliation Process

CONFLICT
→ IDENTIFY RECORDS
→ IDENTIFY SOURCES
→ CHECK DATES
→ CHECK AUTHORITY
→ CHECK VERSION
→ CHECK SCOPE
→ DETERMINE AUTHORITATIVE SOURCE
→ RESOLVE OR ESCALATE
→ DOCUMENT RESULT.

---

# 130. Duplicate Records

Potential duplicates should be identified.

---

# 131. Duplicate Resolution

Records should not be merged merely because names or identifiers appear similar.

---

# 132. Entity Resolution

Entity resolution should use sufficient evidence to determine whether records represent the same entity.

---

# 133. False Merge

Incorrectly merging two distinct entities can materially damage records and must be avoided.

---

# 134. False Split

Incorrectly treating one entity as multiple entities can also damage record integrity.

---

# 135. Record Integrity

Record integrity requires preservation of accuracy, consistency, provenance, and history.

---

# 136. Data Integrity

Material data should be protected from unauthorized alteration.

---

# 137. Integrity Verification

Where appropriate, technical mechanisms may be used to detect unauthorized changes.

---

# 138. Backup

Material records should be backed up according to applicable requirements.

---

# 139. Recovery

Material records should be recoverable when required.

---

# 140. Disaster Recovery

Record systems should have appropriate recovery procedures.

---

# 141. Recovery Version

Recovered records should preserve the version or state that was restored where practical.

---

# 142. Record Deletion

Deletion of records must follow applicable retention, legal, operational, and authorization requirements.

---

# 143. Deletion Authority

Only appropriately authorized actors may delete material records.

---

# 144. Deletion Record

Material deletion should be recorded where required.

---

# 145. Logical Deletion

A record may be marked deleted without immediately destroying underlying data.

---

# 146. Permanent Destruction

Permanent destruction should be distinguished from logical deletion.

---

# 147. Retention

Records should be retained according to applicable requirements.

---

# 148. Retention Period

A retention period may depend on:

- Record type
- Legal requirements
- Operational need
- Historical value
- Litigation or preservation requirements
- Governance requirements.

---

# 149. Preservation Hold

Records subject to a preservation requirement must not be destroyed contrary to that requirement.

---

# 150. Archive

Archived records remain preserved but may no longer be active.

---

# 151. Archive Integrity

Archived records should preserve sufficient metadata to establish their identity and historical state.

---

# 152. Record Lifecycle

A record may follow:

CREATE
→ ACTIVE
→ UPDATED
→ SUPERSEDED
→ ARCHIVED
→ DISPOSED

according to applicable requirements.

---

# 153. Lifecycle Exception

Not every record follows every lifecycle stage.

---

# 154. Record Restoration

Archived records may be restored to active use where authorized.

---

# 155. Restoration History

Restoration should not erase the fact that a record was previously archived.

---

# 156. Record Publication

Publication creates an externally accessible representation of a record.

---

# 157. Published Version

The published version should be identifiable.

---

# 158. Publication Correction

Corrections to published records should preserve the historical publication where appropriate.

---

# 159. Public Record History

Publicly visible records may require preservation of prior versions to maintain accountability.

---

# 160. Record Relationships and Website Navigation

The website should expose appropriate record relationships through navigation.

---

# 161. Entity Page

An entity page may link to relevant:

- Positions
- Organizations
- Events
- Evidence
- Findings
- Decisions
- Authority relationships
- Jurisdictional relationships
- Accountability records.

---

# 162. Authority Navigation

An authorized user should be able to navigate from an authority figure to relevant downstream organizational relationships.

---

# 163. Downstream Event Navigation

Where appropriate, an entity page may expose relevant downstream events through established relationships.

---

# 164. Upstream Accountability Navigation

Where appropriate, an event or record may identify relevant upstream supervisory, oversight, appointment, governance, or jurisdictional relationships.

---

# 165. Relationship Qualification

Downstream navigation must preserve the distinction between:

- Direct conduct
- Supervision
- Oversight
- Appointment
- Governance
- Jurisdiction.

---

# 166. No Automatic Attribution

Displaying a downstream event on an upstream entity page must not imply that the upstream entity personally committed the event.

---

# 167. Accountability Context

Where an event is displayed through an upstream relationship, the relationship type should be identifiable.

---

# 168. Example

If a maintenance employee is documented as having committed an event:

MAINTENANCE EMPLOYEE
→ SUPERVISED BY
→ EXECUTIVE DIRECTOR
→ OVERSIGHT RELATIONSHIP
→ BOARD
→ APPOINTMENT AUTHORITY
→ COUNTY BOARD CHAIRPERSON

the website may permit navigation through those relationships.

The system must not represent the county board chairperson as having committed the employee's conduct merely because the event is reachable through the authority chain.

---

# 169. Supervisory Boundary

If an office employee and maintenance employee both report directly to an executive director, neither employee should automatically be represented as the supervisor of the other.

---

# 170. Peer Relationship

Two employees may be organizational peers even when one provides instructions or coordinates work.

---

# 171. Instruction Versus Supervision

Giving an instruction does not automatically establish a formal supervisory relationship.

---

# 172. Formal Supervision

Formal supervision should be based on the applicable organizational structure or authoritative source.

---

# 173. Accountability Propagation

Relevant events may be navigable through an authority chain without automatically propagating personal responsibility.

---

# 174. Propagation Rule

The system should distinguish:

EVENT PROPAGATION FOR NAVIGATION

from:

RESPONSIBILITY ATTRIBUTION.

---

# 175. Event Navigation

An event may be linked upward through relevant relationships so users can understand organizational context.

---

# 176. Responsibility Attribution

Responsibility must be established independently according to applicable evidence, authority, supervision, oversight, and governing rules.

---

# 177. Website Presentation

The website should make relationship type visible when an event is reached through an organizational or authority relationship.

---

# 178. Record Transparency

Where appropriate, users should be able to determine why a record appears on an entity's page.

---

# 179. Explainable Relationship

A relationship displayed by the website should be explainable through its source and relationship type.

---

# 180. No Hidden Relationship

Material accountability relationships should not be silently created by the interface.

---

# 181. Record Provenance

Material records should maintain provenance sufficient to reconstruct their origin.

---

# 182. Provenance Chain

Provenance may include:

SOURCE
→ ACQUISITION
→ STORAGE
→ TRANSFORMATION
→ REVIEW
→ PUBLICATION
→ UPDATE.

---

# 183. Provenance Preservation

Material provenance should survive reasonable transformations and exports.

---

# 184. Provenance Failure

If provenance cannot be established, that limitation should be recorded where material.

---

# 185. Uncertain Provenance

Information with uncertain provenance should not automatically be treated as authoritative.

---

# 186. Imported Record

Imported records should retain information identifying the originating system where practical.

---

# 187. Import Date

The import date should be distinguished from the original record date.

---

# 188. Import Transformation

Material import transformations should be documented.

---

# 189. External Synchronization

External data synchronization should preserve source identity and synchronization time.

---

# 190. Synchronization Failure

Failed synchronization should not silently overwrite valid records with incomplete information.

---

# 191. Data Conflict

Data conflicts should be surfaced for resolution when material.

---

# 192. Record Auditability

A reviewer should be able to reconstruct material record history.

---

# 193. Audit Trail

The audit trail should identify material:

- Creation
- Modification
- Approval
- Publication
- Access
- Export
- Deletion
- Restoration.

---

# 194. Audit Integrity

Audit records should be protected against unauthorized alteration.

---

# 195. Audit Retention

Audit records should be retained according to applicable requirements.

---

# 196. Record Reconstruction

APIG should be able to reconstruct the relevant historical state of material records where practical.

---

# 197. Historical State

Historical state reconstruction should consider:

- Version
- Effective date
- Relationship state
- Authority
- Jurisdiction
- Source
- Evidence.

---

# 198. Current Versus Historical Page

Where the website displays historical information, users should be able to distinguish historical state from current state.

---

# 199. Record Interoperability

Records should use consistent identifiers and relationships where practical so that different APIG components can reference the same entities.

---

# 200. Core Principles

1. Every material record should have a stable identity.
2. Record identity should remain distinct from record content.
3. Record authorship should remain distinct from record ownership.
4. Record authority should remain distinct from authorship.
5. Material records should preserve provenance.
6. Material changes should remain traceable.
7. Historical states should not be silently rewritten.
8. Current and historical information must remain distinguishable.
9. Event date, creation date, publication date, modification date, effective date, and expiration date are distinct concepts.
10. Derived data must remain distinguishable from source data.
11. AI-generated information must remain distinguishable from source information.
12. Material transformations should be documented.
13. Material relationships should be explicit.
14. Relationships should identify their type.
15. Relationships may have effective and expiration dates.
16. Historical relationships should be preserved.
17. Authority relationships must be distinguished from general organizational relationships.
18. Supervision must be distinguished from oversight.
19. Oversight must be distinguished from appointment authority.
20. Appointment authority must be distinguished from operational command.
21. Jurisdiction must be distinguished from personal responsibility.
22. An organizational relationship does not automatically establish responsibility.
23. Event navigation and responsibility attribution are separate functions.
24. Downstream events may be navigable through upstream authority relationships without implying personal misconduct by the upstream actor.
25. Peer employees should not automatically be represented as supervisors.
26. Giving instructions does not automatically establish formal supervision.
27. Formal supervisory relationships should be based on authoritative organizational information.
28. Evidence must be linked to claims and findings where practical.
29. Findings must be linked to their supporting evidence.
30. Decisions should be linked to applicable authority and findings where practical.
31. Source conflicts should be identified and resolved or escalated.
32. Duplicate records should not be merged without sufficient evidence.
33. False merges and false splits must be avoided.
34. Record copies should remain distinguishable from authoritative records.
35. Exports should preserve material metadata.
36. Synchronization conflicts must not be silently overwritten.
37. Deletion requires appropriate authority.
38. Preservation requirements override ordinary deletion procedures.
39. Archives should preserve historical identity and metadata.
40. Published corrections should preserve relevant historical context.
41. Material access and modification should be auditable where appropriate.
42. The website should expose relevant relationships through understandable navigation.
43. Users should be able to determine why a record appears through a relationship.
44. Material relationships should be explainable through sources.
45. APIG should preserve enough lineage to reconstruct how important information moved from source to conclusion.
46. APIG should preserve enough history to reconstruct material prior states.
47. APIG should never silently convert derived information into source information.
48. APIG should never silently convert inferred relationships into authoritative relationships.
49. APIG should never use interface navigation to imply responsibility that the underlying records do not establish.
50. The record architecture must allow another authorized human or AI to reconstruct the history, provenance, relationships, and transformations underlying a material record.

---

# 201. Record Creation Sequence

SOURCE
→ IDENTIFY
→ CREATE RECORD
→ ASSIGN IDENTIFIER
→ CLASSIFY
→ RECORD PROVENANCE
→ ESTABLISH RELATIONSHIPS
→ ASSIGN VERSION
→ STORE
→ AUDIT.

---

# 202. Record Modification Sequence

REQUEST CHANGE
→ VERIFY AUTHORITY
→ IDENTIFY CURRENT VERSION
→ CLASSIFY CHANGE
→ PRESERVE PRIOR STATE
→ APPLY CHANGE
→ ASSIGN NEW VERSION
→ RECORD CHANGE
→ UPDATE DEPENDENCIES
→ AUDIT.

---

# 203. Record Reconciliation Sequence

CONFLICT
→ IDENTIFY RECORDS
→ IDENTIFY SOURCES
→ CHECK AUTHORITY
→ CHECK DATES
→ CHECK VERSIONS
→ CHECK SCOPE
→ CHECK PROVENANCE
→ RESOLVE OR ESCALATE
→ DOCUMENT RESULT
→ PRESERVE HISTORY.

---

# 204. Data Lineage Sequence

SOURCE
→ ACQUIRE
→ STORE
→ TRANSFORM
→ DERIVE
→ ANALYZE
→ REVIEW
→ PUBLISH
→ UPDATE
→ PRESERVE LINEAGE.

---

# 205. Historical Reconstruction Sequence

QUESTION
→ IDENTIFY RELEVANT DATE
→ IDENTIFY APPLICABLE VERSION
→ IDENTIFY EFFECTIVE RELATIONSHIPS
→ IDENTIFY APPLICABLE AUTHORITY
→ IDENTIFY RELEVANT EVIDENCE
→ RECONSTRUCT STATE
→ DISTINGUISH HISTORICAL FROM CURRENT
→ RECORD BASIS.

---

# 206. Accountability Navigation Sequence

EVENT
→ IDENTIFY PERSON
→ IDENTIFY POSITION
→ IDENTIFY ORGANIZATION
→ IDENTIFY RELATIONSHIP TYPE
→ IDENTIFY UPSTREAM AUTHORITY
→ IDENTIFY DOWNSTREAM RELATIONSHIPS
→ DISPLAY NAVIGATION PATH
→ DISPLAY RELATIONSHIP TYPE
→ DISPLAY SUPPORTING RECORDS
→ DO NOT AUTOMATICALLY ATTRIBUTE RESPONSIBILITY.

---

# 207. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-31