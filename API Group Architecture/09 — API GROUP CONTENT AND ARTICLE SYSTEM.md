# 09 — API GROUP CONTENT AND ARTICLE SYSTEM

## PURPOSE

This document defines how written content is created, organized, stored, displayed, searched, and connected within the API Group website.

API Group is a database-driven information system.

Articles are one type of content within that system.

Profiles are structured database records and are NOT hard-written articles.

An article may reference profiles, agencies, personnel, jurisdictions, civic organizations, documents, sources, and other records, but those records remain independent database entities.

---

# 1. API GROUP CONTENT STRUCTURE

The API Group website contains two fundamentally different kinds of information:

1. LIBRARY CONTENT
2. PROFILE/DATABASE INFORMATION

Library content is editorial and informational.

Profile information represents real-world entities and relationships being tracked by API Group.

---

# 2. API GROUP LIBRARY

The API Group Library is the public resource and information area for API Group.

Initial Library categories include:

- News
- Guides
- Checklists
- Agent Training
- About API Group

These are Library categories.

They are not Profile categories.

---

# 3. PROFILE SYSTEM

The Profile System is separate from the Library.

Profiles represent structured entities such as:

- Federal agencies
- State agencies
- County agencies
- City agencies
- Village agencies
- Civic organizations
- Personnel
- Jurisdictions
- Organizations

Profiles should be stored as database records.

---

# 4. ARTICLES ARE DATABASE RECORDS

Every article must be stored as a database record.

An article should contain structured fields such as:

- Title
- Slug
- Summary
- Body
- Content type
- Category
- Subcategory
- Author
- Status
- Publication date
- Updated date
- Featured status
- Tags
- Sources
- Related profiles
- Related articles
- Media

---

# 5. ARTICLES MUST NOT BE HARD-CODED

Articles must never require a developer to edit website code.

An editor or administrator with no coding experience must be able to:

- Create an article
- Edit an article
- Categorize an article
- Add tags
- Add sources
- Link profiles
- Feature an article
- Publish an article
- Unpublish an article
- Archive an article

---

# 6. CONTENT CATEGORIES

Categories must be database-driven.

The system must not assume that the number of categories is fixed forever.

An administrator must be able to create additional categories and subcategories through the CMS.

---

# 7. CATEGORY HIERARCHY

The CMS must support hierarchical categories.

Example:

Agent Training
→ Specifications
→ Legacy
→ APIG-01

Another example:

Guides
→ Research
→ Public Records

The system should not impose an unnecessary depth limitation.

If a future section requires many levels of hierarchy, the CMS must support it.

---

# 8. CATEGORY RECORDS

A category should itself be a database record.

It may contain:

- Name
- Description
- Parent category
- Sort order
- Image
- Visibility
- Template
- Sidebar configuration

---

# 9. AUTOMATIC CATEGORY NAVIGATION

When a new category is created, the CMS should be capable of automatically making it available in configured:

- Sidebars
- Navigation
- Category directories
- Breadcrumbs
- Search filters

The administrator should not have to manually edit HTML to add the category.

---

# 10. ARTICLE TAGS

Tags are separate from categories.

An article may have multiple tags.

Example:

Article:

"Understanding Illinois FOIA"

Tags:

Illinois
FOIA
Public Records
Government
Transparency

---

# 11. TAGS ARE DATABASE RECORDS

Tags should also be managed through the CMS.

The administrator should be able to:

- Create tags
- Rename tags
- Merge tags
- Remove tags
- Search by tags

---

# 12. FEATURED CONTENT

Any article may be marked:

FEATURED

Featured status should be a database property.

The administrator should not have to manually place the article on the homepage.

---

# 13. FEATURED ARTICLE AREAS

The website may have configurable featured areas.

Examples:

- Featured Articles
- Featured Guides
- Featured Agent Training
- Featured API Group News
- Featured Profiles

The component should retrieve the appropriate records from the database.

---

# 14. LATEST CONTENT

The API Group homepage should be capable of automatically displaying the latest published articles.

Default sorting:

Newest publication date first.

The number displayed should be configurable.

---

# 15. ARTICLE CARDS

Articles may be displayed as cards.

A card may contain:

- Thumbnail
- Category
- Title
- Summary
- Publication date
- Author
- Featured indicator

The card should link to the article's canonical page.

---

# 16. ARTICLE LISTS

Not every article collection should use cards.

Large collections may use compact lists.

This is particularly appropriate for:

- Agent Training
- Specifications
- Search results
- Archives
- Checklists
- Documentation

---

# 17. ARTICLE TEMPLATES

Articles must use reusable templates.

Initial article templates may include:

- Standard Article
- Guide
- Checklist
- Training Article
- API Group News
- Announcement

