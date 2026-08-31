
# APIG-34 — Asset Tracking and Management Specification

## Purpose

APIG shall maintain a centralized, machine-readable system for tracking and managing the operational assets used by the APIG project.

The system must allow an authorized human or AI to determine what assets APIG already has, what each asset does, where it is located, how it is used, and how it connects to other assets and systems without repeatedly asking the administrator or rediscovering existing resources.

## Asset Scope

Assets include, but are not limited to:

* Accounts
* Domains
* Hosting services
* Software services
* GitHub repositories
* Google Workspace resources
* Tally forms
* Webhooks
* Google Apps Scripts
* APIs and integrations
* Websites and applications
* Payment and operating accounts
* External services
* Project-specific tools
* Other operational infrastructure

## Asset Records

Each asset shall have a persistent asset record containing, when applicable:

* Unique asset ID
* Asset name
* Asset type
* Description
* Purpose and function
* Provider or service
* Owner or controlling organization
* URL or location
* Status
* Associated project or system
* Related workflows
* Connected assets
* Dependencies
* Relevant configuration information
* Creation date
* Last verified date
* Historical notes and decisions

Asset records shall identify relationships between assets when those relationships are necessary to understand or operate the APIG system.

## Credentials and Secrets

Asset records shall never contain:

* Passwords
* API keys
* Private tokens
* Authentication secrets
* Security credentials
* Other sensitive secrets

Asset records may identify that a credential is required and identify the secure system or location where an authorized operator can obtain it.

## Asset Creation and Changes

Whenever a new operational asset is created for APIG, an asset record shall be created.

Whenever an existing asset is materially changed, its record shall be updated.

When an asset is retired, replaced, transferred, or becomes unavailable, its record shall be updated while preserving the appropriate historical information.

## AI Use

Authorized AI systems shall consult the asset inventory before recommending or creating new assets.

AI systems should:

1. Search for existing assets before creating new ones.
2. Reuse existing assets when appropriate.
3. Identify dependencies before modifying an asset.
4. Create or update asset records when authorized to create or modify assets.
5. Identify missing, conflicting, or outdated asset information.
6. Request human intervention when required authorization, credentials, or external action cannot be obtained through available systems.

## Asset Relationships

The system shall support relationships between assets.

For example:

**Tally Account → FOIA Request Builder → Webhook → Google Apps Script → Workflow**

Each component is a distinct asset, while the relationships between them are retained so an authorized AI or administrator can understand how the system operates.

## Human Authorization

Asset tracking does not grant an AI authority to create accounts, spend money, enter contracts, disclose protected information, or perform other consequential actions.

Where human authorization is required, the system shall identify the required action and obtain appropriate authorization before proceeding.

## Inventory Integrity

The asset inventory shall be treated as an operational record rather than informal documentation.

Duplicate, obsolete, conflicting, incomplete, or unverified asset records shall be identifiable and subject to reconciliation.

Significant changes to assets and their relationships shall preserve appropriate historical information.

## Separation From Secrets

The asset inventory is an infrastructure and relationship record. It is not a password manager or secrets repository.

Sensitive credentials shall remain in an appropriately secured credential-management system separate from the machine-readable asset records.

## Architectural Relationship

Asset Tracking and Management is an operational component of the APIG infrastructure.

It supports the APIG website, investigative database, AI operations, workflows, integrations, and other project systems by maintaining a persistent record of the infrastructure on which those systems depend.

The asset system shall be structured so that an authorized AI can understand the existing APIG operational environment without assuming direct access to APIG databases or relying on undocumented administrator knowledge.
