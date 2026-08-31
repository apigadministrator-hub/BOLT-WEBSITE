# APIG-30 — Evidence, Verification, and Source Evaluation Specification

## Status

Active

## Purpose

This specification defines how APIG evaluates information, evidence, sources, claims, allegations, records, and conclusions so that the system can distinguish verified information from unverified information and AI analysis.

The fundamental principle is:

CLAIM
→ SOURCE
→ EVIDENCE
→ VERIFICATION
→ CONTEXT
→ CONFIDENCE
→ CONCLUSION
→ RECORD.

---

# 1. Core Principle

APIG must distinguish what is known, what is reported, what is alleged, what is inferred, what is estimated, and what has been verified.

---

# 2. Information

Information is any material received, generated, observed, retrieved, or recorded by APIG.

---

# 3. Claim

A claim is an assertion that something is true.

---

# 4. Fact

A fact is information sufficiently established for the applicable purpose.

---

# 5. Reported Information

Reported information is information provided by another source that has not necessarily been independently verified.

---

# 6. Allegation

An allegation is a claim of misconduct, wrongdoing, or other behavior that has not yet been established.

---

# 7. Finding

A finding is a conclusion reached through an appropriate evaluation of available evidence.

---

# 8. Evidence

Evidence is information that supports, contradicts, or otherwise informs evaluation of a claim or conclusion.

---

# 9. Source

A source is the origin of information.

---

# 10. Primary Source

A primary source directly originates from the person, organization, system, event, or official record being evaluated.

---

# 11. Secondary Source

A secondary source reports, summarizes, interprets, or republishes information originating elsewhere.

---

# 12. Tertiary Source

A tertiary source aggregates information from multiple sources.

---

# 13. Official Source

An official source is produced or maintained by an entity with recognized authority over the subject.

---

# 14. Independent Source

An independent source is sufficiently separate from the subject being evaluated to provide potentially independent corroboration.

---

# 15. Anonymous Source

An anonymous source is a source whose identity is not disclosed or cannot be established.

---

# 16. Source Identity

Where material, the identity of a source should be established and preserved.

---

# 17. Source Reliability

Source reliability concerns the likelihood that a source provides accurate information.

---

# 18. Source Authority

Source authority concerns the source's legitimate authority concerning the subject.

---

# 19. Source Reliability Versus Authority

A source may be reliable without having authority over the subject.

---

# 20. Source Authority Versus Reliability

An authoritative source may still contain errors or outdated information.

---

# 21. Source Recency

The date of information may affect its relevance.

---

# 22. Historical Source

A historical source may accurately describe a past condition even when it no longer describes the current condition.

---

# 23. Current Source

A current source describes information applicable to the relevant present period.

---

# 24. Temporal Relevance

Evidence must be evaluated against the time period relevant to the question.

---

# 25. Jurisdictional Relevance

Evidence must be evaluated against the jurisdiction relevant to the question.

---

# 26. Scope Relevance

Evidence must be evaluated against the precise claim being examined.

---

# 27. Context

Information should be evaluated in its surrounding context.

---

# 28. Context Loss

Removing relevant context may materially change the meaning of information.

---

# 29. Exact Quote

Where a statement's exact wording is material, the original wording should be preserved.

---

# 30. Paraphrase

A paraphrase should remain faithful to the source's meaning.

---

# 31. Interpretation

Interpretation explains what information may mean.

---

# 32. Inference

An inference is a conclusion drawn from available information rather than directly stated by the source.

---

# 33. AI Inference

An AI inference must remain distinguishable from source information.

---

# 34. AI Conclusion

An AI conclusion must not be represented as an independently verified fact unless verification has occurred.

---

# 35. AI Hallucination

AI-generated information that lacks adequate source support must not be treated as evidence merely because the AI produced it.

---

# 36. Verification

Verification is the process of determining whether information is sufficiently supported for the applicable purpose.

---

# 37. Independent Verification

Independent verification uses a source or method sufficiently separate from the original source.

---

# 38. Corroboration

Corroboration occurs when multiple relevant sources support substantially the same information.

---

# 39. Corroboration Is Not Automatic Proof

Multiple sources repeating the same original claim do not necessarily constitute independent corroboration.

---

# 40. Source Independence

Sources should be evaluated for whether they are actually independent of one another.

