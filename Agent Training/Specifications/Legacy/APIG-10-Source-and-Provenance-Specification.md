# APIG-10 — Source and Provenance Specification

## Status

Active

## Purpose

This specification defines how APIG identifies, stores, evaluates, connects, and preserves the sources and provenance of information within the system.

APIG must be able to answer:

- Where did this information come from?
- What source supports it?
- When was the source published or obtained?
- What entity or event does the source describe?
- How reliable is the source?
- Has the information been verified?
- What changed when the information was updated?
- Can an AI distinguish sourced facts from inference?

Source provenance is fundamental to APIG's credibility, accountability, historical accuracy, and AI operations.

---

# 1. Core Principle

Every significant factual claim in APIG should be traceable to a source whenever a source exists.

APIG should preserve the relationship:

CLAIM
→ SUPPORTED BY
→ SOURCE

A source may support one or many claims.

A claim may have one or many supporting sources.

---

# 2. Source as a First-Class Entity

A source should have its own persistent identity.

A source may be:

- Government website
- Government document
- Statute
- Ordinance
- Resolution
- Court record
- Meeting minutes
- Official report
- Public filing
- News article
- Press release
- Public database
- Social media post
- Interview
- User submission
- Archived webpage
- Other documented material

---

# 3. Source Identity

A source record may contain:

- Source ID
- Source type
- Title
- Publisher
- Author
- Organization
- Publication date
- Retrieval date
- URL where applicable
- Archive location where applicable
- Version
- Document identifier
- Jurisdiction
- Language
- Status
- Reliability assessment
- Verification status

---

# 4. Source Types

APIG should classify sources.

Examples:

- Primary Government Source
- Primary Legal Source
- Court Source
- Official Organizational Source
- Public Record
- Secondary News Source
- Academic Source
- Community Source
- User-Submitted Source
- Social Media Source
- Archived Source
- AI-Generated Material

The source classification must remain visible where relevant.

---

# 5. Primary Sources

Primary sources are materials directly produced by the entity or authority responsible for the underlying information.

Examples:

- Statute
- Ordinance
- Court filing
- Government resolution
- Official meeting minutes
- Official appointment record
- Government financial report
- Official agency report

Primary-source status should be preferred when establishing authoritative facts.

---

# 6. Secondary Sources

Secondary sources report, analyze, summarize, or interpret information originating elsewhere.

Examples:

- Newspaper article
- Investigative report
- Commentary
- Research article
- Blog post

Secondary sources may be valuable but should remain distinguishable from primary sources.

---

# 7. Source Reliability

Reliability should not be represented as a universal permanent score unless the methodology supports it.

APIG may instead record characteristics such as:

- Official
- Primary
- Verified
- Corroborated
- Unverified
- Conflicting
- Historical
- Archived
- User-submitted

---

# 8. Verification Status

Information derived from a source may have a verification state.

Examples:

- Verified
- Partially Verified
- Unverified
- Conflicting
- Under Review
- Disputed
- Historical
- Superseded

---

# 9. Source Date

APIG should distinguish:

- Publication date
- Effective date
- Event date
- Retrieval date
- Update date
- Archive date

These dates are not interchangeable.

---

# 10. Source Version

Sources may change.

APIG should preserve versions where practical.

Example:

Government webpage
→ Version 1
→ Version 2
→ Version 3

Historical versions should not be silently replaced.

---

# 11. Source Preservation

Where legally and technically appropriate, APIG should preserve:

- Original URL
- Retrieved copy
- Document
- Archive reference
- Metadata
- Retrieval date
- Hash or integrity identifier where appropriate

---

# 12. Source-to-Claim Relationship

APIG should support explicit relationships such as:

Source
→ supports
→ Claim

Source
→ contradicts
→ Claim

Source
→ updates
→ Claim

Source
→ supersedes
→ Source

Source
→ provides context for
→ Claim

---

# 13. Claim Identity

Significant claims may have persistent internal identifiers.

