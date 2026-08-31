# APIG-19 — Source, Provenance, and Evidence Specification

## Status

Active

## Purpose

This specification defines how APIG identifies, evaluates, preserves, and presents the sources and evidence underlying information, claims, events, relationships, decisions, and accountability records.

The fundamental principle is:

CLAIM
→ SOURCE
→ PROVENANCE
→ VERIFICATION
→ CLASSIFICATION
→ CONTEXT
→ PRESENTATION.

---

# 1. Core Principle

APIG should distinguish between:

- What is claimed
- Who made the claim
- Where the information came from
- When it originated
- Whether it has been verified
- What evidence supports it
- What remains uncertain

---

# 2. Source

A source is the origin of information used by APIG.

Sources may include:

- Government records
- Court records
- Laws
- Regulations
- Policies
- Organizational documents
- Official websites
- Public statements
- News reports
- Social media
- User submissions
- AI-generated information
- Internal records
- External databases
- Other documented materials.

---

# 3. Primary Sources

A primary source is a source that directly records, establishes, or originates the information being evaluated.

Examples may include:

- Statutes
- Court orders
- Official minutes
- Government records
- Organizational resolutions
- Original filings
- Official statements.

---

# 4. Secondary Sources

A secondary source reports, interprets, summarizes, or analyzes information originating elsewhere.

Examples may include:

- News reports
- Research articles
- Commentary
- Analytical reports
- Summaries.

---

# 5. Tertiary Sources

Tertiary sources aggregate or organize information from other sources.

---

# 6. Source Hierarchy

APIG should prefer authoritative primary sources when available.

Secondary and tertiary sources may provide useful context but should not automatically replace stronger primary evidence.

---

# 7. Source Authority

Source authority depends on the subject being evaluated.

A government source may be authoritative for a governmental fact.

A court record may be authoritative for a judicial proceeding.

An organizational document may be authoritative for that organization's internal structure.

---

# 8. No Universal Source Authority

No source is automatically authoritative for every type of claim.

---

# 9. Source Reliability

APIG should evaluate the reliability of sources according to:

- Authority
- Proximity to the underlying event
- Authenticity
- Consistency
- Corroboration
- Timeliness
- Known limitations.

---

# 10. Source Authenticity

Where practical, APIG should determine whether a source is authentic.

---

# 11. Source Identity

APIG should preserve enough information to identify the source.

---

# 12. Source Location

Where appropriate, APIG should preserve the source location or reference.

---

# 13. Source Date

APIG should preserve publication, filing, creation, or access dates where available.

---

# 14. Retrieval Date

For information obtained from changing sources, APIG should preserve when the information was retrieved.

---

# 15. Source Version

Where a source changes over time, APIG should preserve the applicable version when practical.

---

# 16. Historical Sources

Historical sources should remain identifiable as historical sources.

---

# 17. Current Sources

Current information should be distinguishable from historical information.

---

# 18. Source Provenance

Provenance describes the history and origin of information.

---

# 19. Provenance Chain

Where practical, APIG should represent:

INFORMATION
→ SOURCE
→ ORIGINAL SOURCE
→ TRANSFORMATION
→ VERIFICATION
→ CURRENT RECORD.

---

# 20. Transformation

If information is summarized, translated, normalized, extracted, or otherwise transformed, the transformation should remain attributable where material.

---

# 21. AI Transformation

AI-generated summaries must not erase the identity of the underlying source.

---

# 22. AI Summary

An AI summary is not itself a replacement for the source.

---

# 23. AI Citation

Where appropriate, AI-generated claims should reference the underlying source.

---

# 24. AI Hallucination

AI-generated information must not be treated as established fact solely because an AI generated it.

---

# 25. Verification

Verification is the process of determining whether a claim is sufficiently supported.

---

# 26. Verification Status

APIG should support statuses such as:

- Unverified
- Partially verified
- Corroborated
- Verified
- Disputed
- Contradicted
- Unknown.

---

# 27. Verification Does Not Mean Certainty

Verification indicates that the available evidence supports the claim according to the applicable standard.

---

# 28. Evidence

Evidence is information used to support, contradict, contextualize, or evaluate a claim.

---

# 29. Evidence Types

Evidence may include:

