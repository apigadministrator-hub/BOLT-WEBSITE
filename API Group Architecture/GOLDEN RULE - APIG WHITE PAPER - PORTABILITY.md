# GOLDEN RULE — APIG WHITE PAPER: PORTABILITY

## THE GOLDEN RULE

Before API Group does anything, it must ask:

**Is this portable?**

If the answer is no, the action must not proceed without explicit review and approval.

The data belongs to API Group.

The website, CMS, database technology, plugins, templates, frontend, hosting provider, and AI system are tools used to manage and present that data.

They are not the owner of the data.

---

# 1. PORTABILITY IS NON-NEGOTIABLE

Portability is a foundational architectural requirement of API Group.

Every system decision must preserve the ability to move API Group's information to another system.

This applies to:

- Database records
- Profiles
- Personnel
- Agencies
- Counties
- Cities
- Villages
- Civic organizations
- Federal records
- State records
- Articles
- Documents
- Sources
- Citations
- Images
- Media
- Relationships
- Categories
- Tags
- Navigation
- Sidebar configuration
- Templates
- Metadata
- Revision history where practical
- AI-generated information
- Administrative configuration

---

# 2. DATA BELONGS TO API GROUP

The underlying information is the most valuable asset.

The website is a presentation and management system for that information.

The architecture must never reverse this relationship.

Correct:

DATA
→ STRUCTURED DATABASE
→ API / DATA ACCESS
→ APPLICATION
→ PRESENTATION

Incorrect:

WEBSITE
→ PAGES
→ PLUGINS
→ HARD-CODED CONTENT
→ DATA

---

# 3. BEFORE ANYTHING IS DONE

Before creating, modifying, installing, configuring, deleting, importing, exporting, or restructuring anything, the system must evaluate portability.

The system should ask:

- Where will this information live?
- What format will it use?
- Can the information be exported?
- Can another system understand it?
- Are relationships preserved?
- Are identifiers preserved?
- Are sources preserved?
- Are metadata preserved?
- Is the information dependent upon a proprietary feature?
- Could the feature be recreated elsewhere?
- Could the data be migrated to another CMS?
- Could the data be migrated to another database?
- Could the data be used by another application?
- Could another AI system work with the same information?

---

# 4. PORTABILITY CHECK BEFORE ACTION

Every significant action must pass a portability check before execution.

The process is:

1. Identify the proposed change.
2. Identify what data or configuration it affects.
3. Determine how that information will be stored.
4. Determine whether the information remains exportable.
5. Determine whether relationships remain intact.
6. Determine whether the change creates vendor or platform lock-in.
7. Determine whether the change can be reconstructed elsewhere.
8. If portability is preserved, proceed.
9. If portability is uncertain, stop and flag the issue.
10. If portability is violated, do not proceed without explicit approval.

---

# 5. PORTABILITY TAKES PRIORITY

Convenience does not override portability.

A faster solution is not automatically a better solution.

A plugin is not automatically acceptable because it solves a problem quickly.

A CMS feature is not automatically acceptable because it looks good.

An AI-generated shortcut is not automatically acceptable because it saves time.

If the shortcut creates unacceptable dependence on a particular system, it violates the Golden Rule.

---

# 6. STRUCTURED DATA

Important information should be stored as structured data whenever practical.

Examples:

A person should be a person record.

An agency should be an agency record.

A county should be a county record.

A relationship should be a relationship record.

A source should be a source record.

An article should be an article record.

The public webpage should be generated from those records.

---

# 7. NO CRITICAL DATA ONLY IN PRESENTATION

Critical information must not exist only inside:

- HTML
- CSS
- JavaScript
- Page-builder layouts
- Theme files
- Plugin-specific fields
- Images
- Screenshots
- Static page content
- Proprietary widgets

If information is important to the API Group collection, it should exist independently of the presentation layer.

---

# 8. PROFILES MUST REMAIN PORTABLE

Profiles are database records.

A profile must not become permanently dependent upon the webpage used to display it.

The following must remain independently exportable:

- Profile identifier
- Profile type
- Name
- Attributes
- Relationships
- Sources
- Dates
- Status
- Metadata

---

# 9. RELATIONSHIPS MUST REMAIN PORTABLE

Relationships are data.

