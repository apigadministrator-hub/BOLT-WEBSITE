# APIG-02 — Core System Architecture

## Status

Active

## Purpose

This document establishes the foundational architecture of the APIG information system.

It defines the major entities, relationships, information layers, navigation principles, and system boundaries that later APIG specifications will build upon.

This document describes the architecture at a conceptual level. Detailed implementation requirements belong in later specifications.

---

# 1. Architectural Objective

APIG shall be designed as a persistent information system capable of collecting, organizing, connecting, verifying, searching, preserving, and presenting publicly relevant information.

The architecture must support incremental development.

The system should be capable of beginning with a small number of jurisdictions and expanding to additional counties, cities, agencies, organizations, people, documents, and other entities without requiring fundamental architectural redesign.

---

# 2. Primary Information Hierarchy

APIG's geographic and governmental information may generally follow this hierarchy:

State
→ County
→ Municipality
→ Agency / Organization
→ Department / Division
→ Position
→ Person

This is a general model, not an absolute rule.

Actual governmental and organizational structures may differ.

APIG must represent the documented structure rather than forcing every organization into an artificial hierarchy.

---

# 3. Jurisdiction

A jurisdiction is a geographic or governmental area within which an entity operates or has authority.

Examples include:

- State
- County
- City
- Town
- Village
- Township
- District
- Precinct
- Other legally or administratively defined jurisdiction

Jurisdictions may contain or overlap with other jurisdictions.

A jurisdiction should be represented as its own entity rather than merely being stored as text inside another record.

---

# 4. Organization

An organization is an identifiable governmental, nonprofit, civic, social, commercial, religious, political, or other organized entity.

Examples include:

- County government
- City government
- Sheriff's department
- Police department
- Coroner's office
- County clerk's office
- Housing authority
- School corporation
- Nonprofit
- Rotary club
- Church
- Civic organization
- Board
- Commission
- Association
- Business

An organization may contain departments, divisions, positions, boards, committees, and other subordinate entities.

---

# 5. Agency

An agency is an organizational entity performing a governmental or public function.

Examples include:

- Sheriff's department
- Police department
- Health department
- Coroner's office
- County clerk
- Planning department
- Housing authority

Not every organization is an agency.

The system should preserve the distinction between organization type and agency status.

---

# 6. Position

A position represents an identifiable role within an organization.

Examples include:

- Sheriff
- County Commissioner
- County Clerk
- Coroner
- Mayor
- Police Chief
- Deputy
- Clerk
- Director
- Board Member
- Resident Commissioner

A position is an entity separate from the person occupying it.

This allows APIG to preserve the position when the person holding it changes.

---

# 7. Person

A person is an identifiable individual.

A person may have relationships with one or more:

- Positions
- Organizations
- Agencies
- Boards
- Committees
- Documents
- Meetings
- Events
- Jurisdictions

A person's profile should not be limited to their current position.

Historical relationships should be preserved when supported by evidence.

---

# 8. Person-to-Position Relationship

The relationship between a person and a position should be explicitly represented.

Examples:

Person
→ holds
→ Sheriff

Person
→ formerly held
→ County Commissioner

Person
→ appointed to
→ Board Member

Person
→ elected to
→ Mayor

The relationship should support relevant dates and status where available.

---

# 9. Position-to-Organization Relationship

A position belongs to an organization or organizational structure.

Examples:

Sheriff
→ belongs to
→ Sheriff's Department

County Clerk
→ belongs to
→ County Government

Resident Commissioner
→ belongs to
→ Housing Authority

This relationship allows users to navigate from a person to their position and from the position to the organization.

---

# 10. Organization-to-Jurisdiction Relationship

Organizations may operate within, serve, or have authority over one or more jurisdictions.

Examples:

Sheriff's Department
→ serves
→ County

Police Department
→ operates within
→ City

County Government
→ governs
→ County

A single organization may have relationships with multiple geographic areas.

---

# 11. Organization Hierarchy

Organizations may contain subordinate organizations.

Example:

County Government
→ Sheriff's Department
→ Coroner's Office
→ County Clerk's Office
→ Treasurer's Office
→ Auditor's Office

Another organization might have:

Housing Authority
→ Board of Commissioners
→ Executive Director
→ Staff

The architecture must support different organizational structures.

---

# 12. Governmental Hierarchy

Governmental entities should be capable of being connected through their documented hierarchy.