Additional templates may be created later through the CMS.

---

# 18. TEMPLATE SELECTION

The administrator should be able to select a template when creating an article.

Templates may also be assigned automatically based on:

- Category
- Content type
- Section
- Article type

---

# 19. ARTICLE CONTENT BLOCKS

The article editor should support structured content blocks.

Possible blocks include:

- Text
- Heading
- Image
- Video
- Document
- Quote
- Callout
- Table
- List
- Profile Reference
- Article Reference
- Source Reference

---

# 20. NO-CODE ARTICLE EDITING

The administrator should be able to create articles using the visual editor without writing HTML.

The editor should provide formatting controls for:

- Headings
- Paragraphs
- Lists
- Links
- Images
- Tables
- Callouts
- References

---

# 21. ARTICLE SOURCES

Articles should support source records.

Sources may include:

- Government documents
- Government websites
- Public records
- Meeting minutes
- News organizations
- Research
- Contributor material
- Uploaded documents

---

# 22. SOURCE REFERENCES

Sources should be linked to the article through database relationships whenever practical.

This allows the source to be reused or independently inspected.

---

# 23. PROFILE REFERENCES

Articles may reference profiles.

Example:

Article:
"White County Housing Authority"

Referenced records:

White County
Housing Authority
Pam Deig
Carmi

The article should link to the canonical database records.

---

# 24. PROFILE DATA MUST REMAIN CANONICAL

If an article references a person, agency, county, city, village, or civic organization, the article should not create a second hard-written copy of that entity.

The database profile remains the canonical record.

---

# 25. RELATED PROFILES

Article templates should be capable of displaying related profiles.

Example:

RELATED PROFILES

Pam Deig
Housing Authority
White County
Carmi

The records should be retrieved from the database.

---

# 26. RELATED ARTICLES

Articles may have relationships with other articles.

Relationships may be:

- Manually selected
- Category-based
- Tag-based
- Profile-based
- Automatically suggested

---

# 27. ARTICLE SEARCH

The API Group Library should support searching by:

- Title
- Keyword
- Category
- Subcategory
- Tag
- Author
- Date
- Source
- Profile
- Record type

---

# 28. SEARCH MUST BE DATABASE-DRIVEN

Search results must be generated from the database.

There should not be a manually maintained list of article URLs.

---

# 29. ARTICLE STATUS

Articles should support at least:

- Draft
- Review
- Published
- Unpublished
- Archived

---

# 30. DRAFT ARTICLES

Draft articles are not publicly visible.

An editor may work on an article without publishing it.

---

# 31. REVIEW WORKFLOW

Articles may enter a review state before publication.

Reviewers should be able to:

- Edit
- Approve
- Reject
- Return for revision

---

# 32. PUBLICATION

Only approved and published articles should appear in normal public searches and article directories.

---

# 33. SCHEDULED PUBLICATION

The system should support scheduled publication.

An administrator may specify:

- Publication date
- Publication time

The article becomes publicly available automatically.

---

# 34. ARTICLE REVISION HISTORY

The system should preserve article revisions.

Revision history should identify:

- Previous version
- Editor
- Date
- Changes

---

# 35. AUTHORS

Articles should retain authorship information.

Authors may include:

- API Group staff
- Editors
- Contributors
- Partners
- Researchers
- Other approved contributors

---

# 36. CONTRIBUTOR ATTRIBUTION

API Group may work with outside contributors and partners.

Examples include:

- Village Voice
- Edgar County Watchdogs
- Other approved contributors and organizations

Contributor attribution should be preserved in the article record.

---

# 37. ARTICLE MEDIA

Articles should support media.

Media may include:

- Photographs
- Graphics
- Documents
- Video
- Other approved media

Media should be managed through the CMS media library.

---

# 38. ARTICLE NAVIGATION

Article pages should support:

- Breadcrumbs
- Category navigation
- Related articles
- Related profiles
- Sources
- Sidebar navigation
- Footer

---

# 39. BREADCRUMBS

Breadcrumbs should be generated dynamically from the article's category hierarchy.

Example:

API Group
→ Library
→ Agent Training
→ Specifications
→ APIG-09

The breadcrumb should allow the user to return to previous levels.

---

# 40. ARTICLE SIDEBARS

Article pages may have:

- Left sidebar
- Right sidebar
- Both
- Neither

The administrator controls this through the CMS.

---

# 41. LEFT SIDEBAR USE

A left sidebar will generally be appropriate for hierarchical navigation.

Example:

Agent Training
→ Specifications
→ Legacy
→ APIG-01
→ APIG-02
→ APIG-03

---

# 42. RIGHT SIDEBAR USE

A right sidebar may provide contextual information.

Examples:

- Related profiles
- Related articles
- Sources
- Documents
- Connections
- Additional resources

