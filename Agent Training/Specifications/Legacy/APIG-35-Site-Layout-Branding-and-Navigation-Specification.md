# APIG-35 — Site Layout, Branding and Navigation Specification

## Purpose

APIG shall maintain a consistent, recognizable, accessible, and reusable visual and navigational framework across the public website and associated user interfaces.

This specification defines the presentation structure of APIG, including logos, branding, headers, navigation, page layouts, footers, menus, and other common interface elements.

This specification governs presentation and navigation. It does not define the underlying database, investigative data model, entity relationships, AI operations, or other system architecture.

## Branding

APIG shall maintain consistent use of its approved visual identity throughout the website and associated interfaces.

Branding elements may include:

* APIG name
* APIG logo
* Logo variations
* Wordmarks
* Icons
* Typography
* Approved visual treatments
* Other officially adopted brand elements

Brand assets shall be maintained as identifiable project assets and shall have defined locations and usage requirements.

## Logos

The system shall support the appropriate APIG logo or logo variation for each applicable context.

Logo usage shall preserve:

* Correct proportions
* Appropriate sizing
* Adequate surrounding space
* Legibility
* Consistent placement
* Appropriate use on light and dark backgrounds when applicable

Unauthorized alteration, distortion, or inconsistent reproduction of official logos shall be avoided.

## Global Site Structure

The APIG website shall use a consistent global layout.

Common interface elements may include:

* Header
* APIG logo or wordmark
* Primary navigation
* Secondary navigation where appropriate
* Search
* Main content area
* Contextual navigation
* Footer
* Required legal or informational links

Global elements should remain consistent throughout the site unless a documented reason requires a different presentation.

## Navigation

Navigation shall allow users to understand where they are within the APIG information system and how to reach related areas.

Navigation should be based on the structure and function of the system rather than arbitrary page organization.

Navigation may include:

* Primary site sections
* Secondary navigation
* Breadcrumbs
* Related-record navigation
* Contextual links
* Search
* Filters
* Pagination
* Back or return navigation
* Links between related entities

Navigation should make relationships between information discoverable without requiring users to understand the underlying database architecture.

## Page Layout

Pages shall use a consistent structural hierarchy.

A typical page should provide:

1. Site identification and global navigation.
2. Page or record title.
3. Relevant contextual information.
4. Primary content.
5. Related information or navigation where appropriate.
6. Consistent supporting interface elements.

Layouts may vary according to the type of information being presented, but variations shall remain consistent with the overall APIG design system.

## Entity and Record Presentation

Pages representing APIG entities should use consistent layouts appropriate to the entity type.

Examples include:

* Person
* Position
* Office
* Agency
* Organization
* Meeting
* Document
* Article
* Location
* Source
* Investigation

The presentation layer should make important relationships and relevant source information accessible from the record without requiring users to navigate through unrelated pages.

## Responsive Design

The interface shall function appropriately across supported screen sizes and devices.

Layouts shall adapt to:

* Desktop displays
* Laptop displays
* Tablets
* Mobile devices

Navigation, logos, typography, tables, records, and other interface elements shall remain usable at smaller screen sizes.

## Accessibility

The visual and navigational system shall support accessible use.

The interface should provide:

* Adequate text readability
* Logical heading hierarchy
* Keyboard-accessible navigation
* Meaningful link labels
* Appropriate alternative text for meaningful images
* Sufficient visual distinction between interface elements
* Consistent navigation behavior

Accessibility requirements shall be incorporated into reusable interface components rather than treated as an afterthought.

## Reusable Components

Common visual and navigational elements should be implemented as reusable components wherever technically appropriate.

Examples include:

* Header
* Logo
* Navigation menu
* Footer
* Breadcrumbs
* Search interface
* Entity navigation
* Related-record links
* Alerts
* Buttons
* Cards
* Tables
* Filters

Changes to a shared component should propagate consistently throughout the interfaces that use that component.

## Separation of Presentation and Data

The site's visual layout and navigation shall remain separate from the underlying APIG data architecture.

The presentation layer shall obtain and display structured information rather than embedding important information solely within visual layouts or static page designs.

Changes to branding or layout should not require unnecessary changes to the underlying data model.

## Asset Management

Logos, brand files, icons, design resources, reusable interface resources, and other presentation assets shall be tracked through the APIG Asset Tracking and Management system defined by APIG-34.

Each significant externally hosted or operational presentation asset should have an identifiable asset record when its location, ownership, dependency, or configuration is relevant to the operation of APIG.

## Navigation and System Growth

The navigation architecture shall be designed to accommodate expansion of APIG.

The system must be capable of adding:

* New jurisdictions
* New entity types
* New investigative areas
* New services
* New tools
* New public-facing sections

without requiring a fundamental redesign of the global navigation structure.

## Consistency

New pages, applications, tools, and interfaces developed for APIG should follow this specification unless an intentional exception is documented.

Exceptions should have a defined purpose and should not create unnecessary fragmentation of the APIG user experience.

## Governance

The APIG visual identity, site layout, and navigation structure shall be treated as governed components of the APIG system.

Significant changes to the global layout, branding, navigation architecture, or reusable interface system should be documented and reconciled with related APIG specifications before implementation.