---

# 41. Circular Reporting

Multiple sources may appear to corroborate information while ultimately relying on the same original source.

---

# 42. Evidence Weight

Evidence may be assigned greater or lesser weight according to:

- Reliability
- Authority
- Independence
- Recency
- Specificity
- Completeness
- Directness
- Consistency.

---

# 43. Evidence Hierarchy

Evidence should not be ranked by a universal hierarchy without considering the specific question.

---

# 44. Direct Evidence

Direct evidence directly establishes an aspect of a claim.

---

# 45. Circumstantial Evidence

Circumstantial evidence supports a conclusion indirectly.

---

# 46. Documentary Evidence

Documentary evidence includes written, electronic, or recorded documentation.

---

# 47. Digital Evidence

Digital evidence includes information originating from digital systems.

---

# 48. System Evidence

System evidence includes logs, audit trails, configurations, timestamps, and other system-generated information.

---

# 49. Physical Evidence

Physical evidence consists of tangible objects or conditions relevant to a matter.

---

# 50. Testimonial Evidence

Testimonial evidence consists of statements made by a person.

---

# 51. Publicly Available Evidence

Publicly available information may be evidence but must still be evaluated for reliability and context.

---

# 52. Social Media Evidence

Social-media content may be evidence but must be evaluated for authenticity, authorship, context, timing, and reliability.

---

# 53. Screenshot

A screenshot may preserve visual evidence but may omit surrounding information.

---

# 54. Screenshot Verification

Where material, the underlying source should be checked rather than relying solely on a screenshot.

---

# 55. Message Evidence

Messages may be evidence concerning communications, instructions, claims, or events.

---

# 56. Message Authorship

The identity of the person who actually authored a message should be distinguished from the account through which it was sent.

---

# 57. Account Evidence

Account information may help establish the origin of a message but does not automatically prove the identity of the person using the account.

---

# 58. Metadata

Metadata may provide information about creation, modification, origin, location, format, or other characteristics.

---

# 59. Metadata Reliability

Metadata should be evaluated for authenticity and the possibility of alteration.

---

# 60. Timestamp

A timestamp records a time associated with an event or record.

---

# 61. Timestamp Interpretation

A timestamp must be interpreted according to its time zone, system, source, and meaning.

---

# 62. Date Conflict

Conflicting dates should be identified rather than silently reconciled.

---

# 63. Source Conflict

Conflicting sources should be identified and evaluated.

---

# 64. Contradictory Evidence

Evidence contradicting a claim must not be ignored merely because other evidence supports the claim.

---

# 65. Negative Evidence

The absence of expected evidence may be relevant but does not automatically prove that an event did not occur.

---

# 66. Absence of Record

An absence of a record does not necessarily establish that the underlying event did not occur.

---

# 67. Missing Evidence

Missing evidence should be documented when its absence affects confidence.

---

# 68. Evidence Destruction

Evidence that may have been altered, destroyed, or lost should be identified.

---

# 69. Evidence Preservation

Material evidence should be preserved where appropriate.

---

# 70. Chain of Custody

Material evidence may require documentation of possession and transfer.

---

# 71. Evidence Authenticity

Where material, APIG should establish that evidence is genuine.

---

# 72. Evidence Integrity

Material evidence should be protected against unauthorized alteration.

---

# 73. Original Source

Where possible, APIG should prefer access to the original source rather than relying exclusively on reproductions.

---

# 74. Copy Verification

A copy should be checked against the source where practical when exactness matters.

---

# 75. Altered Evidence

Potentially altered evidence should be identified.

---

# 76. Fabricated Evidence

Evidence reasonably believed to be fabricated should not be treated as authentic evidence.

---

# 77. Manipulated Evidence

Potential manipulation should be documented and investigated where material.

---

# 78. Source Preservation

Material sources should be preserved where practical.

---

# 79. Source Location

The location from which material information was obtained should be recorded where practical.

---

# 80. External URL

When an external website materially supports a record, the source location should be preserved where practical.

---

# 81. Link Stability

External links may become unavailable or change over time.

---

# 82. Source Snapshot

Where appropriate, APIG may preserve a copy, capture, or other representation of the source as it existed when reviewed.

---

# 83. Source Date

The date the source was reviewed should be recorded where material.

