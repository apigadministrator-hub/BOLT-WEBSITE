# APIG-04 — Person Identity and Profile Specification

## Status

Active

## Purpose

This specification defines how APIG represents individual people.

The purpose is to ensure that APIG can accurately identify a person, distinguish that person from the positions they hold, connect the person to organizations and jurisdictions, preserve historical roles, document supporting evidence, and prevent unsupported assumptions.

A person is a distinct entity.

A position is a distinct entity.

An organization is a distinct entity.

These entities must be connected through documented relationships rather than being treated as interchangeable.

---

# 1. Core Person Model

APIG should represent a person independently from:

- Position
- Organization
- Agency
- Government
- Jurisdiction
- Document
- News article
- Meeting
- Source

The basic relationship is:

PERSON
→ holds
→ POSITION

POSITION
→ belongs to
→ ORGANIZATION

ORGANIZATION
→ operates within / serves
→ JURISDICTION

This allows a person's organizational and governmental relationships to change without creating a new person record.

---

# 2. Person Record

A person record may include:

- Person ID
- Full legal or publicly documented name
- Preferred public name
- First name
- Middle name
- Last name
- Suffix
- Prefix or title where appropriate
- Known aliases
- Previous names where publicly documented
- Professional names
- Organization relationships
- Position relationships
- Jurisdiction relationships
- Contact information where appropriate and legally/publicly available
- Source records
- Verification status
- Historical information
- Date information
- Notes
- Record creation date
- Record modification date

Only fields supported by appropriate evidence should be populated as verified information.

---

# 3. Person ID

Every person should have a unique internal APIG identifier.

The Person ID should remain stable even if:

- The person changes jobs.
- The person changes offices.
- The person leaves government.
- The person is elected to another position.
- The person becomes associated with another organization.
- A name changes.
- An organization changes its name.

The identifier should not depend solely on a person's name.

---

# 4. Name

APIG should preserve the person's documented name accurately.

Where available, the system may distinguish:

- Legal name
- Publicly used name
- Professional name
- Preferred name
- Historical name

The system should not alter a person's name merely to conform to an assumed naming convention.

---

# 5. Name Components

Where appropriate, the system may store:

- First name
- Middle name
- Last name
- Suffix
- Prefix

Examples of suffixes may include:

- Jr.
- Sr.
- II
- III
- IV

Titles such as:

- Sheriff
- Mayor
- Judge
- Dr.
- Rev.

should generally be represented as titles or relationships rather than permanently incorporated into the person's core identity unless the source treats them as part of the name.

---

# 6. Preferred Display Name

The public-facing display name should be determined from reliable information.

Example:

Robert J. Smith

may be displayed as:

Robert Smith

if that is the person's established public presentation.

However, the underlying record should preserve available identifying information rather than discarding it.

---

# 7. Aliases

APIG may record documented aliases and alternate names.

Examples include:

- Nicknames
- Professional names
- Maiden names
- Former surnames
- Alternate spellings
- Initial-based names

Aliases should be identified as aliases rather than automatically treated as separate people.

---

# 8. Name Changes

A person's name may change over time.

Where a name change is relevant and publicly documented, APIG may preserve:

- Previous name
- New name
- Effective date
- Reason where appropriately documented
- Source

The system should preserve historical searchability.

---

# 9. Identity Resolution

APIG must distinguish between:

Same name

and:

Same person.

Two people may have identical names.

The system must not merge them merely because:

- Their names match.
- They work in the same county.
- They have similar titles.
- A search engine returns the same name.

Identity should be established through corroborating information.

---

# 10. Identity Evidence

Potential identity evidence may include:

- Official government biographies
- Government directories
- Election records
- Meeting minutes
- Appointment records
- Official agency pages
- Public records
- Professional biographies
- Reliable news reporting
- Other authoritative documentation

The stronger the evidence, the greater the confidence in the identity relationship.

---

# 11. Person Matching