- Documents
- Records
- Statements
- Images
- Videos
- Audio
- Databases
- Official actions
- Correspondence
- Other source material.

---

# 30. Direct Evidence

Direct evidence directly supports a proposition.

---

# 31. Circumstantial Evidence

Circumstantial evidence supports a proposition indirectly.

---

# 32. Corroboration

Corroboration occurs when independent evidence supports the same proposition.

---

# 33. Independent Sources

Multiple copies of the same underlying source should not automatically be treated as independent corroboration.

---

# 34. Duplicate Information

APIG should detect duplicate or derivative sources where practical.

---

# 35. Conflicting Sources

Conflicting sources should not be silently reconciled without justification.

---

# 36. Conflict Representation

Where material sources disagree, APIG should preserve the disagreement.

---

# 37. Source Comparison

APIG should be able to compare relevant sources when necessary.

---

# 38. Source Priority

When sources conflict, priority should consider:

- Legal authority
- Directness
- Authenticity
- Recency
- Corroboration
- Jurisdiction
- Subject-matter authority.

---

# 39. Legal Claims

Claims about law should preferably reference authoritative legal sources.

---

# 40. Government Claims

Claims about government structure should preferably reference official governmental sources or controlling law.

---

# 41. Organizational Claims

Claims about organizational structure should preferably reference governing documents or authoritative organizational records.

---

# 42. Appointment Claims

Claims about appointment authority should reference the applicable law, resolution, governing document, or other authoritative source.

---

# 43. Supervisory Claims

Claims about supervision should reference the actual organizational structure rather than assuming that titles establish supervision.

---

# 44. Accountability Claims

Claims about accountability should identify the relationship that creates the accountability.

---

# 45. Conduct Claims

Claims about misconduct should identify the source establishing the alleged conduct.

---

# 46. Allegation

An allegation is a claim that has not yet been established as a verified finding.

---

# 47. Report

A report records that information or an allegation was reported.

---

# 48. Investigation

An investigation represents a process undertaken to evaluate an allegation or event.

---

# 49. Finding

A finding represents an official or otherwise appropriately supported determination.

---

# 50. Confirmed Event

A confirmed event is an event for which APIG has sufficient evidence to represent the event as established under the applicable standard.

---

# 51. Disputed Event

A disputed event is an event or claim for which material disagreement exists.

---

# 52. Unknown

Unknown means APIG does not currently possess sufficient information to establish the relevant fact.

---

# 53. No Inference From Absence

The absence of a record does not automatically establish that an event did not occur.

---

# 54. No Inference From Presence

The existence of a report does not automatically establish that the reported event occurred.

---

# 55. No Guilt by Association

A person's relationship to an event does not establish that the person participated in the event.

---

# 56. Accountability Association

An event may be linked to a supervisor, governing body, appointing authority, or other responsible authority when the relationship is relevant to oversight.

The link must identify the nature of the relationship.

---

# 57. Direct Conduct

Direct conduct must be attributed to the actor who actually engaged in it.

---

# 58. Oversight

Oversight must be represented separately from direct conduct.

---

# 59. Appointment

Appointment authority must be represented separately from supervision.

---

# 60. Governance

Governance authority must be represented separately from personal participation.

---

# 61. Source-to-Entity Link

APIG should support links between sources and entities.

Examples:

SOURCE
→ PERSON

SOURCE
→ ORGANIZATION

SOURCE
→ EVENT

SOURCE
→ POSITION

SOURCE
→ LAW

SOURCE
→ JURISDICTION.

---

# 62. Source-to-Claim Link

APIG should support direct links between sources and claims.

---

# 63. Claim-to-Evidence Link

APIG should support links between claims and supporting or contradicting evidence.

---

# 64. Evidence-to-Event Link

Evidence may support the existence, timing, nature, or context of an event.

---

# 65. Event-to-Authority Link

Events may be linked to applicable authority structures without implying personal participation by upstream authorities.

---

# 66. Provenance Graph

APIG may represent source relationships as a provenance graph.

---

# 67. Source Metadata

Where available, APIG should preserve:

- Source title
- Source type
- Publisher
- Author
- Date
- Location
- Version
- Retrieval date
- Identifier
- Verification status.

---

# 68. Source Integrity