---

# 84. Retrieval Date

The date information was retrieved should be distinguished from the date the underlying information was created.

---

# 85. Source Version

A source may have multiple versions.

---

# 86. Historical Source Version

The version applicable at the relevant historical time should be used when necessary.

---

# 87. Current Source Substitution

A current source must not automatically replace a historical source when evaluating a past event.

---

# 88. Verification Status

Information may be classified as:

- Unverified
- Reported
- Partially verified
- Corroborated
- Verified
- Disputed
- Refuted
- Unknown.

---

# 89. Unverified

Information has not been sufficiently evaluated.

---

# 90. Reported

Information has been attributed to a source but remains unverified.

---

# 91. Partially Verified

Some aspects of the information have been established while others remain uncertain.

---

# 92. Corroborated

Relevant independent sources support the information.

---

# 93. Verified

The information has been sufficiently established for the applicable purpose.

---

# 94. Disputed

A material dispute exists concerning the information.

---

# 95. Refuted

Available evidence materially contradicts the information.

---

# 96. Unknown

Available information is insufficient to determine the truth.

---

# 97. Confidence

Confidence describes the degree to which APIG can reasonably rely on a conclusion.

---

# 98. Confidence Is Not Truth

High confidence does not guarantee that a conclusion is correct.

---

# 99. Low Confidence

Low confidence indicates meaningful uncertainty.

---

# 100. Confidence Factors

Confidence may consider:

- Source quality
- Evidence quality
- Corroboration
- Contradictions
- Completeness
- Temporal relevance
- Jurisdiction
- Identity certainty.

---

# 101. Confidence Change

Confidence should change when material new evidence is received.

---

# 102. Evidence Update

New evidence should not be ignored because an earlier conclusion was already recorded.

---

# 103. Correction

Material factual errors should be corrected.

---

# 104. Historical Preservation

Corrections should preserve relevant historical information rather than silently rewriting the record.

---

# 105. Finding Revision

A finding may be revised when material evidence changes the underlying analysis.

---

# 106. Finding Authority

Material findings should identify the authority or process responsible for making the finding where applicable.

---

# 107. AI Finding

An AI-generated finding should be identified as AI analysis unless an authorized human or authority has adopted it as an official finding.

---

# 108. AI Research

AI research should preserve the distinction between retrieved source material and AI-generated synthesis.

---

# 109. AI Source Citation

Material AI-generated factual claims should be traceable to their sources where practical.

---

# 110. Source Traceability

A reviewer should be able to determine where a material factual assertion originated.

---

# 111. Claim Traceability

Material conclusions should be traceable to the evidence supporting them.

---

# 112. Evidence-to-Claim Mapping

Where practical, APIG should connect evidence to the claims it supports or contradicts.

---

# 113. Claim-to-Record Mapping

Material claims should be connected to relevant records.

---

# 114. Record-to-Entity Mapping

Records should be connected to relevant people, organizations, positions, events, and jurisdictions.

---

# 115. Evidence Graph

APIG may represent:

SOURCE
→ EVIDENCE
→ CLAIM
→ FINDING
→ DECISION.

---

# 116. Evidence Path

Each material step in the evidence path should remain distinguishable.

---

# 117. No Evidence Leap

APIG must not move from a weak or indirect source to a strong conclusion without appropriate justification.

---

# 118. Causal Claim

A causal claim requires evidence sufficient to support causation.

---

# 119. Correlation

Correlation does not automatically establish causation.

---

# 120. Association

An association between entities does not automatically establish responsibility.

---

# 121. Accountability Claim

An accountability claim must distinguish direct conduct from supervisory, oversight, appointment, or jurisdictional relationships.

---

# 122. Oversight Evidence

Evidence that an authority had oversight responsibility does not by itself establish that the authority caused the underlying event.

---

# 123. Supervisory Evidence

Evidence that a person supervised another does not by itself establish responsibility for every action of the subordinate.

---

# 124. Appointment Evidence

Evidence of appointment authority does not by itself establish responsibility for every action of an appointee.

---

# 125. Jurisdictional Evidence

Evidence that a jurisdiction applies does not by itself establish personal responsibility.

---

# 126. Misconduct Claim

A misconduct claim requires appropriate evidence and applicable standards.

---