Example:

Claim ID:
CLAIM-000001

This allows multiple sources and records to reference the same factual proposition.

---

# 14. Claim vs Interpretation

APIG must distinguish:

Source statement

from:

APIG interpretation.

Example:

Source:
"The board voted 4–1 to terminate the contract."

APIG may record:

Claim:
Board voted 4–1 to terminate contract.

APIG must not automatically transform that into:

"The board acted improperly."

The latter is an interpretation requiring additional evidence.

---

# 15. Claim vs Inference

AI may generate inferences.

Inferences must be clearly distinguishable from sourced facts.

Example:

Sourced fact:
Person A was appointed Executive Director.

Inference:
Person A therefore had authority associated with the Executive Director position.

The inference should be derived from documented position authority rather than presented as an independently sourced event.

---

# 16. AI-Generated Information

AI-generated content must be distinguishable from source material.

AI must not present its own generated statement as an original source.

Where AI generates a conclusion, the underlying sources should be available.

---

# 17. Source Attribution

Where practical, users should be able to identify the source supporting a claim.

The interface may provide:

- Source title
- Publisher
- Date
- Source type
- Link
- Document
- Relevant section
- Verification status

---

# 18. Source Navigation

Users should be able to navigate:

Claim
→ Source

and:

Source
→ Claims supported

This should work throughout the website.

---

# 19. Entity Provenance

APIG entities should maintain provenance.

Examples:

Person
→ identified by
→ Government Directory

Organization
→ established by
→ Ordinance

Position
→ created by
→ Resolution

Jurisdiction
→ established by
→ Statute

---

# 20. Relationship Provenance

Relationships should also have provenance.

Example:

Person A
→ occupies
→ Executive Director Position

The occupancy relationship should have supporting evidence.

Likewise:

Executive Director
→ supervises
→ Maintenance Staff

should have a source establishing the supervisory relationship.

---

# 21. Authority Provenance

Authority relationships must be sourced where possible.

Example:

County Board Chair
→ appoints
→ Housing Authority Commissioners

The system should preserve the document, statute, ordinance, or other source establishing that authority.

---

# 22. Jurisdiction Provenance

Jurisdictional relationships should be sourced.

Example:

County
→ jurisdiction over
→ geographic area

The source establishing the jurisdiction should be preserved.

---

# 23. Event Provenance

Events should be sourced.

Examples:

- Appointment
- Resignation
- Arrest
- Charge
- Conviction
- Meeting action
- Organizational change
- Policy change

The event record should identify the source supporting the event.

---

# 24. News Provenance

News records must preserve their originating publication.

The system should distinguish:

News publication
from:

Underlying event.

A news article reporting an event does not become the event itself.

---

# 25. Multiple Sources

A claim may have multiple sources.

Example:

Source A
→ supports
→ Claim

Source B
→ corroborates
→ Claim

Source C
→ disputes
→ Claim

APIG should preserve all relevant relationships.

---

# 26. Conflicting Sources

When sources conflict, APIG should not silently erase the disagreement.

The system should preserve:

- Source A
- Source B
- Nature of conflict
- Relevant dates
- Verification status
- Resolution status where applicable

---

# 27. Source Hierarchy

Source authority may depend on the question being answered.

Example:

For statutory authority:

Statute
→ generally stronger than
News article

For public reaction:

Public comments
→ may be directly relevant

For historical reporting:

Contemporary records
→ may be more relevant than later summaries

APIG should evaluate source suitability in context.

---

# 28. Source Supersession

A source may be superseded.

Example:

Old policy
→ superseded by
New policy

The historical source remains available.

The newer source governs current interpretation where appropriate.

---

# 29. Source Expiration

Some sources have effective periods.

Examples:

- Temporary orders
- Emergency declarations
- Temporary appointments
- Interim policies

APIG should preserve their effective periods.

---

# 30. Archived Sources

Archived sources should retain:

- Original source identity
- Archive location
- Original publication information
- Retrieval date
- Archive date where known