Example:

State
→ County
→ City
→ Police Department
→ Police Chief
→ Person

Another example:

State
→ County
→ County Government
→ Sheriff's Department
→ Sheriff
→ Person

The system should not assume that every county or state uses identical organizational structures.

---

# 13. Non-Governmental Organizations

The same underlying architecture should support organizations that are not governmental.

Example:

Civic Organization
→ Board
→ Officers
→ Members

Example:

Rotary Club
→ Club Leadership
→ Officers
→ Members

Example:

Church
→ Leadership
→ Staff
→ Ministries
→ Members

The hierarchy should reflect the organization's actual documented structure.

---

# 14. Position Type

Positions should be capable of identifying how the position is filled.

Possible classifications include:

- Elected
- Appointed
- Hired
- Contracted
- Volunteer
- Ex officio
- Other
- Unknown

The classification should be based on evidence whenever possible.

---

# 15. Elected Positions

An elected position should be explicitly identified as elected.

This is important because the method by which a person obtains a position is relevant information.

Examples include:

- Sheriff
- Mayor
- County Commissioner
- Clerk
- Treasurer
- Auditor
- Other elected offices

Some organizations outside traditional government may also contain elected positions.

For example, if a housing authority has an elected resident commissioner, that position should be represented as elected.

---

# 16. Documents

A document is a source or record that contains information relevant to APIG.

Examples include:

- Meeting minutes
- Meeting agendas
- Ordinances
- Resolutions
- Reports
- Court documents
- Government records
- Financial documents
- Election records
- Public filings
- Correspondence
- News articles
- Archived webpages
- Other documentary material

Documents should be represented separately from the entities they describe.

---

# 17. Document Relationships

A document may relate to multiple entities.

Example:

Document
→ mentions
→ Person

Document
→ concerns
→ Organization

Document
→ records
→ Meeting

Document
→ establishes
→ Position

Document
→ provides evidence for
→ Relationship

This permits APIG to move from a factual record back to the evidence supporting it.

---

# 18. Meetings

A meeting is an event at which an organization, board, commission, government, or other body conducts official or organizational business.

A meeting may have:

- Date
- Time
- Location
- Organization
- Participants
- Agenda
- Minutes
- Actions
- Votes
- Resolutions
- Related documents
- Sources

Meetings should be represented as separate entities when the information system requires detailed meeting tracking.

---

# 19. Events

APIG should support events beyond meetings.

Examples include:

- Elections
- Appointments
- Resignations
- Hearings
- Public announcements
- Organizational changes
- Legal events
- Other significant occurrences

Events may connect people, organizations, positions, documents, and jurisdictions.

---

# 20. Sources

A source identifies where information came from.

A source may be:

- Government website
- Agency website
- Public record
- Meeting minutes
- Meeting agenda
- Official filing
- Court record
- News organization
- Archived webpage
- Other documented source

Sources should be distinct from the factual claims extracted from them.

---

# 21. Claims

A claim is a statement that APIG is considering or recording as potentially factual.

Examples:

"Jane Doe is the County Clerk."

"John Smith was appointed to the Housing Authority."

"The commission approved the resolution."

Claims should be capable of being connected to one or more sources.

---

# 22. Verification Status

Factual records should support a verification state.

Possible states include:

- Verified
- Unverified
- Partially verified
- Source indicates
- Pending review
- Disputed
- Historical
- Unknown

The exact verification workflow will be defined by later specifications.

---

# 23. Provenance

Provenance describes the history of information.

APIG should be able to determine, where practical:

- Where information originated.
- When it was obtained.
- What source provided it.
- What processing occurred.
- Whether an AI extracted it.
- Whether a human reviewed it.
- Whether an administrator approved it.
- Whether later evidence changed the record.

Provenance is a core architectural principle.

---

# 24. Relationships Are First-Class Information

APIG should not treat relationships merely as incidental text.

Relationships between entities are themselves important information.

Examples:

Person
→ holds
→ Position

Person
→ member of
→ Organization

Organization
→ operates in
→ Jurisdiction

Person
→ served with
→ Person

Document
→ mentions
→ Person

Meeting
→ conducted by
→ Organization

Organization
→ related to
→ Organization

The detailed relationship model will be defined in later specifications.

---

# 25. Multiple Paths Through the Information

Users should be able to reach the same information through different paths.

For example:

## Geographic Path

State
→ County
→ City
→ Agency
→ Position
→ Person

## Agency Path

Agency
→ Position
→ Person

## Person Path

Person
→ Position
→ Organization
→ County

## Document Path

Document
→ Person
→ Position
→ Organization

## News Path

News Article
→ Person
→ Organization
→ Event

The architecture should support these interconnected paths.

---

# 26. Breadcrumb Navigation

The public interface should provide a clear indication of the user's location within the information hierarchy.

Example:

Home
→ Indiana
→ Wayne County
→ Richmond
→ Police Department
→ Chief
→ Person

Users should be able to navigate backward through these levels.

The detailed website implementation will be defined in the website specifications.

---

# 27. Search Is Not the Same as Navigation

APIG should support both:

## Navigation

The user browses through known organizational or geographic relationships.

## Search

The user enters a name, organization, document, topic, or other query and goes directly to relevant information.

Users should not be forced to know the exact jurisdiction or organizational hierarchy before finding information.

---

# 28. Person-First Searching

A user may begin with a person.

Example:

Search:
"John Smith"

APIG may return:

John Smith
→ Position
→ Organization
→ Jurisdiction
→ Related documents
→ Related meetings
→ Related news
→ Historical positions

The person may therefore become the starting point for discovering the larger organizational network.

---

# 29. Organization-First Searching

A user may begin with an organization.

Example:

Search:
"Wayne County Sheriff's Department"

APIG may provide:

Organization
→ Leadership
→ Positions
→ Personnel
→ Jurisdiction
→ Meetings
→ Documents
→ News
→ Related organizations

---

# 30. Geographic-First Searching

A user may begin with a state.

Example:

State
→ County
→ Municipality
→ Agency
→ Position
→ Person

The public interface may use geographic maps and other visual navigation tools where appropriate.

---

# 31. Mobile Architecture

The system must support mobile devices.

The architecture should not depend on desktop-only navigation.

Menus should remain understandable on small screens.

Long hierarchical menus should not overwhelm mobile users.

Detailed responsive design rules belong in later website specifications.

---

# 32. Public Interface Layers

The APIG interface may contain:

- Primary navigation
- Context-sensitive navigation
- Breadcrumb hierarchy
- Main content
- User/account controls
- Notifications
- Search
- Related information
- Optional advertising or promotional areas
- Administrative functions

These interface components may be implemented differently across sections of the site.

---

# 33. Primary Navigation

The primary navigation should provide access to major APIG functions.

The exact final menu may include functions such as:

- Home
- States
- Agencies
- People
- News
- Documents
- Search

The final navigation structure is subject to the website specifications.

---

# 34. Context-Sensitive Navigation

The left-side navigation or equivalent contextual navigation may change depending on the page being viewed.

For example:

On a state page:

- Counties
- State government
- Agencies
- Related information

On a county page:

- Government
- Cities
- Agencies
- Officials
- Documents
- Meetings

On an agency page:

- Overview
- Leadership
- Positions
- Personnel
- Meetings
- Documents
- News
- Sources

The interface should show information relevant to the user's current context rather than presenting every possible option at all times.

---

# 35. Right-Side Information Area

The public website may use a right-side information area on larger screens.

Potential content includes:

- User account information
- Notifications
- Messages
- Related activity
- Relevant links
- Sponsored material
- APIG promotional material
- Advertising

This area must not interfere with primary information access.

On mobile devices it may move below the main content or collapse into an appropriate mobile interface.

---

# 36. Advertising and Revenue

APIG may eventually support revenue-producing content.

Potential mechanisms may include:

- Traditional advertising
- Affiliate links
- Sponsored content
- APIG-promoted services
- Other legitimate revenue mechanisms

Revenue mechanisms must remain distinguishable from factual APIG information.

Advertising must not be allowed to alter factual records or verification decisions.

Detailed advertising rules may be established separately.

---

# 37. Separate Public Sections

APIG may contain specialized sections.

For example:

APIG Core
→ Government / Organizations / People / Documents / Research

Pig Monster News / Pig Monster Media
→ News / Editorial / Media

These sections may use different branding or visual presentation while remaining connected to the APIG information system.

The underlying information architecture should remain interoperable.

---

# 38. Data and Presentation Are Separate

The database should contain structured information.

The website should present that information to users.

The same underlying person, organization, document, or source should be capable of appearing in multiple interfaces.

