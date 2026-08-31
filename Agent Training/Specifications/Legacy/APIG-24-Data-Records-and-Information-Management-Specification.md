# APIG-24 — Data, Records, and Information Management Specification

## Status

Active

## Purpose

This specification defines how APIG creates, stores, organizes, identifies, versions, relates, protects, retrieves, transfers, and preserves information and records.

The fundamental principle is:

CREATE
→ IDENTIFY
→ CLASSIFY
→ STORE
→ RELATE
→ VERSION
→ PROTECT
→ RETRIEVE
→ AUDIT
→ PRESERVE.

---

# 1. Core Principle

APIG information should remain understandable, attributable, retrievable, and portable across systems and AI providers.

---

# 2. Information

Information is any data, statement, observation, instruction, document, record, message, event, or other material retained or processed by APIG.

---

# 3. Record

A record is information retained because it has operational, evidentiary, historical, administrative, governance, or accountability value.

---

# 4. Data

Data is structured or unstructured information used by APIG.

---

# 5. Source

Every material record should identify its source where practical.

---

# 6. Attribution

Material records should identify the actor, system, or source responsible for creating or submitting them where practical.

---

# 7. Timestamp

Material records should include a reliable timestamp where practical.

---

# 8. Record Identity

Material records should have a unique identifier where practical.

---

# 9. Record Type

Records should be classified according to their function.

Examples include:

- Specification
- Policy
- Procedure
- Instruction
- Task
- Event
- Report
- Message
- Evidence
- Configuration
- Decision
- Audit record.

---

# 10. Classification

Information may be classified according to:

- Public
- Internal
- Restricted
- Sensitive
- Administrative
- Operational.

---

# 11. Access Classification

Classification should correspond to applicable access controls.

---

# 12. Data Ownership

Where applicable, records should identify the entity responsible for their management.

---

# 13. Data Stewardship

A data steward is an actor responsible for maintaining a defined information resource.

---

# 14. Record Custody

Custody identifies the system, organization, or actor responsible for maintaining a record.

---

# 15. Source Preservation

The original source of material information should be preserved where practical.

---

# 16. Original Record

Where authenticity matters, the original record should be preserved separately from derived interpretations.

---

# 17. Derived Record

A derived record is produced from one or more other records.

---

# 18. Derivation

Derived information should identify its source records where practical.

---

# 19. Transformation

Material transformations of data should be documented where practical.

---

# 20. Data Integrity

APIG should protect records from unauthorized alteration.

---

# 21. Integrity Verification

Material records may use checksums, hashes, signatures, version histories, or other integrity mechanisms.

---

# 22. Authenticity

APIG should preserve evidence sufficient to establish the authenticity of important records where practical.

---

# 23. Accuracy

Records should be maintained as accurately as reasonably possible.

---

# 24. Uncertainty

Uncertain information should remain identified as uncertain.

---

# 25. No False Certainty

APIG must not convert uncertain information into a definitive fact merely for convenience.

---

# 26. Corrections

Material errors should be corrected without unnecessarily destroying the original record.

---

# 27. Correction History

Material corrections should remain historically traceable where practical.

---

# 28. Superseded Records

Superseded records should remain identifiable as superseded where historical preservation is required.

---

# 29. Deletion

Records may be deleted when authorized and when preservation is not required.

---

# 30. Destruction

Destruction of records should follow applicable authorization and retention requirements.

---

# 31. Retention

Records should be retained for as long as reasonably necessary according to their purpose and applicable requirements.

---

# 32. Retention Rules

Retention requirements may differ by record type.

---

# 33. Legal Hold

Where applicable, records subject to preservation requirements must not be destroyed.

---

# 34. Archiving

Important historical records may be moved to archival storage.

---

# 35. Archive Integrity

Archived records should remain protected against unauthorized alteration.

---

# 36. Retrieval

Authorized actors should be able to retrieve records needed for their functions.

---

# 37. Searchability

Records should be organized to permit efficient retrieval.

---

# 38. Metadata

Records should include useful metadata where practical.

Metadata may include:

- Record ID
- Type
- Source
- Date
- Version
- Status
- Authority
- Classification
- Relationships.

---

# 39. Folder Structure

APIG may use folders to organize records according to functional categories.

---

# 40. Resource Root

The APIG resource root contains the entry point for AI systems accessing APIG documentation.

---

# 41. Start Here