---

# 43. DYNAMIC SIDEBAR CONTENT

Sidebar lists should be capable of being generated from database queries.

Example:

Sidebar:

Recent Agent Training

Query:

Category = Agent Training
Published = Yes
Sort = Newest

The sidebar updates automatically as new articles are added.

---

# 44. API GROUP HOMEPAGE CONTENT

The API Group homepage should be database-driven.

It may contain:

- Introductory information
- Library category cards
- Profile system entry points
- Featured articles
- Latest articles
- Featured profiles
- Recent records
- Search
- Footer

---

# 45. HOMEPAGE CATEGORY CARDS

Major API Group sections may be represented by cards.

The cards should represent categories or sections rather than individual hard-coded pages.

Example:

API Group Library

Cards:

News
Guides
Checklists
Agent Training
About API Group

---

# 46. HOMEPAGE FEATURED CONTENT

The administrator should be able to mark an article or profile as featured.

The homepage should automatically retrieve featured records.

---

# 47. HOMEPAGE LATEST CONTENT

The homepage should automatically retrieve the newest published content.

No manual homepage editing should be required when a new article is published.

---

# 48. PROFILE CONTENT ON ARTICLE PAGES

An article may display information pulled from profiles.

Example:

Article:

"White County Housing Authority"

Profile component:

Pam Deig
Executive Director

The profile information is retrieved from the database.

---

# 49. ARTICLE CONTENT AND PROFILE CONTENT MUST REMAIN SEPARATE

An article can reference a profile.

A profile can reference an article.

Neither should become dependent on the other for its existence.

---

# 50. CROSS-CONNECTIONS

The system must support relationships between:

- Articles
- People
- Agencies
- Organizations
- Counties
- Cities
- Villages
- Civic organizations
- Sources
- Documents

This allows users to move between editorial content and structured information.

---

# 51. API GROUP NEWS

API Group News is specifically content about API Group.

Examples:

- API Group announcements
- Website developments
- New research
- New features
- Organizational developments
- Contributor announcements
- Project updates

API Group News belongs to the API Group Library.

---

# 52. MONSTER NEWS IS NOT API GROUP NEWS

Monster News is a separate website context.

Monster News does not belong inside the API Group Library.

Monster News should have its own:

- Articles
- Categories
- Templates
- Navigation
- Homepage
- Editorial workflow
- Branding
- Control panel

---

# 53. CROSS-SITE REFERENCES

Monster News may intentionally reference API Group information.

Example:

Monster News article
→ API Group Personnel Profile

The article remains a Monster News article.

The personnel record remains an API Group profile.

---

# 54. NO AUTOMATIC CONTENT MERGING

API Group articles must not automatically become Monster News articles.

Monster News articles must not automatically become API Group articles.

The two editorial systems remain independent.

---

# 55. DATABASE-FIRST PRINCIPLE

The system must always prefer:

DATABASE RECORD
→ RELATIONSHIP
→ TEMPLATE
→ DISPLAY

rather than:

HARDCODED INFORMATION
→ STATIC PAGE
→ MANUAL LINK

---

# 56. AUTOMATIC UPDATES

When a new article is created or published, all database-driven components should update automatically.

Examples:

New article
→ Category listing updates

New featured article
→ Featured section updates

New article
→ Search updates

New article
→ Related-content queries may update

New category
→ Configured category navigation updates

---

# 57. EDITORIAL PRINCIPLE

Editors should concentrate on the information.

The CMS should handle:

- Storage
- Relationships
- Navigation
- Search
- Presentation
- Featured content
- Latest content
- Breadcrumbs
- Sidebar generation

---

# 58. FINAL PRINCIPLE

API GROUP ARTICLES ARE DATABASE RECORDS.

API GROUP PROFILES ARE DATABASE RECORDS.

THEY ARE DIFFERENT TYPES OF RECORDS.

ARTICLES MAY REFERENCE PROFILES.

PROFILES MAY REFERENCE ARTICLES.

THE DATABASE STORES THE INFORMATION.

RELATIONSHIPS CONNECT THE INFORMATION.

TEMPLATES PRESENT THE INFORMATION.

THE CMS ALLOWS NON-CODERS TO MANAGE THE INFORMATION.

NAVIGATION, SIDEBARS, BREADCRUMBS, SEARCH, FEATURED CONTENT, AND LATEST CONTENT SHOULD BE GENERATED FROM THE DATABASE WHEREVER POSSIBLE.

NOTHING SHOULD REQUIRE A DEVELOPER TO MANUALLY ADD A NEW ARTICLE, PROFILE, CATEGORY, COUNTY, AGENCY, PERSON, OR OTHER DATABASE RECORD TO A PAGE.