When determining whether two records represent the same person, APIG may compare:

- Name
- Middle name or initial
- Suffix
- Organization
- Position
- Jurisdiction
- Career history
- Public biography
- Election history
- Appointment history
- Other reliable identifying information

No single matching field should automatically determine identity in ambiguous cases.

---

# 12. Duplicate Prevention

The system should attempt to prevent duplicate person records.

If two records appear to represent the same individual, the system should evaluate them before creating a second person entity.

Potential duplicate matches should be flagged for review when confidence is insufficient.

---

# 13. False Merge Prevention

APIG must also prevent incorrectly merging two different people.

Example:

Two individuals named John Smith may both work in government.

If one is a city council member and the other is a county employee, the system must not assume they are the same person.

When identity cannot be established confidently, the records should remain separate.

---

# 14. Unknown Identity

If a source identifies a person but APIG cannot establish sufficient identity information, the system may create a provisional record.

The record should be marked:

Identity Unverified

or another appropriate verification state.

The system must not fill missing identity information through guesswork.

---

# 15. Person and Position

A person and a position are separate entities.

Example:

PERSON
John Smith

POSITION
Wayne County Coroner

RELATIONSHIP
John Smith → holds → Wayne County Coroner

If John Smith leaves the position, the position continues to exist.

Another person may subsequently hold it.

---

# 16. Multiple Positions

A person may hold multiple positions.

Example:

John Smith
→ County Commissioner
→ Board Member
→ Regional Authority Member

Each position should be represented separately.

The system should not collapse multiple positions into one generic job record.

---

# 17. Simultaneous Positions

A person may hold multiple positions at the same time.

APIG should support overlapping position relationships.

Each relationship should include its own:

- Position
- Organization
- Start date
- End date where known
- Status
- Source
- Verification status

---

# 18. Historical Positions

APIG should preserve a person's historical positions.

Example:

John Smith

2018–2022
→ City Council Member

2022–2026
→ Mayor

Historical positions should not be overwritten when a person changes roles.

---

# 19. Current Position

The system may identify one or more current positions.

A current position should be supported by current or sufficiently recent evidence.

The system should not continue displaying an old position as current merely because it was once verified.

---

# 20. Former Position

A former position should be clearly identified as historical.

The record may include:

- Start date
- End date
- Source
- Reason for departure where documented

Possible departure events include:

- Term expiration
- Election loss
- Resignation
- Retirement
- Appointment elsewhere
- Removal
- Death
- Office abolition
- Unknown

The system should not infer the reason when it is not documented.

---

# 21. Vacancy

If a person leaves a position and no successor has been verified, the position should remain active while its occupant is marked appropriately.

Example:

POSITION:
County Coroner

CURRENT HOLDER:
Unknown

This is preferable to inventing a successor.

---

# 22. Elected Officials

When a person holds an elected office, APIG should record the relationship between:

- Person
- Position
- Election
- Jurisdiction
- Term
- Source

Where available, the system may record:

- Election date
- Election result
- Term beginning
- Term ending
- Reelection
- Primary election
- General election
- Vacancy
- Special election

Election information should be sourced.

---

# 23. Appointed Officials

When a person is appointed to a position, APIG should distinguish the appointment relationship.

Where available, record:

- Appointing authority
- Appointment date
- Position
- Organization
- Term
- Source

An appointment should not be represented as an election.

---

# 24. Employees

Government employees may be connected to organizations and positions without being elected or appointed officials.

Examples include:

- Administrative staff
- Clerks
- Deputies
- Analysts
- Directors
- Assistants
- Department employees

Employment relationships should be represented according to available evidence.

---

# 25. Volunteers and Civic Participants

APIG may eventually represent people participating in:

- Civic organizations
- Nonprofits
- Boards
- Commissions
- Churches
- Rotary clubs
- Community organizations
- Other social or civic groups

Participation should be distinguished from employment or government office.

---

# 26. Organization Membership