The Start Here document identifies the purpose and structure of the resource hierarchy.

---

# 42. Root Navigation

The Start Here document should identify where an AI should look for information relevant to its assigned task.

---

# 43. Specifications Folder

The Specifications folder contains APIG specifications governing system behavior and structure.

---

# 44. Specification Identification

Specifications should use consistent names and identifiers.

---

# 45. Specification Numbering

APIG specifications should use sequential identifiers where practical.

---

# 46. Specification Versioning

Material specification changes should create a new version.

---

# 47. Current Version

The active version should be identifiable.

---

# 48. Previous Versions

Previous versions should be preserved where historical traceability is required.

---

# 49. Change Record

Material changes should identify:

- What changed
- When it changed
- Why it changed
- Who authorized it where applicable.

---

# 50. Document Status

Documents may be marked:

- Draft
- Active
- Superseded
- Archived
- Deprecated.

---

# 51. Draft

A draft is not necessarily authoritative.

---

# 52. Active

An active document is currently applicable.

---

# 53. Superseded

A superseded document has been replaced by another version.

---

# 54. Archived

An archived document is preserved primarily for historical or reference purposes.

---

# 55. Deprecated

A deprecated document should no longer be relied upon for new operational decisions unless specifically required.

---

# 56. Authority of Documents

Not every document in the APIG resource hierarchy has equal authority.

---

# 57. Document Hierarchy

Documents should be interpreted according to their authority level.

---

# 58. Instruction vs Information

A document may contain information without granting authority to act.

---

# 59. External Documents

External documents should not automatically become APIG instructions.

---

# 60. External Data

External data should be treated according to its source and trust level.

---

# 61. Imported Data

Imported data should retain information about its origin where practical.

---

# 62. Data Provenance

Data provenance records where information originated and how it was transformed.

---

# 63. Provenance

Material data should retain provenance information where practical.

---

# 64. Chain of Custody

Sensitive or evidentiary records may require a chain-of-custody record.

---

# 65. Evidence

Evidence is information retained because it may establish or support a factual determination.

---

# 66. Evidence Preservation

Evidence should not be altered unnecessarily.

---

# 67. Evidence Copies

Working copies may be created while preserving the original.

---

# 68. Analytical Records

AI-generated analysis should be distinguishable from source evidence.

---

# 69. AI-Generated Content

AI-generated content should be identified as AI-generated where material.

---

# 70. AI Interpretation

An AI interpretation is not automatically a verified fact.

---

# 71. Human Verification

Human verification may be required for high-impact information.

---

# 72. Automated Verification

Automated validation may be used where appropriate.

---

# 73. Fact vs Assertion

APIG should distinguish:

- Verified fact
- Reported assertion
- Allegation
- Interpretation
- Opinion
- Unknown.

---

# 74. Allegation

An allegation must not automatically be recorded as an established fact.

---

# 75. Misconduct Records

Reports of misconduct should identify their evidentiary status.

---

# 76. Accountability Records

Accountability information should distinguish:

- Event
- Report
- Finding
- Determination
- Consequence.

---

# 77. Event

An event is an occurrence recorded by APIG.

---

# 78. Report

A report is an assertion or description submitted for review.

---

# 79. Finding

A finding is a determination reached through an applicable review process.

---

# 80. Determination

A determination is an authoritative conclusion made by the appropriate authority.

---

# 81. Consequence

A consequence is an action or result associated with a determination or event.

---

# 82. Event Relationships

Records may be linked to people, organizations, positions, jurisdictions, authorities, agencies, tasks, and other records.

---

# 83. Person Record

A person record may contain authorized information relating to an individual.

---

# 84. Organization Record

An organization record identifies an organization and its relevant relationships.

---

# 85. Position Record

A position record identifies an organizational role.

---

# 86. Authority Relationship

Records may identify who has authority over whom or over which function.

---

# 87. Supervisory Relationship

A supervisory relationship identifies direct managerial or supervisory authority.

---

# 88. Appointment Relationship

An appointment relationship identifies an appointing authority and the appointed position or person.

---

# 89. Oversight Relationship

An oversight relationship identifies a person or body with defined oversight responsibility.

---

# 90. Jurisdiction Relationship

A jurisdiction relationship identifies the governmental, geographic, organizational, or functional jurisdiction applicable to a record.

---

# 91. Downstream Relationship

A downstream relationship identifies entities or positions operating under a defined authority or oversight relationship.

