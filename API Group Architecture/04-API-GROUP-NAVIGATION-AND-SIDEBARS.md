# 04 — API GROUP NAVIGATION AND SIDEBARS

## PURPOSE

This document defines how navigation, breadcrumbs, sidebars, and page-to-page movement work throughout the API Group website.

The navigation system must make a database-driven information system understandable to the public while giving a non-technical administrator complete control over page layouts and navigation.

The navigation is not the database.

The database contains entities and relationships.

Navigation provides ways for users to discover and move through those entities.

---

# 1. API GROUP IS THE PRIMARY WEBSITE

API Group is the primary website context.

Its purpose is to house the complete API Group information system.

The primary API Group areas include:

- API Group Library
- Profiles

Monster News is NOT part of this navigation.

Monster News is a completely independent website/portal and must have its own navigation and administration.

---

# 2. API GROUP AND MONSTER NEWS MUST REMAIN SEPARATE

The system must treat API Group and Monster News as two independent website contexts.

API Group:

- Own logo
- Own navigation
- Own page templates
- Own content
- Own sidebars
- Own administration
- Own control panel
- Own visual presentation

Monster News:

- Own logo
- Own navigation
- Own page templates
- Own news content
- Own sidebars
- Own administration
- Own control panel
- Own visual presentation

API Group data may be referenced by Monster News when appropriate.

For example, a Monster News article may reference:

- A person
- An agency
- A county
- A city
- A civic organization

That does not make API Group a subsection of Monster News.

Likewise, Monster News must never appear as an ordinary API Group navigation category.

---

# 3. PRIMARY API GROUP NAVIGATION

The exact wording of the public navigation may change during design.

The architecture must support a small number of prominent primary links that lead to major areas of the API Group system.

The primary navigation should not attempt to expose every database category.

Instead, it should provide clear entry points into the information system.

---

# 4. API GROUP LIBRARY

The API Group Library is the public resource and information area for API Group itself.

It may contain:

- API Group website news
- About API Group
- Contact information
- Guides
- Tips and tricks
- Help
- Checklists
- Contributions
- Partner information
- Contributor information
- Agent Training
- Other API Group resource materials

The Library is not the Profile database.

The Library contains API Group's own informational and editorial resources.

---

# 5. PROFILES

Profiles are a separate major area of the API Group system.

Profiles contain database-driven information about entities being researched and documented.

Examples include:

- Agency Profiles
- Personnel Profiles
- Civic Profiles
- Jurisdiction Profiles
- Contributor Profiles
- Partner Profiles

Profiles are not hard-written articles.

They are database records rendered through templates.

---

# 6. AGENCY PROFILES

Agency Profiles are a primary discovery path for organizational information.

The initial classifications are:

- Federal
- State
- County
- City
- Village
- Civic

These classifications should be database-driven and extensible.

The administrator must be able to add another classification without manually rebuilding every page.

---

# 7. PERSONNEL

Personnel must be independently discoverable.

A user should not have to navigate through:

Federal
→ State
→ County
→ City
→ Village

before finding a person.

A person may have relationships with multiple jurisdictions and organizations.

Personnel therefore requires its own search and discovery path.

---

# 8. CIVIC

Civic organizations must also be independently discoverable.

A civic organization may relate to:

- A county
- A city
- A village
- Multiple jurisdictions
- Personnel
- Agencies
- Other organizations

Civic information must not be forced into a single government hierarchy.

---

# 9. RECORD ROOM / PROFILE DISCOVERY

The API Group public discovery experience should make it obvious that users can search and browse the collection.

The exact public title may be:

Record Room

or another final API Group Library/Profile title selected during design.

The important principle is that the interface provides both:

SEARCH

and

BROWSE.

---

# 10. LEFT SIDEBAR DEFAULT

The primary navigation pattern should favor a left sidebar.

The left sidebar provides contextual navigation as users move through the hierarchy.

Example:

API Group
→ Profiles
→ Agency Profiles

Left Sidebar:

Federal
State
County
City
Village
Civic
Personnel

Main Content:

Agency Profiles

---

# 11. SIDEBAR IS OPTIONAL

Every major page should support:

- No sidebar
- Left sidebar
- Right sidebar
- Both sidebars

The administrator determines the appropriate layout.

The system must not force every page to have the same sidebar configuration.

---

# 12. SIDEBAR CONFIGURATION

A non-technical administrator must be able to configure the sidebar from the CMS.

The administrator should be able to:

- Turn sidebar on
- Turn sidebar off
- Choose left
- Choose right
- Choose both
- Change width
- Change order
- Add sections
- Remove sections
- Add links
- Remove links
- Add database-driven lists
- Add related content
- Add custom content
- Expand/collapse sections

No coding should be required.

---

