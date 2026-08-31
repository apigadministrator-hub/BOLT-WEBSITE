# APIG-01 — Mission and Core Purpose

## Status

Active

## Purpose

This document establishes the fundamental mission and purpose of APIG (AP Investigative Group).

It is a foundational specification. Other APIG specifications should be consistent with the principles established here unless an administrator explicitly changes or supersedes them.

---

# 1. APIG Mission

APIG exists to investigate, organize, preserve, analyze, and present publicly relevant information in a manner that makes complex governmental, organizational, civic, financial, documentary, and interpersonal relationships easier to understand.

APIG is intended to help people understand:

- Who holds public positions.
- What organizations and agencies exist.
- How those organizations are structured.
- Who works for or serves those organizations.
- Who is elected, appointed, hired, contracted, or otherwise associated with an organization.
- How people and organizations are connected.
- What actions government and organizations have taken.
- What documents establish those actions.
- What meetings, votes, resolutions, ordinances, decisions, and other records establish.
- What public information is available.
- Where that information came from.
- What has been verified.
- What remains unverified or unknown.
- How historical relationships and events developed over time.

---

# 2. Public Information First

APIG should prioritize information that can be supported by publicly available sources and records.

Potential sources include:

- Government websites
- Official agency websites
- Public meeting minutes
- Meeting agendas
- Resolutions
- Ordinances
- Court and public-record documents
- Election records
- Public financial records
- Official reports
- Public databases
- Public filings
- News reports
- Archived material
- Other documentary evidence

The existence of a claim does not make the claim a fact.

APIG should preserve the distinction between what a source says and what APIG concludes from that source.

---

# 3. Evidence and Provenance

Important factual information should be traceable to its source whenever practical.

A record should be capable of answering:

- What is being claimed?
- Where did the information come from?
- When was the source published or created?
- When was the information obtained?
- Is the source official?
- Has the information been independently verified?
- What is the current verification status?
- Is the information historical?
- Is there conflicting information?

APIG should favor documented evidence over unsupported assumptions.

---

# 4. Unknown Is Acceptable

APIG must never require the system to invent an answer merely because a field exists.

If a person's name cannot be established, the value may be:

`Unknown`

If a source indicates a person may hold a position but the information has not been independently verified, the record should clearly indicate that status.

Examples include:

- Unknown
- Unverified
- Source indicates
- Pending verification
- Historical
- Disputed

An incomplete but honest record is preferable to a complete record containing fabricated or unsupported information.

---

# 5. Historical Preservation

APIG should preserve historical information.

When a person leaves an office, the historical relationship should not simply disappear.

When an agency changes leadership, previous leadership should remain part of the historical record.

When an organization changes structure, APIG should preserve the previous structure when documentation permits.

APIG is intended to represent both current conditions and institutional history.

---

# 6. People and Organizations

APIG should treat people, positions, agencies, governments, organizations, and jurisdictions as distinct entities.

For example:

A person is not the same entity as the position they hold.

A position is not the same entity as the organization that controls the position.

An organization is not the same entity as the jurisdiction in which it operates.

The system should represent the relationships between these entities.

This allows APIG to represent relationships such as:

Person → holds → Position

Position → belongs to → Organization

Organization → operates within → Jurisdiction

Person → served on → Board

Person → appeared in → Document

Document → concerns → Organization

Organization → operates within → County

County → belongs to → State

---

# 7. Governmental Hierarchy

APIG should be capable of representing governmental information through a hierarchical structure.

A general structure may include:

State

→ County

→ City / Town / Village

→ Agency / Department / Office

→ Position

→ Person

The actual hierarchy may vary by jurisdiction.

APIG must not force every governmental structure into an inaccurate hierarchy merely because a standard structure would be convenient.

The documented structure of the relevant jurisdiction should control.

---

# 8. Organizations Beyond Government

APIG is not limited to government agencies.

The system may represent:

- Nonprofit organizations
- Civic organizations
- Social organizations
- Community organizations
- Religious organizations
- Clubs
- Boards
- Commissions
- Housing authorities
- Political organizations
- Businesses
- Associations
- Advocacy organizations
- Other relevant entities

The organizational hierarchy should adapt to the organization being documented.

For example:

Organization

→ Board

→ Officers

→ Staff

may be appropriate for one organization.

Another may require:

Organization

→ Executive

→ Department

→ Division

→ Staff

The system should represent the actual documented structure.

---

# 9. Elected and Appointed Positions

APIG should distinguish among different methods by which a person obtains a position.

Where documentation establishes the distinction, a position should identify whether it is:

- Elected
- Appointed
- Hired
- Contracted
- Volunteer
- Ex officio
- Other documented relationship

If an organization contains an elected position, APIG should identify that position as elected.

For example, if a housing authority has an elected resident commissioner, that position should be represented as an elected position rather than being treated simply as an ordinary staff position.

---

# 10. Profiles

APIG should provide structured profiles for relevant people and organizations.

A person profile may contain:

- Name
- Position
- Organization
- Jurisdiction
- Position type
- Current status
- Historical positions
- Contact information where appropriate and publicly available
- Sources
- Documents
- Meetings
- Votes or actions where documented
- Organizational relationships
- Verification status
- Notes
- Historical information

An organization profile may contain:

- Official name
- Organization type
- Jurisdiction
- Address
- Contact information
- Website
- Leadership
- Departments
- Positions
- Meetings
- Documents
- Sources
- Historical information
- Related organizations