---

# 92. Upstream Relationship

An upstream relationship identifies the authority or organizational source above an entity or position.

---

# 93. Relationship Direction

Relationships should identify their direction where direction affects accountability.

---

# 94. Relationship Type

Relationships should identify their type rather than simply linking two records without explanation.

---

# 95. Relationship History

Material relationships should remain historically traceable when they change.

---

# 96. Organizational Change

When authority structures change, historical relationships should not be rewritten as though the previous structure never existed.

---

# 97. Accountability Link

A record may be linked to every applicable authority relationship without automatically assigning responsibility for the underlying event.

---

# 98. No Automatic Guilt

A downstream or upstream relationship does not automatically establish personal wrongdoing.

---

# 99. Oversight vs Responsibility

Oversight, supervision, appointment authority, and personal responsibility are distinct concepts.

---

# 100. Attribution of Responsibility

Responsibility should be established according to applicable facts, authority, duties, and determinations.

---

# 101. Navigation

The APIG website should allow authorized users to navigate between related records.

---

# 102. Relationship Navigation

Users may navigate:

PERSON
→ POSITION
→ SUPERVISOR
→ APPOINTING AUTHORITY
→ ORGANIZATION
→ JURISDICTION.

---

# 103. Reverse Navigation

Users may also navigate:

AUTHORITY
→ ORGANIZATION
→ POSITIONS
→ PEOPLE
→ EVENTS
→ REPORTS
→ FINDINGS.

---

# 104. Record Linking

Related records should be linked rather than duplicated unnecessarily.

---

# 105. Canonical Record

Where possible, APIG should maintain one canonical record for a person, organization, position, or other persistent entity.

---

# 106. Duplicate Records

Duplicate records should be identified and resolved where practical.

---

# 107. Record Merge

Merging records must preserve relevant historical information.

---

# 108. Record Split

If a record was incorrectly combined, separation should preserve the original history where practical.

---

# 109. Identifier Stability

Identifiers should remain stable when the underlying entity remains the same.

---

# 110. Name Changes

A person's or organization's name may change without requiring a new identity record when the underlying entity remains the same.

---

# 111. Alias

Known aliases may be associated with the canonical record.

---

# 112. Historical Names

Historical names may be preserved where relevant.

---

# 113. Position Changes

A person moving between positions should retain the same person identity while receiving new position relationships.

---

# 114. Organizational Changes

An organization may change structure without requiring historical records to be rewritten.

---

# 115. Temporal Data

Records should support effective dates when relationships or facts change over time.

---

# 116. Effective Date

The effective date identifies when a record, relationship, or status becomes applicable.

---

# 117. End Date

The end date identifies when a relationship or status ceases to apply.

---

# 118. Historical State

APIG should be capable of representing what the organizational or authority structure was at a particular time where practical.

---

# 119. Current State

APIG should clearly distinguish current relationships from historical relationships.

---

# 120. Future State

Planned or scheduled changes should be distinguishable from current conditions.

---

# 121. Record Status

Every material record should have an identifiable status where practical.

---

# 122. Record Relationships

Records may relate through:

- Parent
- Child
- Authority
- Supervision
- Appointment
- Oversight
- Jurisdiction
- Dependency
- Evidence
- Source
- Derivation
- Reference.

---

# 123. Cross-References

Documents may reference related specifications and records.

---

# 124. Broken References

Broken references should be identified and repaired where practical.

---

# 125. Portable References

References should remain understandable when records are migrated between systems.

---

# 126. External URLs

External resources may be referenced when necessary.

---

# 127. URL Stability

External links should not be treated as permanent unless their continued availability is reasonably established.

---

# 128. Local Copies

Important external material may be preserved locally where authorized.

---

# 129. File Formats

APIG should favor durable, widely supported, machine-readable formats for core documentation.

---

# 130. Markdown

Markdown files may be used for specifications, instructions, documentation, and other structured text.

---

# 131. Plain Text

Plain-text files may be used for simple records and compatibility.

---

# 132. PDF

PDF may be used for stable presentation, archival copies, or human-readable distribution.

---

# 133. Structured Data

Structured formats such as JSON, CSV, or database records may be used when machine processing is required.

---

# 134. Source vs Presentation

A presentation format should not become the only source of critical machine-readable information when a structured source is available.

---

# 135. Code Documentation