For example:

PERSON
→ works_for
→ AGENCY

The relationship must be stored in a form that another system can understand.

It must not exist only as a hyperlink embedded in an article.

---

# 10. IDENTIFIERS

Records should have stable identifiers.

The identifier should remain consistent when the presentation changes.

Changing:

- Website
- URL
- Theme
- Template
- CMS
- Frontend

should not require recreating the underlying entity.

---

# 11. ARTICLES

Articles must remain portable content records.

An article should be exportable with:

- Title
- Body
- Author
- Date
- Status
- Categories
- Tags
- Sources
- References
- Related profiles
- Media references
- Metadata

---

# 12. MEDIA

Images and documents should not become permanently trapped inside a proprietary media system.

Media should retain:

- Stable identifier
- Filename
- File type
- Metadata
- Source
- Relationships
- Caption where applicable
- Alt text where applicable
- Copyright information where applicable

---

# 13. SOURCES

Sources are part of the data.

A source reference must remain understandable outside the website that originally displayed it.

Where appropriate, preserve:

- Source title
- Source organization
- Source URL
- Publication date
- Retrieval date
- Document identifier
- Citation information
- Relationship to the record

---

# 14. TAXONOMIES AND CATEGORIES

Categories, tags, record types, and classifications must be exportable.

The system should not rely upon a proprietary category system that cannot be reconstructed elsewhere.

---

# 15. NAVIGATION

Navigation is presentation configuration.

The underlying records must not depend upon the navigation menu.

If a menu disappears, the data must remain intact.

If the website is rebuilt, the navigation can be recreated from the database and configuration.

---

# 16. SIDEBARS

Sidebars are presentation configuration.

A sidebar may contain:

- Links
- Queries
- Directory lists
- Related records
- Widgets
- Text
- Images

But the underlying information must remain independent of the sidebar.

A database-driven county list must remain a database query, not a collection of manually typed sidebar links.

---

# 17. DYNAMIC CONTENT

Dynamic content should be generated from structured information.

Example:

DATABASE
→ County records
→ Query
→ County directory
→ Sidebar

The sidebar is not the source of the county list.

The database is.

---

# 18. TEMPLATES

Templates are presentation instructions.

Templates may change.

The data must survive the template.

A new template should be capable of rendering the same underlying records.

---

# 19. CMS INDEPENDENCE

API Group should not become permanently dependent upon one CMS.

The architecture should allow the collection to be migrated to another CMS or application.

A CMS may be replaced.

The data must survive.

---

# 20. DATABASE INDEPENDENCE

The architecture should avoid unnecessary dependence on proprietary database features.

Where practical, information should use portable, well-documented structures.

The goal is not to prevent the use of advanced database technology.

The goal is to prevent unnecessary lock-in.

---

# 21. PLUGIN INDEPENDENCE

Plugins may provide useful functionality.

However, critical API Group information should not be trapped inside a plugin-specific storage system when a portable alternative is practical.

Before adopting a plugin, determine:

- What data does it create?
- Where does it store it?
- Can that data be exported?
- Can the data be understood without the plugin?
- Can the functionality be replaced?
- Can the data be migrated?

---

# 22. AI INDEPENDENCE

API Group must not become dependent upon one AI model.

AI is a tool for managing and enriching the collection.

AI-generated information should enter the same structured data system as human-created information.

Another AI system should be capable of reading and working with the same records.

---

# 23. AI-GENERATED PROFILES

AI may create or update profiles.

The resulting information must be stored as structured records.

It must not exist only inside the AI's generated webpage output.

---

# 24. AI MUST PRESERVE SOURCES

When AI adds information based on source material, the source relationship should be preserved whenever practical.

The goal is to maintain the chain:

SOURCE
→ INFORMATION
→ DATABASE RECORD
→ PROFILE
→ PUBLIC PRESENTATION

---

# 25. AI MUST NOT CREATE LOCK-IN

AI should not create proprietary structures that prevent API Group from moving its information to another system.

If an AI tool produces a useful structure, API Group should retain the underlying information in a portable format.

---

# 26. MONSTER NEWS

Monster News is a separate system from API Group.

Monster News must maintain its own independent portability.

Monster News must not become technically dependent upon API Group.