---

# 31. Broken Sources

If a source becomes unavailable, APIG should not automatically delete the claim it previously supported.

The source should be marked unavailable and preserved where possible.

---

# 32. Source Integrity

Where practical, APIG should maintain integrity information such as:

- File hash
- Document hash
- Retrieval timestamp
- Archive identifier
- Version identifier

This can help establish that a preserved document has not been altered.

---

# 33. Source Access

A source may have different access conditions.

Examples:

- Public
- Restricted
- Archived
- Paywalled
- Login required
- Internal
- Unavailable

APIG should record access status without treating restricted access as evidence of unreliability.

---

# 34. Source Privacy

APIG must protect private source information.

A source may be retained internally while only an appropriate public reference is displayed.

---

# 35. User-Submitted Sources

Users may submit sources.

User submissions should be clearly identified as user-submitted until independently verified.

A user submission must not automatically become an authoritative source.

---

# 36. Social Media Sources

Social media posts may be sources for claims about what was publicly stated or published.

They should not automatically establish the truth of the underlying statement.

Example:

Person posted:
"Meeting was canceled."

This establishes that the person made the statement.

It does not independently establish why the meeting was canceled.

---

# 37. Anonymous Sources

Anonymous or unidentified sources should be handled separately from identified authoritative sources.

The system should preserve appropriate confidentiality where required.

---

# 38. Source Quotations

When APIG stores quoted material, it should preserve:

- Exact quotation
- Speaker/author
- Date
- Source
- Context

Quotes should not be altered in a way that changes their meaning.

---

# 39. Source Context

A source should not be interpreted without considering relevant context.

APIG should preserve enough surrounding information to understand:

- Who made the statement
- When it was made
- What was being discussed
- Whether it was allegation, finding, opinion, or fact

---

# 40. Legal Characterization

Sources involving legal or misconduct matters must preserve the source's actual characterization.

Examples:

- Alleged
- Accused
- Charged
- Arrested
- Convicted
- Acquitted
- Found liable
- Disciplined
- Exonerated

APIG must not upgrade an allegation into a proven fact.

---

# 41. Source-to-Event Separation

The source and event are separate entities.

Example:

News article
→ reports
→ DUI arrest

The news article is not itself the arrest.

The underlying event should have its own record and provenance.

---

# 42. Source-to-Person Separation

A source mentioning a person does not automatically establish every statement about that person as fact.

The specific claim and supporting evidence must be evaluated.

---

# 43. Source-to-Organization Separation

A source mentioning an organization does not automatically establish misconduct or responsibility by the organization.

The claim must identify its actual subject.

---

# 44. Source-to-Authority Separation

A source describing a person's position does not automatically establish all authority associated with that position.

Authority should be established from appropriate sources.

---

# 45. Provenance Graph

APIG should support a provenance graph.

Example:

SOURCE
↓ supports
CLAIM
↓ describes
PERSON
↓ occupies
POSITION
↓ belongs to
ORGANIZATION
↓ exists within
JURISDICTION

This allows an AI to trace information back to its origin.

---

# 46. Provenance Chain

For important information, APIG should support:

Claim
→ Source
→ Publisher
→ Original document
→ Relevant section
→ Retrieval information

---

# 47. Provenance and AI

When AI answers a question, it should be able to identify the relevant supporting resources.

AI should distinguish:

- Directly sourced facts
- Derived facts
- Inferences
- Summaries
- Interpretations
- Unknown information

---

# 48. AI Source Selection

When multiple sources exist, AI should prefer sources appropriate to the question.

For legal authority:

Primary legal sources should generally be preferred.

For current organizational structure:

Current official sources should generally be preferred.

For historical questions:

Contemporaneous or archival sources may be more appropriate.

---

# 49. AI Conflict Handling

If sources conflict, AI should identify the conflict rather than inventing certainty.

Example:

"Source A states X, while Source B states Y."