A person may be a member of an organization without holding an organizational position.

Example:

John Smith
→ member of
→ Rotary Club

This is different from:

John Smith
→ President of
→ Rotary Club

The organization membership relationship and leadership position should be separately represented.

---

# 27. Board Membership

A person may serve on one or more boards.

APIG should represent:

Person
→ member of
→ Board

and, when applicable:

Person
→ Chair of
→ Board

Board membership may also have:

- Appointment source
- Term
- Start date
- End date
- Organization
- Jurisdiction
- Verification status

---

# 28. Civic and Social Organizations

APIG should eventually support people associated with organizations outside government.

Examples include:

- Rotary clubs
- Churches
- Neighborhood organizations
- Civic associations
- Nonprofits
- Charitable organizations
- Community groups
- Professional organizations
- Social organizations

These organizations should be represented according to the broader organization specification.

---

# 29. Person-to-Person Relationships

APIG may eventually support relationships between people.

Examples may include:

- Colleague
- Supervisor
- Subordinate
- Board colleague
- Appointing authority
- Candidate
- Opponent
- Spokesperson
- Representative

Such relationships must be evidence-based.

APIG must not infer personal relationships without evidence.

---

# 30. Sensitive Personal Information

APIG should minimize collection of unnecessary personal information.

The system should not collect or publish sensitive personal information merely because it can be found.

Examples of information requiring special handling may include:

- Social Security numbers
- Financial account information
- Passwords
- Private contact information
- Medical information
- Private family information
- Personal security information
- Other protected or highly sensitive data

The existence of publicly available information does not automatically mean APIG should reproduce it.

---

# 31. Public Contact Information

Publicly documented professional contact information may be associated with a person where appropriate.

Examples include:

- Government office phone
- Government email
- Official office address
- Official contact form
- Public professional website

Personal contact information should not be substituted for official contact information unless there is a legitimate reason and the information is appropriate for publication.

---

# 32. Person Photos

APIG may eventually support profile photographs.

A photograph should preferably originate from:

- Official government source
- Official organization source
- Licensed source
- Other legally usable source

The system should preserve the source and usage information where required.

---

# 33. Source Attribution

Every significant person fact should be traceable to one or more sources.

Examples:

Person holds office
→ official government page

Person appointed
→ official meeting minutes

Person elected
→ election record

Person resigned
→ official announcement or meeting minutes

Person quoted
→ news article

The source should be attached to the relevant fact whenever practical.

---

# 34. Verification Status

Person information should support verification states.

Possible states include:

- Verified
- Partially Verified
- Unverified
- Conflicting
- Historical
- Proposed
- Rejected
- Unknown

The exact implementation will be defined in the source and verification specifications.

---

# 35. Current Verification

A person record may be verified while a particular relationship involving that person is not.

Example:

Person:
John Smith
Status: Verified

Position:
County Coroner
Status: Unverified

The system must allow verification at the appropriate level rather than treating the entire person record as automatically verified.

---

# 36. Conflicting Sources

If credible sources disagree about a person's current position, APIG should preserve the conflict.

Example:

Source A:
John Smith is County Coroner.

Source B:
Jane Doe is County Coroner.

The system should not silently choose one without evaluating the evidence.

The conflict should be available for administrative review.

---

# 37. Source Dates

Sources relating to people should retain relevant dates.

Important dates may include:

- Publication date
- Meeting date
- Appointment date
- Election date
- Term date
- Last verified date
- Document date

A person record should not be considered current merely because an old source once verified it.

---

# 38. Last Verified

APIG should support a Last Verified date for important person relationships.

Example:

Position:
County Coroner

Current holder:
John Smith

Last verified:
2026-08-30

The exact date should reflect the date on which APIG or an authorized process verified the information.

---

# 39. Verification Expiration

Certain information may require periodic re-verification.

Examples:

- Current officeholders
- Current employees
- Current board members
- Current agency leadership

The system may eventually assign review intervals based on the type of information.