API Group must not become technically dependent upon Monster News.

---

# 27. CROSS-SYSTEM REFERENCES

API Group and Monster News may reference one another.

For example:

Monster News article
→ references API Group profile

API Group profile
→ references Monster News article

These should be relationships or references.

They should not create destructive system dependencies.

Either system should remain capable of existing independently.

---

# 28. EXPORTABILITY

The system should provide practical methods for exporting the API Group collection.

Exports should preserve, where applicable:

- Records
- Identifiers
- Relationships
- Categories
- Sources
- Media references
- Metadata
- Dates
- Status
- Revision information

---

# 29. IMPORTABILITY

Portability requires more than export.

The exported collection should be sufficiently structured that another application can import it.

The architecture should document:

- Data schema
- Record types
- Field definitions
- Relationships
- Identifier rules
- Taxonomies
- Media relationships
- Source relationships

---

# 30. SCHEMA DOCUMENTATION

The structure of the database must be documented.

The documentation should explain:

- What each record type means
- What each field means
- What each relationship means
- Which fields are required
- Which fields are optional
- How records are identified
- How records relate to one another

---

# 31. OPEN FORMATS

Where practical, use widely understood and documented formats.

Examples may include:

- JSON
- CSV
- XML
- Markdown
- Plain text
- Standard image formats
- Standard document formats

The appropriate format depends on the type of information.

---

# 32. MARKDOWN

Markdown should be used where appropriate for portable human-readable documentation.

Markdown documentation should not depend upon a particular CMS.

This architecture itself should remain readable outside the website.

---

# 33. HUMAN READABILITY

Portable data should be understandable by humans as well as machines.

Documentation should make it possible for a technically competent person to understand:

- What the data represents
- How the records connect
- How to migrate the information

---

# 34. MACHINE READABILITY

Portable data should also be structured so software can process it.

The collection should be usable by:

- Websites
- Applications
- Search systems
- Databases
- AI systems
- Data analysis tools

---

# 35. NO HARD-CODED RECORD LISTS

Do not hard-code database-driven records into website templates.

Do not manually maintain:

- County lists
- Agency lists
- Personnel lists
- City lists
- Village lists
- Civic organization lists

when those lists can be generated from the database.

---

# 36. NEW RECORD TEST

When a new record is added, ask:

Can the system automatically discover it?

If a new county is added, the appropriate directory and database-driven sidebar should be able to display it without manually editing a webpage.

---

# 37. CHANGE TEST

Whenever a system component is changed, ask:

Would the underlying data still work if this component disappeared tomorrow?

If the answer is no, the architecture requires review.

---

# 38. REPLACEMENT TEST

For major components, ask:

Could we replace this component without rebuilding the collection from scratch?

Examples:

Could we replace the CMS?

Could we replace the frontend?

Could we replace the database?

Could we replace the AI?

Could we replace the hosting provider?

Could we replace the search system?

If the answer is no, investigate why.

---

# 39. DISASTER RECOVERY

Portability supports disaster recovery.

API Group should maintain the ability to restore its collection independently of the website's current implementation.

The website should be replaceable.

The collection must survive.

---

# 40. BACKUP PRINCIPLE

Backups should preserve the underlying data, not merely copies of rendered webpages.

A database backup and portable data export are both valuable.

---

# 41. MIGRATION TEST

The architecture should eventually be tested by attempting to reconstruct a portion of the system elsewhere.

For example:

Export:

- Several profiles
- Several relationships
- Several articles
- Several sources

Then import them into a separate environment.

If the information and relationships survive, portability is demonstrated.

---

# 42. PORTABILITY AUDIT

Major architectural changes should be subject to a portability audit.

The audit should ask:

- What changed?
- What data is affected?
- What dependencies were introduced?
- Can the affected information still be exported?
- Can the information be reconstructed elsewhere?
- Were identifiers preserved?
- Were relationships preserved?
- Were sources preserved?
- Was any proprietary dependency introduced?

---

# 43. PORTABILITY FAILURE

If a proposed change fails the portability test:

DO NOT SILENTLY IMPLEMENT IT.

The system should explain:

- What is not portable
- Why it is not portable
- What dependency it creates
- What alternatives exist
- What would be required to approve the exception

---

# 44. EXCEPTIONS