The system may identify which source appears more authoritative and explain why, but should preserve the underlying disagreement.

---

# 50. Source Freshness

Current questions should favor current sources.

Historical questions should favor sources appropriate to the historical period.

A current webpage should not automatically override a historical source when answering a historical question.

---

# 51. Source Relevance

A source should be evaluated for relevance to the specific claim.

A highly authoritative source about one subject may be irrelevant to another.

---

# 52. Source Completeness

A source may support only part of a claim.

APIG should avoid treating a partial source as support for unsupported portions.

---

# 53. Source Scope

Sources may apply to:

- Person
- Position
- Organization
- Jurisdiction
- Event
- Relationship
- Document
- Policy
- Time period

Scope should be explicit where necessary.

---

# 54. Source Relationships

APIG should support:

Source
→ supports
→ Claim

Source
→ contradicts
→ Claim

Source
→ references
→ Entity

Source
→ establishes
→ Relationship

Source
→ modifies
→ Rule

Source
→ supersedes
→ Source

---

# 55. Source Indexing

Sources should be searchable by:

- Title
- Publisher
- Author
- Date
- Type
- Jurisdiction
- Entity
- Claim
- Topic
- Source ID

---

# 56. Source Search

Users should eventually be able to ask:

"What is the source for this?"

"Show me the document establishing this authority."

"Where did this information come from?"

"What sources contradict this?"

"Show me the original government record."

---

# 57. Source Display

The interface should make source provenance accessible without overwhelming the primary page.

A claim may display:

Source
→ Publisher
→ Date
→ Verification
→ View source

---

# 58. Source Change Detection

Where technically feasible, APIG may detect changes to recurring sources.

Examples:

- Government webpages
- Agency directories
- Public reports
- Policies
- Meeting calendars

Changes should create historical versions rather than silently overwrite prior information.

---

# 59. Source Monitoring

APIG may monitor important sources for changes.

Examples:

- Government websites
- Agency pages
- Official directories
- Legal databases
- Meeting records

Monitoring should be configurable.

---

# 60. Source Alerts

A source change may trigger an internal review.

Examples:

- Official changes leadership
- New ordinance
- Position vacancy
- New meeting minutes
- Updated agency policy

AI may identify potentially affected records, but changes to authoritative records should follow verification rules.

---

# 61. Source Quality Review

Administrators should be able to review:

- Source reliability
- Verification status
- Conflicts
- Missing provenance
- Duplicate sources
- Broken links
- Outdated sources

---

# 62. Duplicate Sources

APIG should identify duplicate or substantially identical sources where practical.

Duplicates should not create artificial corroboration.

Example:

Ten websites copying the same press release are not necessarily ten independent sources.

---

# 63. Source Independence

Corroboration is stronger when sources are genuinely independent.

APIG should distinguish:

Independent reporting

from:

Repeated publication of the same underlying material.

---

# 64. Source Chains

A secondary source may cite a primary source.

APIG should attempt to preserve the chain:

Secondary Source
→ cites
→ Primary Source
→ supports
→ Claim

The primary source should be preferred when available and appropriate.

---

# 65. Source Recovery

If an important source disappears, APIG should attempt to preserve or identify:

- Archive
- Document copy
- Citation
- Alternate official source
- Historical version

---

# 66. Source Removal

Sources should not be deleted merely because they are inconvenient or contradictory.

Removal should require appropriate administrative authority and an audit trail.

---

# 67. Provenance Audit Trail

Changes to provenance should be auditable.

The system should record:

- Previous source
- New source
- Date
- User or AI
- Reason
- Verification status

---

# 68. Missing Provenance

If no source is available, APIG should identify the information as:

- Unverified
- User-provided
- AI-derived
- Unknown source
- Historical information with incomplete provenance

The system must not fabricate a source.

---

# 69. Provenance Confidence

Where APIG uses confidence indicators, they should describe the confidence in the source/claim relationship, not imply legal certainty.

---

# 70. Source and Accountability