# 13. SIDEBAR CONTENT TYPES

Sidebar components may include:

- Navigation links
- Database entity lists
- Related profiles
- Related records
- Search
- Filters
- Categories
- Subcategories
- Custom links
- Text
- Images
- Widgets
- Other CMS components

The administrator should be able to arrange these components visually.

---

# 14. DATABASE-DRIVEN SIDEBAR LISTS

When a sidebar represents database entities, it must be generated from the database.

Example:

COUNTIES

White County
Edgar County
Vermilion County

If a new county is added:

New County

the sidebar should automatically include it.

The administrator should not have to manually create a navigation link.

This principle applies to:

- Counties
- Cities
- Villages
- Agencies
- Personnel
- Civic organizations
- Other database entities

---

# 15. EXPANDABLE SIDEBARS

Sidebar sections should support expansion and collapse.

Example:

COUNTIES
▸ White County
▸ Edgar County
▸ Vermilion County

An entity may contain additional navigation.

Example:

WHITE COUNTY
▾ Agencies
▾ Personnel
▾ Cities
▾ Villages
▾ Civic
▾ Records

The exact structure depends on the current page context.

---

# 16. CONTEXTUAL SIDEBARS

The sidebar changes as the user moves deeper into the information system.

Example:

PAGE 1

Agency Profiles

Sidebar:

Federal
State
County
City
Village
Civic
Personnel

The user selects:

County

---

PAGE 2

County Profiles

Sidebar:

Counties
→ White County
→ Edgar County
→ Vermilion County
→ ...

The user selects:

White County

---

PAGE 3

White County

Sidebar:

Overview
Agencies
Personnel
Cities
Villages
Civic
Records

The user selects:

Housing Authority

---

PAGE 4

Housing Authority

Sidebar:

Overview
Departments
Personnel
Records
Documents
Related Organizations

Each page represents a new contextual level.

---

# 17. THE SIDEBAR DOES NOT DEFINE OWNERSHIP

A sidebar link does not mean that the destination is permanently nested beneath the current entity in the database.

For example:

White County
→ Housing Authority
→ Pam Deig

does not mean Pam Deig belongs exclusively to White County.

Pam Deig remains an independent person entity.

The relationship may be:

Pam Deig
→ works_for
→ Housing Authority

and:

Housing Authority
→ associated_with
→ White County

and:

Pam Deig
→ associated_with
→ City of Carmi

The navigation merely provides one path to the person.

---

# 18. BREADCRUMBS

Breadcrumbs must appear above the primary page content.

They show the user's current navigation context.

Example:

API Group
→ Profiles
→ Agency Profiles
→ County
→ White County
→ Housing Authority

Breadcrumbs should be clickable.

A user should be able to move backward to any previous level.

---

# 19. BREADCRUMBS REMAIN VISIBLE

The breadcrumb should remain available as users navigate deeper into the system.

The user should never feel trapped inside a deep hierarchy.

Example:

API Group
→ Profiles
→ Agency Profiles
→ State
→ Illinois
→ Agency
→ Attorney General
→ FOIA

The user can select:

Illinois

to return to the Illinois context.

Or:

Agency Profiles

to return to the Agency Profiles level.

---

# 20. BREADCRUMB CONTEXT VS. CANONICAL URL

The breadcrumb represents the user's navigation path.

The profile's canonical identity remains independent.

A person may be reached through:

Personnel
→ Person

or:

Agency
→ County
→ Agency
→ Personnel
→ Person

The person should still have one canonical profile.

The breadcrumb reflects the route the user followed.

---

# 21. NEW PAGE AT EACH MAJOR LEVEL

Major navigation transitions should produce a new page/view.

The user should experience the system as moving through distinct sections rather than simply expanding one enormous page.

Example:

API Group Library

opens a Library landing page.

Profiles

opens a Profiles landing page.

Agency Profiles

opens an Agency Profiles page.

County

opens a County directory.

White County

opens the White County page.

Housing Authority

opens the agency profile.

Pam Deig

opens the personnel profile.

---

# 22. PAGE TEMPLATES

Each major page level should be template-driven.

Possible templates include:

- Landing Page
- Directory Page
- Category Page
- Subcategory Page
- Jurisdiction Page
- Agency Profile
- Personnel Profile
- Civic Profile
- Search Results
- Article
- Resource
- Record

The administrator must be able to assign templates without coding.

---

# 23. PAGE LAYOUT CONTROLS

The administrator should be able to configure each page template with:

- Header
- Logo
- Primary navigation
- Breadcrumb
- Main content
- Left sidebar
- Right sidebar
- Footer

Each element should be independently configurable.

---

# 24. HEADER

The API Group header should contain:

- API Group logo
- Primary navigation
- Appropriate controls
- Optional search
- Other administrator-selected components