# 127. Performance Claim

A performance concern should be distinguished from a finding of misconduct.

---

# 128. Compliance Claim

A compliance claim should identify the applicable requirement.

---

# 129. Violation Claim

A violation claim should identify the rule allegedly violated.

---

# 130. Legal Claim

Legal conclusions require applicable legal authority and should not be presented as established merely because an AI inferred them.

---

# 131. Legal Source

Legal claims should rely on authoritative legal sources where practical.

---

# 132. Administrative Source

Administrative claims should rely on applicable official administrative sources where practical.

---

# 133. Organizational Source

Organizational claims should rely on appropriate organizational records where practical.

---

# 134. Source Priority

When sources conflict, consider:

1. Authority
2. Jurisdiction
3. Temporal relevance
4. Directness
5. Reliability
6. Independence
7. Specificity.

---

# 135. No Automatic Source Supremacy

No source type should automatically override all other sources in every circumstance.

---

# 136. Source Conflict Resolution

When sources conflict:

IDENTIFY CONFLICT
→ IDENTIFY SOURCES
→ IDENTIFY AUTHORITY
→ CHECK DATE
→ CHECK JURISDICTION
→ CHECK SCOPE
→ CHECK RELIABILITY
→ DETERMINE WHETHER RESOLVABLE
→ RESOLVE OR ESCALATE
→ DOCUMENT RESULT.

---

# 137. Evidence Evaluation

Evidence evaluation should ask:

- What exactly does this evidence establish?
- What does it not establish?
- Who produced it?
- When?
- Under what authority?
- Is it authentic?
- Is it complete?
- Is it independent?
- Does contradictory evidence exist?

---

# 138. What Evidence Establishes

The AI should identify the precise proposition supported by evidence.

---

# 139. What Evidence Does Not Establish

The AI should identify material conclusions that cannot reasonably be drawn from the evidence.

---

# 140. Evidence Scope

Evidence should not be stretched beyond what it reasonably supports.

---

# 141. Contextual Qualification

Where evidence is incomplete, the AI should qualify conclusions appropriately.

---

# 142. Uncertainty Statement

Material uncertainty should be communicated clearly.

---

# 143. Unknown Should Remain Unknown

When available evidence cannot establish an answer, APIG should preserve the uncertainty rather than inventing a conclusion.

---

# 144. Request for More Evidence

When additional evidence could materially improve confidence, the AI may identify what evidence would be useful.

---

# 145. Evidence Collection

Evidence collection should follow applicable authority and legal requirements.

---

# 146. Unauthorized Evidence Collection

The AI must not obtain information through unauthorized access merely to improve verification.

---

# 147. Privacy

Evidence handling must follow applicable privacy and access requirements.

---

# 148. Sensitive Evidence

Sensitive evidence requires appropriate access controls.

---

# 149. Public Evidence

Public availability does not eliminate the need for accurate interpretation.

---

# 150. Evidence Redaction

Sensitive information may be redacted when appropriate.

---

# 151. Redaction Record

Material redactions should be documented where appropriate.

---

# 152. Redaction Does Not Change Evidence

A redacted representation should not be mistaken for the complete original.

---

# 153. Source Authentication

When practical, verify that the source is what it claims to be.

---

# 154. Identity Verification

When the identity of a source materially affects reliability, verify the source identity where practical.

---

# 155. Organizational Verification

Verify that a purported organization or official source actually represents the claimed organization or authority.

---

# 156. Document Verification

Verify that a purported official document originates from the claimed authority when material.

---

# 157. Website Verification

Verify official websites and domains when source authenticity matters.

---

# 158. Social Account Verification

A social-media account should not automatically be treated as official solely because its name or appearance suggests official status.

---

# 159. Account Compromise

Potentially compromised accounts should be treated as a source-authentication concern.

---

# 160. Message Verification

A message claiming to originate from an authorized person should be verified when the requested action is material.

---

# 161. Screenshot Limitation

A screenshot may demonstrate what was displayed but may not establish the complete underlying context.

---

# 162. Video Evidence

Video should be evaluated for source, completeness, timing, authenticity, and context.

---

# 163. Audio Evidence

Audio should be evaluated for source, completeness, authenticity, and context.

---

# 164. Generated Media

AI-generated or manipulated media must be treated as such when identified.