APIG should preserve source integrity where practical.

---

# 69. Original Documents

When practical, APIG should preserve or reference original documents rather than relying solely on summaries.

---

# 70. Document Preservation

Important documents should be preserved according to applicable retention requirements.

---

# 71. Immutable Evidence

Where appropriate, evidence may be preserved in a form that makes unauthorized alteration detectable.

---

# 72. Hashes and Integrity Records

Digital evidence may use integrity mechanisms such as cryptographic hashes where appropriate.

---

# 73. Chain of Custody

High-impact evidence may require documentation of its custody and handling.

---

# 74. Evidence Handling

Evidence should not be altered unnecessarily.

---

# 75. Evidence Copies

Copies should remain distinguishable from originals where material.

---

# 76. Screenshots

Screenshots may preserve a representation of information but should not automatically be treated as equivalent to the original source.

---

# 77. Social Media Evidence

Social media information should preserve:

- Platform
- Account
- Post or message identifier where available
- Date
- Retrieval date
- Relevant surrounding context.

---

# 78. Social Media Identity

A social-media account should not automatically be treated as authentic merely because it uses a person's name.

---

# 79. Public Messages

Public messages may be evidence of what was communicated without necessarily establishing the truth of every statement contained within the message.

---

# 80. Private Messages

Private communications require appropriate privacy and authorization controls.

---

# 81. User Submissions

User-submitted information should be identified as user-submitted information.

---

# 82. Contributor Submissions

Contributor submissions should identify the contributing actor where appropriate.

---

# 83. Anonymous Submissions

Anonymous submissions may be accepted where permitted, but their source limitations should remain clear.

---

# 84. Source Credibility

Anonymous information may require additional corroboration before being treated as established fact.

---

# 85. Source Bias

Potential source bias should be considered where relevant.

---

# 86. Conflicts of Interest

Material conflicts of interest affecting a source should be represented where relevant.

---

# 87. Editorial Independence

Source evaluation should not be changed merely because a source is politically, organizationally, or personally inconvenient.

---

# 88. Equal Standards

Comparable claims should be evaluated using comparable standards.

---

# 89. Evidence Threshold

The required evidence threshold may vary according to the consequence of the claim.

---

# 90. High-Impact Claims

Claims capable of materially harming a person's reputation or rights require heightened care.

---

# 91. Public Interest

Public interest may justify publication of certain information but does not eliminate the need for evidence and context.

---

# 92. Right Context

APIG should provide enough context to prevent a source from being misleadingly interpreted.

---

# 93. Source Context

A quotation, image, document, or statement should not be selectively presented in a manner that materially changes its meaning.

---

# 94. Temporal Context

Information should be interpreted according to the circumstances existing at the relevant time.

---

# 95. Jurisdictional Context

Legal and governmental information should be interpreted within the applicable jurisdiction.

---

# 96. Organizational Context

Organizational information should be interpreted according to the organization's actual governing structure.

---

# 97. Identity Context

Evidence should be associated with the correct person or entity.

---

# 98. Similar Names

APIG must avoid conflating people or organizations with similar names.

---

# 99. Entity Resolution

Where identity is uncertain, APIG should represent the uncertainty rather than merging records without sufficient evidence.

---

# 100. Source Corrections

If a source is corrected, APIG should preserve the correction where material.

---

# 101. Retracted Sources

Retracted or withdrawn sources should remain identifiable as such where historically relevant.

---

# 102. Deleted Sources

If a source disappears from the original location, APIG should preserve available provenance information where legally and practically appropriate.

---

# 103. Broken Links

A broken link should not cause the underlying provenance record to disappear.

---

# 104. Archived Sources

Archived copies may be used to preserve historical context.

---

# 105. Archive Authenticity

Archived information should be identified as archived material.

---

# 106. Source Date Changes

If a source's contents change after APIG retrieves it, APIG should distinguish the historical version from the current version when material.

---

# 107. Dynamic Websites

Dynamic websites should be treated as potentially changing sources.

---

# 108. Retrieval Evidence

For important dynamic-source claims, APIG should preserve sufficient retrieval information to reconstruct what was observed where practical.

---

# 109. API Sources

Information obtained through APIs should preserve the originating service and relevant retrieval metadata where practical.