When code is copied into an external service, APIG should retain documentation identifying:

- Where the code was used
- What the code does
- When it was deployed
- Which version was used
- What inputs it expects
- What outputs it produces
- What external dependencies exist.

---

# 136. External Platform Records

Examples include:

- Tally
- Google Sheets
- Website platforms
- APIs
- Automation systems
- Social media platforms.

---

# 137. Exact Code Preservation

When exact code is operationally important, the exact deployed or copied version should be preserved separately from explanatory documentation.

---

# 138. Code Documentation vs Code

Documentation explains code.

The exact code itself should be preserved in an appropriate source or text-based format.

---

# 139. Configuration Records

Important configuration settings should be documented.

---

# 140. Deployment Records

Material deployments should identify:

- System
- Version
- Date
- Responsible actor
- Purpose.

---

# 141. Change Comparison

Material changes should be comparable against the previous version where practical.

---

# 142. Backup

Important records should have appropriate backup mechanisms.

---

# 143. Backup Verification

Backups should be tested periodically where practical.

---

# 144. Recovery

APIG should be capable of recovering important records after system failure where practical.

---

# 145. Migration

Records should be structured so they can be migrated to another platform.

---

# 146. AI Migration

AI-provider migration should preserve the information required for another AI to continue the work.

---

# 147. AI Handoff Package

A portable task package may include:

- Task description
- Current status
- Relevant specifications
- Relevant records
- Authority context
- Constraints
- Dependencies
- Previous decisions
- Required outputs.

---

# 148. AI Resource Access

An AI should be directed to the relevant resource folders rather than receiving every APIG record for every task.

---

# 149. Task-Based Retrieval

AI systems should retrieve the minimum relevant documentation necessary for the assigned task where practical.

---

# 150. Resource Hierarchy

The resource hierarchy should allow an AI to determine:

START HERE
→ RELEVANT SPECIFICATION
→ RELEVANT FUNCTIONAL FOLDER
→ RELEVANT RECORD
→ RELEVANT TASK MATERIAL.

---

# 151. Root Document Maintenance

The Start Here document should be updated when the resource hierarchy itself changes.

---

# 152. Folder Creation

When a new functional resource category is created, the root document should identify the new category.

---

# 153. Existing Folder Changes

Adding or changing documents within an existing documented folder does not necessarily require changing the root document.

---

# 154. Record Discovery

AI systems should be able to discover relevant records through documented folder structure and metadata.

---

# 155. Indexing

A separate master index is not required when the resource hierarchy and document metadata provide sufficient discoverability.

---

# 156. Optional Index

APIG may create an index when the volume or complexity of records makes one useful.

---

# 157. Index Maintenance

An index should not become a single point of failure for resource discovery.

---

# 158. Resource Independence

Documents should remain understandable without requiring a proprietary AI system to interpret them.

---

# 159. AI Independence

Documentation should be usable by different AI providers.

---

# 160. Provider Migration

A new AI should be able to review the resource hierarchy and determine how APIG functions.

---

# 161. Portable Documentation

Core APIG documentation should use broadly supported formats where practical.

---

# 162. Human Readability

Core documentation should remain understandable to human operators.

---

# 163. Machine Readability

Core documentation should also remain reasonably interpretable by AI systems and software.

---

# 164. Documentation Consistency

Document naming and organization should remain consistent.

---

# 165. Naming Convention

APIG documents should use predictable names.

---

# 166. File Naming

File names should communicate:

- APIG identifier
- Subject
- Document type where useful.

---

# 167. Folder Naming

Folder names should clearly describe their function.

---

# 168. No Ambiguous Storage

Important records should not be stored in locations whose purpose is unclear.

---

# 169. Resource Separation

Specifications, operational instructions, records, and sensitive materials should be separated when appropriate.

---

# 170. Information Minimization

A task should not receive unrelated information merely because it is available.

---

# 171. Context Preservation

Information necessary to understand a decision should remain associated with that decision.

---

# 172. Decision Record

Material decisions should identify:

- Decision
- Date
- Authority
- Reason
- Alternatives where relevant
- Result.

---

# 173. Decision History

Material decisions should remain historically traceable.

---

# 174. Task Record

A task record should identify:

- Task
- Requester
- Authority
- Status
- Resources
- Result
- Relevant records.

---

# 175. Task Status

Tasks may be:

- Pending
- Active
- Paused
- Completed
- Failed
- Cancelled
- Deferred.