---

# 165. Synthetic Evidence

Synthetic evidence must not be represented as naturally occurring evidence.

---

# 166. Deepfake Risk

Potentially manipulated media may require additional authentication.

---

# 167. OCR

Text extracted from images should be treated as a transcription that may contain errors.

---

# 168. OCR Verification

Material OCR-derived text should be checked against the original image where practical.

---

# 169. Translation

Translated evidence should preserve the original where possible.

---

# 170. Translation Verification

Material translated evidence should be checked for meaning and context.

---

# 171. Machine Translation

Machine translation should not automatically be treated as authoritative.

---

# 172. Calculation

Calculated information should preserve the inputs and methodology when material.

---

# 173. Derived Data

Derived data should remain distinguishable from source data.

---

# 174. Data Transformation

Material transformations should be documented.

---

# 175. Statistical Evidence

Statistical conclusions should identify relevant assumptions and limitations.

---

# 176. Model Output

Predictive or analytical model output is not automatically factual evidence.

---

# 177. Algorithmic Evidence

Algorithmic results should be evaluated according to the reliability and limitations of the underlying method.

---

# 178. AI Tool Result

Information returned by an AI tool should remain attributable to that tool and distinguishable from independently verified evidence.

---

# 179. Search Result

A search result is not necessarily the authoritative source itself.

---

# 180. Search Snippet

A search snippet should not automatically be treated as equivalent to the underlying source.

---

# 181. External Research

External research should preserve the sources consulted where practical.

---

# 182. Research Date

Material research should record when it was performed.

---

# 183. Research Scope

Research should define the question or scope being investigated.

---

# 184. Research Completeness

The AI should not imply exhaustive research unless the research was actually exhaustive.

---

# 185. Search Limitations

Search systems may omit relevant sources.

---

# 186. Retrieval Limitations

A failure to retrieve information does not prove that the information does not exist.

---

# 187. Source Availability

Unavailable sources should be identified as unavailable.

---

# 188. Broken Source

A broken external source should not be replaced with an invented version.

---

# 189. Archived Source

Archived copies may be useful when the original is unavailable.

---

# 190. Archive Verification

Archived material should be evaluated for authenticity and completeness.

---

# 191. Evidence Retention

Material evidence should be retained according to applicable requirements.

---

# 192. Evidence Destruction

Evidence should not be destroyed when subject to applicable preservation requirements.

---

# 193. Evidence Access

Evidence access should follow authorization requirements.

---

# 194. Evidence Transfer

Material evidence transfers should be documented where practical.

---

# 195. Evidence Review

Material evidence may be independently reviewed when stakes justify additional verification.

---

# 196. Peer Review

High-impact conclusions may benefit from independent review.

---

# 197. Second Review

A second reviewer may be used when a conclusion is particularly consequential or uncertain.

---

# 198. Escalation

Material unresolved evidence conflicts should be escalated to the appropriate authority.

---

# 199. Final Determination

A final determination should identify the authority or process responsible for making it where applicable.

---

# 200. Core Principles