A change to the visual presentation should not require duplicate factual records.

---

# 39. AI and Data Propagation

AI may assist in discovering and organizing information.

Potential AI functions include:

- Discovering agencies
- Discovering positions
- Identifying people
- Extracting information from documents
- Identifying relationships
- Comparing sources
- Detecting changes
- Suggesting new records
- Updating records
- Identifying missing information

AI-discovered information should be subject to the applicable verification and approval rules.

---

# 40. Administrator Approval

APIG may use an administrator approval process before AI-generated or AI-discovered information becomes publicly authoritative.

Potential workflow:

AI discovers information
→ creates proposed record
→ attaches source
→ assigns verification status
→ administrator reviews
→ administrator approves/rejects
→ approved information becomes public

The detailed workflow will be established by later specifications.

---

# 41. Scalability

The architecture must support expansion.

The system should eventually be capable of handling:

- Multiple states
- Multiple counties
- Multiple municipalities
- Thousands of organizations
- Large numbers of people
- Large document collections
- Large numbers of relationships
- Historical records
- News articles
- Source records

The initial system may begin with a small number of counties.

The architecture should not assume that the initial geographic scope is permanent.

---

# 42. Modularity

APIG should be modular.

Major functions should be capable of being developed, modified, replaced, or expanded independently when practical.

Examples:

- Search
- Profiles
- Documents
- News
- FOIA
- Verification
- AI ingestion
- Database
- Authentication
- Notifications

A failure or replacement of one module should not unnecessarily destroy unrelated APIG information.

---

# 43. External Services

APIG may depend on external services during development or operation.

Examples include:

- Cloud services
- Database providers
- Spreadsheet systems
- Form systems
- Hosting providers
- APIs
- AI providers
- Repository systems
- Automation services

External dependencies must be documented.

Deployment records should preserve exactly how external services were configured.

---

# 44. AI Independence

No critical APIG architecture should depend upon a single AI model.

AI agents may come and go.

The persistent architecture, specifications, data, source records, deployment records, and operational instructions must remain accessible independently of any one AI provider.

---

# 45. Security Boundary

The public information system and administrative systems should be treated as different security contexts.

Public users may browse approved information.

Authorized users may perform additional actions.

Administrators may perform privileged actions.

AI agents may have task-specific permissions.

Detailed authentication, authorization, security, and audit rules belong in later specifications.

---

# 46. Auditability

Important system changes should be traceable.

The system should eventually be capable of determining:

- What changed
- When it changed
- Who or what changed it
- Why it changed
- What source supported the change
- Whether approval was required
- Whether approval occurred

This is particularly important for factual records and administrative changes.

---

# 47. Core Architectural Principle

APIG should connect information rather than isolate it.

A person should connect to positions.

Positions should connect to organizations.

Organizations should connect to jurisdictions.

Documents should connect to the entities they describe.

Meetings should connect to organizations, people, documents, and actions.

News should connect to people, organizations, events, and sources.

The result should be a connected information network rather than a collection of unrelated pages.

---

# 48. Future Specifications

This architecture will be expanded by more detailed specifications.

Likely areas include:

- Person Profile & Identity Model
- Government Hierarchy
- Agency Directory
- Organization Model
- Position Model
- Source and Document Provenance
- Meeting and Minutes System
- Database Schema
- Website Architecture
- Search System
- Newsroom Architecture
- FOIA System
- AI Operations
- Verification and Approval
- Security and Permissions
- Deployment Architecture

Each later specification should remain consistent with this architectural foundation unless this document is formally revised.

---

# 49. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root APIG AI resource index if the change affects resource navigation.
- Identify any specifications that must also be updated.

---

# 50. Summary

APIG is a connected information architecture.

Its fundamental entities include:

- Jurisdictions
- Organizations
- Agencies
- Positions
- People
- Documents
- Sources
- Meetings
- Events
- Claims
- Relationships

Its fundamental principles include:

- Evidence
- Provenance
- Verification
- Historical preservation
- Explicit relationships
- Multiple navigation paths
- Searchability
- Mobile usability
- Modularity
- Scalability
- AI-assisted operations
- Administrator oversight
- Portability between AI systems

The architecture is intended to allow APIG to grow from a small initial geographic implementation into a larger persistent information system without losing the relationships and evidence that make the information useful.

---

# END OF APIG-02