An exception to portability may be considered only when there is a compelling reason.

Any exception should be documented.

The documentation should identify:

- The exception
- The reason
- The affected system
- The affected data
- The dependency
- The migration risk
- The planned mitigation

Portability exceptions should never become accidental permanent architecture.

---

# 45. PORTABILITY BEFORE SPEED

API Group wants the website to launch quickly.

Speed is important.

However:

**Speed must not create permanent technical debt that traps the collection inside a temporary implementation.**

Build quickly.

Build simply.

Build portably.

---

# 46. PORTABILITY BEFORE APPEARANCE

A visually impressive feature is not more important than preserving the data.

A beautiful page that creates data lock-in is an architectural failure.

---

# 47. PORTABILITY BEFORE CONVENIENCE

The easiest implementation is not necessarily the correct implementation.

When two approaches provide approximately the same result, prefer the one that preserves greater portability.

---

# 48. PORTABILITY BEFORE AUTOMATION

Automation must not create hidden dependencies.

Before automating a process, determine:

- What data is created?
- Where is it stored?
- What format is used?
- Can it be exported?
- Can the process be replaced?

---

# 49. PORTABILITY BEFORE AI ACTION

Before AI makes a change to API Group:

CHECK PORTABILITY.

If portable:

PROCEED.

If uncertain:

STOP AND FLAG.

If not portable:

DO NOT PROCEED WITHOUT EXPLICIT APPROVAL.

---

# 50. PORTABILITY AFTER EVERY CHANGE

After making a change, the system must verify that portability remains intact.

The verification should consider:

- Data integrity
- Record structure
- Relationships
- Sources
- Identifiers
- Exportability
- System dependencies
- Configuration dependencies

---

# 51. REQUIRED FINAL CONFIRMATION

After a change has been completed and portability has been verified, the final confirmation to the administrator must be:

**Portability confirmed.**

This confirmation is required.

It should be the final statement after a completed change when the system has verified portability.

---

# 52. IF PORTABILITY CANNOT BE CONFIRMED

The system must not claim:

"Portability confirmed."

unless it has actually performed the required verification.

Instead, it must clearly state that portability could not be confirmed and identify the unresolved issue.

---

# 53. PORTABILITY IS A CONTINUOUS REQUIREMENT

Portability is not something checked once at launch.

It applies:

- Before development
- During development
- During content creation
- During database changes
- During plugin installation
- During template changes
- During AI operations
- During migrations
- During upgrades
- During redesigns
- During maintenance

---

# 54. THE APIG PORTABILITY TEST

Before any significant decision, apply this test:

1. Does the data remain independent?
2. Does the data remain structured?
3. Does the data remain exportable?
4. Do relationships remain intact?
5. Do identifiers remain stable?
6. Are sources preserved?
7. Can another system understand the data?
8. Can another application use the data?
9. Can the current component be replaced?
10. Can the collection survive without the current website?

If any answer is unclear, investigate before proceeding.

---

# 55. THE GOLDEN RULE IN ONE SENTENCE

**Before API Group does anything, make sure it is portable.**

---

# 56. THE GOLDEN RULE IN TWO SENTENCES

**The data belongs to API Group. The system is only a tool for storing, managing, connecting, and presenting that data.**

**Before every significant change, verify portability; after every completed change, verify it again and confirm: "Portability confirmed."**

---

# 57. FINAL ARCHITECTURAL STANDARD

API GROUP MUST ALWAYS BE ABLE TO SAY:

WE CAN MOVE OUR DATA.

WE CAN MOVE OUR PROFILES.

WE CAN MOVE OUR RELATIONSHIPS.

WE CAN MOVE OUR ARTICLES.

WE CAN MOVE OUR SOURCES.

WE CAN MOVE OUR MEDIA.

WE CAN CHANGE OUR CMS.

WE CAN CHANGE OUR DATABASE.

WE CAN CHANGE OUR FRONTEND.

WE CAN CHANGE OUR HOST.

WE CAN CHANGE OUR AI.

WE CAN REBUILD THE WEBSITE.

WE CAN REBUILD THE APPLICATION.

THE COLLECTION SURVIVES.

THAT IS PORTABILITY.

THAT IS THE GOLDEN RULE.