---

# 40. AI Discovery

AI may discover people through:

- Government websites
- Meeting minutes
- Public documents
- News articles
- Election records
- Agency directories
- Other permitted sources

AI should record how the person was discovered.

Discovery does not automatically equal verification.

---

# 41. AI Person Matching

AI may compare potential person records.

For example:

Record A:
John R. Smith — County Commissioner

Record B:
John Smith — Wayne County Commissioner

AI may identify them as a probable match.

However, if the evidence is insufficient, the system should mark the relationship as requiring review.

---

# 42. AI Must Not Invent Identity

AI must never create unsupported information merely to complete a profile.

The system must not invent:

- Middle names
- Birth dates
- Addresses
- Employment history
- Family relationships
- Positions
- Education
- Credentials
- Contact information
- Political affiliations
- Other personal facts

If information is unknown, it should remain unknown.

---

# 43. AI Confidence

Where appropriate, AI-generated identity matches may include an internal confidence assessment.

Possible classifications include:

- High confidence
- Moderate confidence
- Low confidence
- Requires review

Confidence should not replace evidence.

A high-confidence AI prediction is still not equivalent to an authoritative source.

---

# 44. Administrator Review

Administrators should be able to review:

- New person records
- Potential duplicate people
- Identity matches
- Position relationships
- Conflicting sources
- Historical relationships
- Unverified information
- AI-generated suggestions

Administrative decisions should be recorded where appropriate.

---

# 45. Person Search

Users should be able to search for people directly.

Search may include:

- Full name
- Partial name
- Former name
- Position
- Organization
- Jurisdiction
- Agency

Example:

Search:
"Wayne County Coroner"

may return:

Person
→ Position
→ Organization
→ County

---

# 46. Person Navigation

When viewing a person, the user should be able to navigate to connected entities.

Example:

Person
→ Current Position
→ Organization
→ County
→ State

The user should also be able to navigate to:

- Former positions
- Other organizations
- Documents
- Meetings
- News
- Sources

---

# 47. Breadcrumb Navigation

A person page should preserve the user's navigation path.

Example:

Home
→ Indiana
→ Wayne County
→ Coroner's Office
→ Coroner
→ John Smith

Each prior level should be selectable.

The user should not become trapped inside a person record.

---

# 48. Multiple Search Paths

The same person should be discoverable through multiple routes.

Example:

States
→ Indiana
→ Wayne County
→ Coroner
→ John Smith

or:

People
→ John Smith

or:

Search
→ John Smith

All routes should lead to the same underlying person entity where identity has been established.

---

# 49. Person Page Structure

A person page may eventually include:

- Name
- Photograph
- Current positions
- Previous positions
- Organizations
- Jurisdictions
- Biography
- Official contact information
- Documents
- Meeting appearances
- News references
- Sources
- Verification status
- Historical timeline

The exact visual design belongs to the website interface specifications.

---

# 50. Timeline

APIG may provide a chronological timeline of a person's documented public roles.

Example:

2018
→ Elected City Council Member

2020
→ Appointed to Regional Board

2022
→ Elected Mayor

2026
→ Current position

Timeline entries should be based on documented events.

---

# 51. Historical Accuracy

Historical person records should not be rewritten to reflect current circumstances.

If a person held a position in 2020, that historical relationship should remain visible even after the person leaves the position.

---

# 52. Death and Inactive Records

Where a person's death is reliably documented, the record may be marked inactive or deceased according to APIG policy.

The system should not infer death from disappearance from an organization.

Any such status should require appropriate evidence.

---

# 53. People With Similar Names

Search results should clearly distinguish people with similar names when possible.

Useful distinguishing information may include:

- Position
- Organization
- Jurisdiction
- Approximate historical period
- Professional affiliation

The system should avoid presenting two similarly named people as one individual.

---

# 54. Person Merge

If two APIG records are later proven to represent the same person, the system may merge them.

The merge process should:

- Preserve the surviving Person ID.
- Preserve source records.
- Preserve historical relationships.
- Preserve audit information.
- Preserve references to the former record.
- Prevent loss of verified information.

Merges should be reversible or auditable where practical.

---

# 55. Person Split

If one person record is discovered to contain information belonging to two different people, the system should support splitting the record.

The system should preserve:

- Original record history
- Source relationships
- Corrected person records
- Administrative action
- Audit information

---

# 56. Audit Trail

Important changes to person records should be auditable.

The system should eventually be able to identify:

- What changed
- When it changed
- Who or what changed it
- Previous value
- New value
- Supporting source
- Approval status

AI-generated changes should be distinguishable from human-approved changes.

---

# 57. Public vs Administrative Information

The public person profile may show approved information.

The administrative view may additionally show:

- Unverified information
- Candidate matches
- Source conflicts
- AI confidence
- Proposed relationships
- Internal notes
- Review status

Internal administrative information should not automatically become public.

---

# 58. Person Data and Privacy

APIG should follow a principle of:

Collect what is necessary.
Verify what is published.
Do not expose unnecessary private information.

The system's purpose is public-interest information about people and their documented relationships to governments and organizations.

It is not intended to create unrestricted personal dossiers.

---

# 59. Person Record Example

Conceptual example:

PERSON

Name:
John R. Smith

Person ID:
APIG-PERSON-000001

CURRENT POSITION

Position:
Wayne County Coroner

Organization:
Wayne County Coroner's Office

Jurisdiction:
Wayne County, Indiana

Status:
Verified

Last Verified:
2026-08-30

SOURCE

Official government directory

HISTORICAL POSITION

Position:
Deputy Coroner

Organization:
Wayne County Coroner's Office

Period:
2019–2023

Status:
Historical

SOURCE

Official meeting minutes

This example is structural only.

It does not establish that these facts are true about any real person.

---

# 60. Core Person Relationships

The APIG person model should support relationships including:

- Holds position
- Formerly held position
- Appointed to
- Elected to
- Employed by
- Member of
- Serves on
- Chairs
- Reports to
- Supervises
- Represents
- Associated with
- Mentioned in
- Appears in
- Quoted in
- Referenced by
- Verified by source

Relationship definitions should be formally specified in the data model.

---

# 61. Person-to-Organization Navigation

A user viewing an organization should be able to see associated people.

Example:

Wayne County Coroner's Office
→ Current Coroner
→ Staff
→ Former Officials

A user viewing a person should be able to navigate back to the organization.

This creates bidirectional navigation.

---

# 62. Person-to-Document Navigation

Documents may identify or reference people.

A person page may therefore provide links to relevant:

- Meeting minutes
- Agendas
- Appointment documents
- Election documents
- Government reports
- Public notices
- Other records

The document remains the authoritative source.

The person page provides the relationship.

---

# 63. Person-to-News Navigation

News articles may reference people.

A person page may provide relevant news references.

News references should identify:

- Article
- Publication
- Date
- Person relationship
- Source

News should not automatically be treated as authoritative government documentation.

---

# 64. Person-to-Meeting Navigation

Meeting records may establish a person's participation or position.

A person page may link to:

- Meeting minutes
- Meeting agendas
- Meeting recordings
- Meeting packets
- Other meeting documentation

The relevant meeting source should be preserved.

---

# 65. Person Source Evidence

For significant claims, APIG should make it possible for a user to answer:

"What proves this?"

The person record should therefore connect important facts to source evidence.

Example:

Claim:
John Smith is Wayne County Coroner.

Evidence:
Official county directory.

Claim:
John Smith was appointed on a specific date.

Evidence:
County meeting minutes dated on or near the appointment.

This evidence-first model is central to APIG.

---

# 66. Source Presentation

Public users should be able to access source information when legally and technically possible.

A source presentation may include:

- Source title
- Source type
- Organization
- Date
- Document
- Link
- Relevant section
- Verification status