Claims involving accountability, authority, misconduct, or organizational responsibility should receive particularly strong provenance requirements.

Examples:

- Who appointed whom?
- Who supervises whom?
- Who had authority?
- What happened?
- Who was responsible?
- What disciplinary action occurred?

These should be supported by appropriate sources.

---

# 71. Source and Authority

Authority claims should preferably be established by:

- Law
- Ordinance
- Charter
- Resolution
- Bylaws
- Official organizational rules
- Other authoritative documentation

News reports may provide context but should not automatically replace the underlying authority source.

---

# 72. Source and Personnel

Personnel claims should be sourced appropriately.

Examples:

- Appointment
- Resignation
- Termination
- Promotion
- Position
- Employment status

---

# 73. Source and Historical Records

Historical claims should preserve historical provenance.

The source should be evaluated according to the historical period being studied.

---

# 74. Source and Website Architecture

The website should allow users to move from an entity to its supporting sources.

Example:

Person
→ Position
→ Authority
→ Source establishing authority

and:

Event
→ Source reporting event

---

# 75. Source and AI Resource Library

The APIG AI resource library itself contains specifications.

These specifications are internal guidance resources.

They should be distinguished from external sources used to establish facts about real-world entities.

---

# 76. AI Operating Rule

AI must never cite an APIG specification as though it were evidence that a real-world event occurred.

Specifications explain how APIG operates.

External sources establish real-world facts.

---

# 77. Source Priority

When answering factual questions, AI should generally prioritize:

1. Primary authoritative source
2. Official organizational source
3. Official public record
4. Independent reliable reporting
5. Other relevant secondary sources
6. User-submitted or informal sources

The appropriate priority may vary by question.

---

# 78. No False Authority

A source should not be labeled authoritative merely because it appears professional.

Authority comes from the source's relationship to the underlying subject matter.

---

# 79. No False Corroboration

Multiple sources repeating the same unsupported statement should not automatically be treated as independent corroboration.

---

# 80. Core Provenance Principles

1. Significant claims should be traceable to sources.
2. Sources are first-class entities.
3. Source type must be identifiable.
4. Primary and secondary sources must remain distinct.
5. Claims must remain distinct from sources.
6. Events must remain distinct from reporting about events.
7. Authority relationships must have appropriate provenance.
8. Historical information must preserve historical sources.
9. Conflicting sources must remain visible.
10. AI inference must remain distinguishable from sourced fact.
11. Missing sources must remain unknown.
12. Sources must not be fabricated.
13. Duplicate sources must not create false corroboration.
14. Source changes should be historically preserved where practical.
15. Provenance should be navigable through the website.
16. AI should be able to trace important answers to supporting resources.
17. Legal and misconduct-related claims require careful source characterization.
18. Source provenance is part of APIG's accountability architecture.

---

# 81. Summary

APIG's provenance system creates a traceable chain:

SOURCE
→ CLAIM
→ ENTITY
→ RELATIONSHIP
→ EVENT
→ ORGANIZATION
→ JURISDICTION

The system preserves where information came from, how it was characterized, when it applied, whether it has been verified, and what other sources support or contradict it.

This allows users and AI systems to distinguish:

FACT
from
SOURCE
from
INFERENCE
from
INTERPRETATION
from
UNKNOWN.

That distinction is fundamental to trustworthy APIG operation.

---

# 82. Relationship to Other Specifications

This specification connects directly with:

- Government and jurisdiction hierarchy
- Organization and agency specification
- Person identity and relationship specification
- Authority, accountability, and chain-of-command specification
- Position and office specification
- Event specification
- News specification
- Document specification
- Meeting specification
- User account specification
- Authentication and authorization specification
- Database specification
- Website interface specification
- AI operations specification
- Privacy and security specification

The APIG root resource document should identify this specification as the primary resource for questions concerning sources, evidence, provenance, verification, attribution, conflicting information, historical source preservation, and AI source handling.

---

# 83. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-10