---

# 110. Database Sources

Database-derived information should preserve the originating database where appropriate.

---

# 111. AI Sources

Information produced by AI should identify the AI-generated nature of the content where material.

---

# 112. AI Reasoning

Private model reasoning does not become evidence merely because an AI used it to reach an answer.

---

# 113. AI Confidence

AI confidence is not equivalent to evidence.

---

# 114. AI Verification

AI claims should be independently verified when they are material to consequential decisions.

---

# 115. Automated Verification

Automated verification may be used where reliable mechanisms exist.

---

# 116. Human Verification

Human verification may be required for high-impact information.

---

# 117. Verification Record

Material verification should identify:

- What was verified
- Against what source
- By whom or what system
- When
- Result
- Limitations.

---

# 118. Verification Changes

Verification status may change as new evidence becomes available.

---

# 119. Evidence Updates

New evidence should not silently overwrite the historical evidence record.

---

# 120. Evidence Versioning

Material evidence changes should be versioned where practical.

---

# 121. Claim Versioning

Material claims may require version history.

---

# 122. Source Versioning

Material source versions should remain distinguishable.

---

# 123. Provenance Preservation

Provenance should survive transformations of information.

---

# 124. Migration

When APIG data is migrated between systems, provenance must remain associated with the information where practical.

---

# 125. AI Provider Migration

Changing AI providers must not destroy source provenance.

---

# 126. Data Portability

Source and evidence metadata should use portable representations where practical.

---

# 127. External AI Review

A replacement AI should be able to determine where important information came from.

---

# 128. Resource Folder Integration

The APIG resource hierarchy may contain source documents, specifications, evidence records, and reference materials.

Each should be distinguishable by purpose.

---

# 129. Specification Sources

Specifications should identify their authoritative source where applicable.

---

# 130. Operational Documentation

Operational documentation should identify whether it represents:

- Policy
- Procedure
- Current configuration
- Historical configuration
- Example
- Draft
- Proposal.

---

# 131. Code Documentation

Documentation describing externally entered code should identify:

- Destination system
- Purpose
- Current status
- Date
- Source
- Relevant version
- Known dependencies.

---

# 132. Exact Code Preservation

When code is copied into an external system, APIG should preserve the exact version used when practical.

---

# 133. Code vs Documentation

Code and documentation should remain separate resources.

Documentation may explain code without replacing the actual code record.

---

# 134. External Configuration

External configurations should preserve their source and version where practical.

---

# 135. Operational History

Material operational changes should remain historically traceable.

---

# 136. Current State

APIG should distinguish current state from historical state.

---

# 137. Proposed State

Proposed changes should be distinguishable from implemented changes.

---

# 138. Draft Information

Draft information should not automatically be treated as final.

---

# 139. Official Information

Official information should be identified according to its actual source and authority.

---

# 140. Unsupported Claims

Unsupported claims should not be represented as verified facts.

---

# 141. Missing Evidence

When evidence is unavailable, APIG should state that evidence is unavailable rather than inventing support.

---

# 142. Uncertainty

Uncertainty should be explicitly represented where material.

---

# 143. Confidence

Confidence may be represented separately from verification status.

---

# 144. Confidence Is Not Truth

A confidence score does not transform an uncertain claim into an established fact.

---

# 145. Source Ranking

Source rankings should be explainable where practical.

---

# 146. Search Results

Search results are discovery mechanisms and are not automatically authoritative evidence.

---

# 147. Search Snippets

Search-result snippets should not automatically be treated as complete representations of the underlying source.

---

# 148. Search Verification

Important claims discovered through search should be verified against the underlying source.

---

# 149. External AI Search

AI-generated search summaries should not replace review of authoritative source material for consequential claims.

---

# 150. Evidence and Public Display

Public displays should communicate evidence status clearly enough to avoid misleading interpretation.

---

# 151. Evidence and Accountability

Accountability relationships should be supported by evidence establishing the underlying authority relationship.

---

# 152. Evidence and Jurisdiction

Jurisdictional claims should be supported by the appropriate legal or governmental sources.

---

# 153. Evidence and Organizational Structure

Organizational relationships should be supported by appropriate organizational or governmental sources.

---