---

# 176. Failed Task

A failed task should not be represented as successfully completed.

---

# 177. Partial Completion

Partial results should be identified as partial.

---

# 178. AI Output Record

Material AI outputs may be retained as records.

---

# 179. AI Output Attribution

Material AI outputs should identify the AI system that produced them where practical.

---

# 180. AI Output Verification

AI output should not automatically be treated as verified fact.

---

# 181. AI Output Version

Material AI-generated work should retain the applicable model or system information where practical.

---

# 182. Prompt Context

Material AI decisions may require preservation of relevant task instructions and context.

---

# 183. Privacy

AI task records must not unnecessarily expose private or sensitive information.

---

# 184. Security

AI task records must follow applicable security controls.

---

# 185. Data Transfer

Transfers between systems should preserve record identity and provenance where practical.

---

# 186. Export

APIG should support export of important information in portable formats.

---

# 187. Import

Imported information should retain its source and import context where practical.

---

# 188. Migration Validation

After migration, important records should be checked for completeness and integrity.

---

# 189. Migration Failure

Migration failures should not silently destroy the source records.

---

# 190. System Independence

The information model should not depend on one vendor's database or AI system.

---

# 191. Vendor Independence

APIG should maintain enough documentation and data portability to change vendors when necessary.

---

# 192. Disaster Recovery

Important records should have recovery mechanisms appropriate to their importance.

---

# 193. Continuity

The loss of one AI provider should not eliminate APIG's core institutional knowledge.

---

# 194. Institutional Memory

The APIG resource hierarchy serves as persistent institutional memory.

---

# 195. AI Continuity

A new AI should be able to use the documentation to understand APIG without relying exclusively on the previous AI's conversational memory.

---

# 196. Core Principles

1. Records should remain identifiable.
2. Material records should retain their source where practical.
3. Material records should retain timestamps where practical.
4. Material records should remain attributable.
5. Information should be classified appropriately.
6. Access should follow authorization.
7. Original evidence should be preserved where necessary.
8. Derived analysis should remain distinguishable from source material.
9. Uncertainty must remain visible.
10. Allegations must not automatically become facts.
11. Findings must remain distinct from reports.
12. Determinations must remain distinct from allegations.
13. Relationships must identify their type.
14. Authority relationships should remain navigable.
15. Historical relationships should not be erased unnecessarily.
16. Oversight does not automatically establish personal responsibility.
17. A relationship does not automatically establish wrongdoing.
18. Material changes should be versioned.
19. Superseded records should remain identifiable where required.
20. Important records should be recoverable.
21. Documentation should be portable across AI providers.
22. Markdown and plain text are appropriate formats for core documentation.
23. PDF may serve as a presentation or archival format.
24. Structured data should be used when machine processing requires it.
25. Exact operational code should be preserved separately from code documentation.
26. External platform configurations should be documented.
27. AI-generated material should remain distinguishable from verified facts.
28. AI systems should retrieve task-relevant information rather than everything.
29. The resource root should direct AI systems to the appropriate folders.
30. A separate master index is optional, not mandatory.
31. The resource hierarchy should remain usable without a particular AI provider.
32. The APIG record system should preserve institutional knowledge through AI-provider changes.
33. The information system exists to preserve APIG's operational continuity, accountability, and institutional memory.

---

# 197. Data Management Sequence

SOURCE
→ RECORD
→ IDENTIFY
→ CLASSIFY
→ STORE
→ RELATE
→ VERSION
→ PROTECT
→ RETRIEVE
→ USE
→ AUDIT
→ ARCHIVE / DELETE.

---

# 198. AI Retrieval Sequence

TASK
→ IDENTIFY REQUIRED INFORMATION
→ READ START HERE
→ IDENTIFY RELEVANT FOLDER
→ READ RELEVANT SPECIFICATION
→ RETRIEVE RELEVANT RECORDS
→ APPLY AUTHORITY
→ PERFORM TASK
→ RECORD RESULT.

---

# 199. Migration Sequence

CURRENT SYSTEM
→ EXPORT
→ PRESERVE IDENTIFIERS
→ PRESERVE RELATIONSHIPS
→ PRESERVE VERSIONS
→ PRESERVE AUTHORITY
→ IMPORT
→ VALIDATE
→ VERIFY
→ CONTINUE OPERATIONS.

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

# END OF APIG-24