The header must use the API Group branding.

It must not display Monster News branding on API Group pages.

---

# 25. LOGO

The correct API Group logo must be used throughout the API Group website.

The Monster News logo belongs to the Monster News portal.

The CMS should allow the administrator to configure logo placement and sizing without coding.

---

# 26. FOOTER

The API Group footer should be independently configurable.

It may contain:

- API Group information
- Navigation
- Contact
- Contributors
- Partners
- Legal information
- Additional resources
- Other administrator-defined components

Monster News footer content must remain separate.

---

# 27. CONTRIBUTOR AND PARTNER INFORMATION

API Group should support profiles or information for contributors and partners.

Examples include:

- Village Voice
- Edgar County Watchdogs
- Other contributors
- Other partners

These relationships should be represented through database records when appropriate.

Contributor and partner information should not be treated as ordinary manually typed sidebar links when it is actually database information.

---

# 28. SEARCH WITHIN NAVIGATION

Search should remain available even when the user is deep within the hierarchy.

For example, while viewing:

White County
→ Agencies

the user should still be able to search for a person or agency directly.

The hierarchy is a browsing mechanism.

Search is a direct discovery mechanism.

Both are necessary.

---

# 29. NAVIGATION AND DATABASE GROWTH

The navigation must automatically accommodate growth.

If the database contains:

10 counties

the county directory shows 10.

If it contains:

50 counties

the county directory shows 50.

If it contains:

1,000 personnel records

the personnel directory shows the available records using an appropriate compact presentation.

The system must not require redesign simply because the number of records increases.

---

# 30. NAVIGATION AND NEW CATEGORIES

When the administrator creates a new category that is configured as navigable, the CMS should be able to automatically expose it in the appropriate:

- Sidebar
- Directory
- Search filter
- Navigation
- Breadcrumb
- Landing page

The administrator should not need to create a separate webpage manually.

---

# 31. CUSTOM NAVIGATION

The CMS should also support manually created navigation items.

This is necessary for pages that are not database entities.

Examples:

- About API Group
- Contact
- Help
- Contributions
- Agent Training

The administrator should be able to combine:

DATABASE-DRIVEN LINKS

with

MANUALLY CONFIGURED LINKS.

---

# 32. NAVIGATION ORDER

The administrator must control navigation order.

For example:

Agency Profiles
Personnel
Civic

or:

Federal
State
County
City
Village
Civic

The order should be configurable without coding.

---

# 33. MOBILE NAVIGATION

The same hierarchy must remain usable on mobile devices.

The sidebar may become:

- A collapsible drawer
- An expandable menu
- A mobile navigation panel

The database-driven behavior must remain unchanged.

---

# 34. VISUAL DESIGN

The existing API Group website is the visual reference.

The new CMS should preserve the qualities that make the existing site effective:

- Strong editorial layout
- Clear cards
- Strong typography
- Consistent spacing
- Clear hierarchy
- Black, white, gold, and appropriate pink accents
- Strong visual identity
- Clean navigation

The new CMS architecture must change how content is managed without unnecessarily changing the visual language users already like.

---

# 35. NAVIGATION SHOULD FEEL SIMPLE

The underlying database may become extremely complex.

The public navigation should not feel complicated.

Users should be able to understand:

WHERE THEY ARE

WHERE THEY CAME FROM

WHAT THEY CAN SELECT NEXT

HOW TO SEARCH

HOW TO RETURN

The breadcrumb and contextual sidebar work together to accomplish this.

---

# 36. FINAL NAVIGATION PRINCIPLE

THE HEADER PROVIDES GLOBAL NAVIGATION.

THE BREADCRUMB PROVIDES NAVIGATION CONTEXT.

THE SIDEBAR PROVIDES LOCAL NAVIGATION.

THE DATABASE PROVIDES THE AVAILABLE ENTITIES.

THE RELATIONSHIPS PROVIDE THE CONNECTIONS.

THE TEMPLATE PROVIDES THE PRESENTATION.

THE ADMINISTRATOR CONTROLS THE LAYOUT.

THE USER CAN SEARCH OR BROWSE.

The navigation system must never become a collection of manually maintained pages and links.

It must remain a dynamic interface over the database.

---

# 37. CORE EXAMPLE

A user begins at:

API GROUP

They select:

PROFILES

They select:

AGENCY PROFILES

They select:

COUNTY

They select:

WHITE COUNTY

They select:

HOUSING AUTHORITY

They select:

PERSONNEL

They select:

PAM DEIG

At every level:

- The breadcrumb shows the path.
- The sidebar changes to match the current context.
- The content changes to match the current page.
- Database relationships determine what can be discovered.
- The administrator controls the presentation.
- The underlying entities remain independent.

This is the intended navigation model for the API Group website.