# 154. Evidence and Misconduct

Misconduct claims should identify the source and status of the underlying allegation or finding.

---

# 155. Evidence and Reputation

The stronger the potential reputational impact, the greater the need for careful source evaluation, context, and verification.

---

# 156. No Fabrication

APIG must never fabricate a source, citation, evidence record, verification status, or provenance chain.

---

# 157. No False Citation

A source must not be represented as supporting a claim when it does not support the claim.

---

# 158. No Citation Laundering

Multiple sources repeating an unsupported claim do not automatically create independent evidence.

---

# 159. No Provenance Laundering

Transforming an unsupported claim through multiple AI or human systems does not create authoritative provenance.

---

# 160. No Authority Laundering

A claim does not become authoritative merely because it appears inside an official-looking document.

---

# 161. Evidence Review

High-impact claims should be reviewable against their underlying evidence.

---

# 162. Source Navigation

Where appropriate, users should be able to navigate from a claim to its supporting sources.

---

# 163. Evidence Navigation

Where appropriate, users should be able to navigate from an event to supporting evidence.

---

# 164. Provenance Navigation

Where appropriate, users should be able to trace information backward through its provenance chain.

---

# 165. Authority Navigation

Where appropriate, users should be able to trace an authority relationship back to its source.

---

# 166. Historical Navigation

Where appropriate, users should be able to examine historical versions of important information.

---

# 167. Privacy Controls

Source and evidence navigation must remain subject to privacy and authorization controls.

---

# 168. Restricted Evidence

Restricted evidence must not become publicly accessible merely because it supports a public claim.

---

# 169. Sensitive Sources

Sensitive source identities may require protection.

---

# 170. Confidential Evidence

Confidential evidence should be disclosed only to authorized actors.

---

# 171. Source Security

Sources containing credentials or security-sensitive information must receive appropriate protection.

---

# 172. Evidence Security

Evidence must be protected against unauthorized alteration or disclosure.

---

# 173. Auditability

Material provenance changes should be auditable.

---

# 174. Change Attribution

Material changes to evidence or source records should identify the responsible actor or system.

---

# 175. Record Integrity

Source and evidence records should remain internally consistent.

---

# 176. Duplicate Records

Duplicate records should not create the appearance of independent evidence.

---

# 177. Merge Operations

When records are merged, the underlying provenance should remain recoverable.

---

# 178. Split Operations

When records are separated, their source histories should remain recoverable.

---

# 179. Entity Corrections

Correcting an entity association should preserve the history of the correction where material.

---

# 180. Source Disputes

Disputes concerning source authenticity or interpretation should be represented where relevant.

---

# 181. Evidence Disputes

Material disputes concerning evidence should be preserved.

---

# 182. Review Status

Evidence may have review states such as:

- Not reviewed
- Under review
- Reviewed
- Escalated
- Resolved.

---

# 183. Reviewer Attribution

Material human review should identify the reviewer where appropriate.

---

# 184. Automated Review Attribution

Automated review should identify the responsible system where practical.

---

# 185. Review Limitations

Review records should identify material limitations where relevant.

---

# 186. Source Expiration

Some sources may become outdated.

APIG should distinguish current validity from historical usefulness.

---

# 187. Current Validity

A historical source may remain valid as evidence of what was true or recorded at the time while no longer describing the current state.

---

# 188. Historical Truth

APIG should preserve historical context rather than rewriting history solely to reflect current conditions.

---

# 189. Current Truth

Current claims should be evaluated against current authoritative sources where available.

---

# 190. Temporal Reconciliation

When historical and current sources differ, APIG should determine whether the difference reflects a change over time.

---

# 191. Source Lifecycle

Sources may move through:

DISCOVERED
→ CAPTURED
→ REVIEWED
→ VERIFIED
→ PUBLISHED
→ UPDATED
→ ARCHIVED.

---

# 192. Evidence Lifecycle

Evidence may move through:

RECEIVED
→ CLASSIFIED
→ PRESERVED
→ REVIEWED
→ CORROBORATED
→ USED
→ ARCHIVED.

---

# 193. Claim Lifecycle

Claims may move through:

PROPOSED
→ REPORTED
→ REVIEWED
→ VERIFIED / DISPUTED / REJECTED
→ UPDATED
→ ARCHIVED.