The detailed source interface belongs to the source and provenance specification.

---

# 67. Currentness

Current person information should be treated as time-sensitive.

A person who held an office last year may no longer hold it.

Therefore, APIG should distinguish:

Historically verified

from:

Currently verified.

This distinction is especially important for elected and appointed positions.

---

# 68. No Assumption of Continuity

The system must not assume that a person continues holding a position merely because no replacement has been found.

If current information is unavailable:

Current holder:
Unknown / Needs Verification

rather than:

Previous holder assumed current.

---

# 69. Person Profile Expansion

The person model should be extensible.

Future versions may support:

- Education
- Professional licenses
- Publications
- Public statements
- Voting records where appropriate
- Campaign history
- Committee memberships
- Professional affiliations
- Public events
- Other documented activities

Each additional category must have its own evidence and privacy rules.

---

# 70. Person Record as a Connected Entity

A person should ultimately function as a node in the APIG information network.

Example:

PERSON
|
+-- POSITION
|     |
|     +-- ORGANIZATION
|           |
|           +-- JURISDICTION
|
+-- DOCUMENTS
|
+-- MEETINGS
|
+-- NEWS
|
+-- SOURCES
|
+-- HISTORICAL POSITIONS
|
+-- ORGANIZATIONS
|
+-- OTHER VERIFIED RELATIONSHIPS

This structure allows users and AI systems to move through the information network from any valid entry point.

---

# 71. AI Tasking

When an AI receives a task involving a person, it should first determine what type of task is being requested.

Examples:

"Who is this person?"

"Is this person currently the sheriff?"

"Find the source proving this person was appointed."

"Show me every government position this person has held."

"Find news articles mentioning this person."

Different tasks may require different source categories.

The AI should not automatically perform every possible person-related operation.

---

# 72. Task-Specific Resource Use

When an AI is assigned a person-related task, it should consult the relevant APIG resource specification.

For example:

Identity question
→ Person Identity specification

Government position question
→ Position specification

Source verification question
→ Source and Provenance specification

News question
→ News specification

The root APIG AI resource file determines where the AI should find the applicable specification.

---

# 73. Person Data Quality Rules

A person record should be considered stronger when:

- Identity is established.
- The relevant organization is established.
- The position is established.
- The jurisdiction is established.
- The relationship is documented.
- The source is identifiable.
- Dates are available where relevant.
- Currentness is established.
- Conflicts have been evaluated.
- Verification status is recorded.

---

# 74. Unknown Information

Unknown information must remain explicitly unknown.

Examples:

Middle name:
Unknown

Current position:
Unknown

Appointment date:
Unknown

Former organization:
Unknown

The system should never substitute invented information simply to make a profile appear complete.

---

# 75. Summary

APIG treats a person as a distinct, persistent entity connected to positions, organizations, jurisdictions, documents, meetings, news, and sources.

The core principle is:

PERSON ≠ POSITION ≠ ORGANIZATION ≠ JURISDICTION

These entities are connected through documented relationships.

APIG must:

- Establish identity through evidence.
- Prevent false merges.
- Prevent duplicate records where possible.
- Preserve historical positions.
- Distinguish current from former roles.
- Support multiple simultaneous positions.
- Record source evidence.
- Preserve conflicting information.
- Support administrator review.
- Allow AI-assisted discovery.
- Prevent AI from inventing personal information.
- Protect unnecessary private information.
- Maintain an audit trail.
- Support navigation between people and connected entities.

The person model should support both public transparency and administrative data management while maintaining evidence-based accuracy.

---

# 76. Relationship to Other Specifications

This specification defines the conceptual person entity.

Related specifications should define:

- Position records
- Organization records
- Source and provenance
- Verification
- Documents
- Meetings
- News
- Search
- Database schema
- Website interface
- AI operations
- Privacy and security

Those specifications should remain consistent with this person model unless this specification is formally revised.

---

# 77. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource index if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-04