1. APIG must distinguish facts, claims, allegations, findings, inferences, estimates, and AI analysis.
2. Evidence must be evaluated according to the specific question.
3. Sources must be evaluated for authority and reliability.
4. Authority and reliability are not the same thing.
5. Historical sources may remain authoritative for historical questions.
6. Current sources must not automatically replace historical sources.
7. Source independence matters.
8. Repetition does not automatically constitute corroboration.
9. Conflicting evidence must not be ignored.
10. Missing evidence does not automatically prove that an event did not occur.
11. Absence of a record does not automatically establish absence of an event.
12. Material evidence should be preserved.
13. Material evidence should be protected against unauthorized alteration.
14. Material evidence may require chain-of-custody documentation.
15. Original sources should be preferred when practical.
16. Copies should be verified when exactness matters.
17. Screenshots may omit relevant context.
18. Social-media content requires source and context evaluation.
19. Account identity does not automatically prove message authorship.
20. AI-generated information is not automatically evidence.
21. AI inference must remain distinguishable from source information.
22. AI conclusions must not be represented as verified facts without verification.
23. Search results are not necessarily authoritative sources.
24. Search snippets are not equivalent to underlying sources.
25. External research should preserve source information.
26. Research limitations should be acknowledged.
27. Unknown information should remain unknown rather than being fabricated.
28. Material uncertainty should be recorded.
29. Confidence is not the same as truth.
30. Confidence should change when material evidence changes.
31. Evidence should be mapped to the claims it supports or contradicts.
32. Claims should be mapped to relevant records.
33. Records should be mapped to relevant entities.
34. Causation requires evidence sufficient to establish causation.
35. Association does not automatically establish responsibility.
36. Oversight does not automatically establish causation.
37. Supervision does not automatically establish responsibility for every subordinate action.
38. Appointment authority does not automatically establish responsibility for every appointee action.
39. Jurisdiction does not automatically establish personal responsibility.
40. Legal conclusions require applicable legal authority.
41. Publicly available information still requires verification and context.
42. Unauthorized access must not be used merely to obtain evidence.
43. Sensitive evidence requires appropriate access control.
44. Material redactions should preserve awareness that the original is incomplete.
45. AI should identify what evidence establishes and what it does not establish.
46. Evidence must not be stretched beyond its reasonable scope.
47. Material source conflicts should be resolved or escalated.
48. Material findings should identify the responsible authority or process.
49. Historical evidence and authority relationships should be preserved.
50. APIG's evidence architecture must allow another authorized human or AI to reconstruct how a conclusion was reached.

---

# 201. Evidence Evaluation Sequence

CLAIM
→ IDENTIFY PRECISE PROPOSITION
→ IDENTIFY SOURCES
→ VERIFY SOURCE IDENTITY
→ EVALUATE AUTHORITY
→ EVALUATE RELIABILITY
→ CHECK DATE
→ CHECK JURISDICTION
→ CHECK SCOPE
→ CHECK INDEPENDENCE
→ CHECK CONTRADICTIONS
→ ASSESS EVIDENCE
→ ASSIGN VERIFICATION STATUS
→ ASSIGN CONFIDENCE
→ CONCLUDE OR REMAIN UNCERTAIN
→ RECORD BASIS.

---

# 202. Source Conflict Sequence

CONFLICT
→ IDENTIFY SOURCES
→ IDENTIFY SOURCE AUTHORITY
→ CHECK TEMPORAL RELEVANCE
→ CHECK JURISDICTION
→ CHECK SCOPE
→ CHECK SOURCE RELIABILITY
→ CHECK SOURCE INDEPENDENCE
→ IDENTIFY SUPPORTING EVIDENCE
→ RESOLVE OR ESCALATE
→ DOCUMENT RESULT.

---

# 203. Accountability Evidence Sequence

ACCOUNTABILITY CLAIM
→ IDENTIFY PERSON
→ IDENTIFY POSITION
→ IDENTIFY ORGANIZATION
→ IDENTIFY RELATIONSHIP TYPE
→ IDENTIFY AUTHORITY
→ IDENTIFY JURISDICTION
→ IDENTIFY EVENT
→ IDENTIFY EVIDENCE
→ DETERMINE WHAT EVIDENCE ESTABLISHES
→ DETERMINE WHAT IT DOES NOT ESTABLISH
→ AVOID AUTOMATIC ATTRIBUTION
→ RECORD CONCLUSION.

---

# 204. AI Research Sequence

QUESTION
→ DEFINE SCOPE
→ SEARCH RELEVANT SOURCES
→ IDENTIFY PRIMARY SOURCES
→ PRESERVE MATERIAL SOURCES
→ COMPARE SOURCES
→ IDENTIFY CONFLICTS
→ EVALUATE EVIDENCE
→ DISTINGUISH FACT FROM INFERENCE
→ FORM CONCLUSION
→ IDENTIFY UNCERTAINTY
→ RECORD SOURCES
→ RECORD RESEARCH DATE.

---

# 205. Evidence Update Sequence

NEW EVIDENCE
→ IDENTIFY AFFECTED CLAIM
→ CHECK AUTHENTICITY
→ EVALUATE RELEVANCE
→ COMPARE EXISTING EVIDENCE
→ CHECK WHETHER CONCLUSION CHANGES
→ UPDATE CONFIDENCE
→ REVISE FINDING WHEN REQUIRED
→ PRESERVE PRIOR RECORD
→ DOCUMENT CHANGE.

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

# END OF APIG-30