The detailed structure of these profiles is defined by later specifications.

---

# 11. Search From Multiple Directions

APIG should allow users to begin their search from different starting points.

A user may begin with:

- A state
- A county
- A city
- An agency
- An organization
- A person
- A document
- A news article
- A source
- A topic

The system should allow users to move through relationships rather than forcing them to know the exact name or location of the record they seek.

For example:

Person → Organization → County

or:

State → County → Agency → Position → Person

or:

Document → Organization → Position → Person

---

# 12. Progressive Navigation

APIG should provide navigation that allows users to understand where they are within the information hierarchy.

Users should be able to move backward through the hierarchy.

The system may use breadcrumb navigation or another equivalent mechanism.

Example:

State

→ County

→ City

→ Agency

→ Position

→ Person

A user viewing the person should be able to return to the position, agency, city, county, or state without starting the search over.

---

# 13. Verification and Administrator Review

APIG may use AI to discover, collect, organize, classify, and analyze information.

AI-generated information should not automatically become verified APIG information merely because an AI produced it.

Where the system requires administrator approval, newly discovered or generated information should remain appropriately marked until approved.

The exact approval workflow is defined in later specifications.

---

# 14. AI-Assisted Operations

AI is a tool used to help APIG perform its mission.

AI may assist with:

- Research
- Document extraction
- Classification
- Entity identification
- Relationship discovery
- Source comparison
- Data entry
- Data normalization
- Website development
- News processing
- Search
- Analysis
- Administrative workflows

AI output must remain distinguishable from documented source evidence.

The AI should follow the applicable APIG specifications rather than inventing its own operating rules.

---

# 15. Multiple AI Models

APIG should not depend on any particular AI provider or model.

Different AI systems may participate in APIG operations over time.

The persistent APIG resource library should therefore contain the specifications, procedures, data structures, deployment records, and other information necessary for a new AI to understand the system.

A new AI should be able to begin by reading:

`APIG-AI-START-HERE.md`

and then follow the resource structure to the specifications relevant to its task.

---

# 16. Transparency

APIG should favor transparency about the difference between:

- Fact
- Source statement
- AI interpretation
- Analysis
- Allegation
- Unverified information
- Verified information
- Historical information
- Unknown information

The system should not intentionally present speculation as established fact.

---

# 17. Public Usability

APIG is intended to be usable by ordinary members of the public.

Users should not be required to understand APIG's internal database structure.

The public-facing system should provide intuitive ways to:

- Search
- Browse
- Discover organizations
- Discover people
- Navigate jurisdictions
- Read news
- Review documents
- Follow relationships
- Understand sources

Technical complexity should remain behind the interface whenever practical.

---

# 18. Mobile Accessibility

The APIG public interface must be designed for both desktop and mobile use.

Important functions should remain usable on a cell phone.

Navigation should not depend on large desktop-only menus.

Detailed responsive design requirements will be established in later specifications.

---

# 19. Separation of Functions

APIG may contain multiple public-facing sections with different purposes.

Examples may include:

- APIG investigative information
- Government and agency directory
- People and organization profiles
- Documents
- Search
- News
- Pig Monster News / Pig Monster Media
- FOIA/public-records functions
- Future forums or community functions

Different sections may use different visual treatments while remaining part of the same overall APIG system.

The underlying APIG information architecture and core color identity should remain coherent.

---

# 20. Institutional Memory

Important APIG decisions should eventually be preserved in persistent project resources.

This includes:

- Specifications
- Architecture decisions
- Workflows
- Data structures
- Deployment records
- Code records
- Source procedures
- Verification procedures
- AI operating rules
- Major administrative decisions
- Historical changes

The objective is to prevent critical project knowledge from existing only inside an AI conversation.

---

# 21. Administrator Authority

The APIG administrator may modify the APIG system, specifications, workflows, priorities, and organizational structure.

When a permanent rule changes, the corresponding persistent APIG resource should be updated.

The root AI resource document should also be updated when the resource structure changes.

---

# 22. Development Principle

APIG should be built incrementally.

Initial development may focus on a limited number of jurisdictions or counties.

The system should be capable of expanding without requiring the underlying architecture to be redesigned for every new county, city, agency, organization, or person.

The objective is to establish a repeatable system that can eventually support large-scale data propagation and AI-assisted maintenance.

---

# 23. Core Mission Statement

APIG exists to make publicly relevant information easier to discover, understand, verify, connect, and preserve.

The system should connect people, organizations, positions, jurisdictions, documents, events, and sources while preserving the distinction between evidence and inference.

APIG should become a persistent, searchable, transparent, and expandable information system that remains useful regardless of which AI models, developers, servers, repositories, or external services are used to operate it.

---

# 24. Relationship to Other Specifications

This document establishes the foundational mission and principles of APIG.

Detailed rules should be maintained in separate specifications.

Examples include:

- Person Profile & Identity Model
- Source & Document Provenance
- Government Hierarchy
- Agency Directory
- Database Architecture
- Website Architecture
- Newsroom Architecture
- FOIA System
- AI Operations
- Security and Permissions
- Deployment Architecture

When a later specification provides more detailed rules for a specific subject, that specification should be consulted for implementation details.

---

# 25. Change Control

This document may be modified by the APIG administrator.

When substantive changes are made:

- Update the version number.
- Record the change.
- Preserve the previous version when practical.
- Ensure the APIG AI resource index points to the current version.

The current version of this document represents the current foundational mission unless explicitly superseded.

---

# END OF APIG-01