---

# 194. Source-to-Decision Traceability

Material decisions should be traceable to the information and authority underlying them where practical.

---

# 195. AI Decision Traceability

When AI makes a consequential recommendation, the relevant source material and authorization context should remain identifiable where practical.

---

# 196. AI Action Traceability

When AI performs a consequential action, APIG should preserve the relevant task, authority, and source context where practical.

---

# 197. Migration Traceability

Moving information to another AI system should preserve provenance and source references.

---

# 198. Resource Folder Principle

The APIG resource hierarchy is intended to allow a replacement AI system to enter the root resource document, identify the relevant specification, and follow the documented resource structure.

---

# 199. Root Resource Relationship

The root resource document should identify this specification as the primary resource for source evaluation, evidence, provenance, verification, claims, citations, historical records, and information traceability.

---

# 200. Core Principles

1. Claims must remain distinguishable from evidence.
2. Sources must remain identifiable.
3. Provenance must survive transformation.
4. Primary sources should be preferred when available.
5. Source authority depends on the subject.
6. Multiple copies of one source are not independent corroboration.
7. Conflicting sources should not be silently reconciled.
8. Verification status must remain explicit.
9. Allegations must remain distinguishable from findings.
10. Absence of evidence does not automatically prove absence of an event.
11. Presence of a report does not automatically prove the reported event.
12. AI-generated information is not automatically authoritative.
13. AI confidence is not evidence.
14. Important claims should be independently verified.
15. High-impact claims require heightened care.
16. Direct conduct must remain separate from oversight.
17. Appointment must remain separate from supervision.
18. Accountability relationships must be supported by evidence.
19. Public transparency must not override privacy controls.
20. Restricted evidence must remain protected.
21. Sources must never be fabricated.
22. Citations must accurately support the claims they accompany.
23. Provenance must not be laundered through repeated summaries.
24. Historical and current information must remain distinguishable.
25. Material changes should remain attributable.
26. Evidence should remain traceable.
27. Source records should remain portable.
28. AI provider changes must not destroy provenance.
29. Replacement AI systems must be able to reconstruct important information sources.
30. APIG must preserve the distinction between what is known, what is claimed, what is supported, and what remains unknown.

---

# 201. Source Evaluation Sequence

CLAIM
→ IDENTIFY SOURCE
→ DETERMINE SOURCE AUTHORITY
→ CHECK AUTHENTICITY
→ CHECK DATE
→ CHECK CONTEXT
→ SEEK CORROBORATION
→ DETERMINE VERIFICATION STATUS
→ RECORD PROVENANCE
→ PRESENT WITH APPROPRIATE CONTEXT.

---

# 202. High-Impact Claim Sequence

CLAIM
→ IDENTIFY ACTOR / ENTITY
→ IDENTIFY SOURCE
→ PRESERVE ORIGINAL EVIDENCE
→ VERIFY IDENTITY
→ VERIFY EVENT
→ CHECK JURISDICTION
→ CHECK TEMPORAL CONTEXT
→ CHECK CONTRADICTING EVIDENCE
→ CLASSIFY CLAIM
→ PRESENT WITHOUT FALSE ATTRIBUTION.

---

# 203. AI Research Sequence

QUESTION
→ IDENTIFY REQUIRED FACTS
→ FIND AUTHORITATIVE SOURCES
→ REVIEW SOURCES
→ EXTRACT INFORMATION
→ PRESERVE PROVENANCE
→ CROSS-CHECK MATERIAL CLAIMS
→ IDENTIFY UNCERTAINTY
→ ANSWER
→ PROVIDE SOURCE PATHS WHERE APPROPRIATE.

---

# 204. AI Migration Sequence

CURRENT AI
→ PRESERVE TASK
→ PRESERVE AUTHORITY
→ PRESERVE SOURCE REFERENCES
→ PRESERVE CURRENT STATE
→ PRESERVE RELEVANT HISTORY
→ TRANSFER MINIMUM NECESSARY CONTEXT
→ NEW AI
→ REVIEW ROOT RESOURCE
→ REVIEW RELEVANT SPECIFICATIONS
→ CONTINUE TASK.

---

# 205. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-19