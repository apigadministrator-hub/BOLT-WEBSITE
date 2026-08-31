# APIG-21 — Task Execution and Workflow Specification

## Status

Active

## Purpose

This specification defines how APIG receives, interprets, authorizes, prioritizes, assigns, executes, verifies, records, and completes tasks.

The fundamental principle is:

REQUEST
→ IDENTIFY REQUESTER
→ DETERMINE AUTHORITY
→ CLASSIFY TASK
→ DETERMINE PRIORITY
→ IDENTIFY RESOURCES
→ ASSIGN AI
→ EXECUTE
→ VERIFY
→ RECORD
→ COMPLETE.

---

# 1. Core Principle

Every task must be evaluated according to:

- Who requested it
- Whether the requester is authorized
- What the requester is asking
- What authority applies
- What priority applies
- What resources are required
- What existing functions must be protected
- What AI or other system should perform the work
- What verification is required
- What must be recorded.

---

# 2. Task

A task is a discrete action requested, authorized, scheduled, or required within APIG.

---

# 3. Task Request

A task request is an instruction proposing or requiring execution of a task.

---

# 4. Requester

Every task should identify its requester where possible.

---

# 5. Requester Identity

APIG must distinguish an authorized principal, contributor, system actor, and member of the public.

---

# 6. Public Request

A message from the general public does not automatically possess operational authority.

---

# 7. Contributor Request

A contributor may have defined authority according to their assigned role.

---

# 8. Principal Authority

The designated APIG principal may issue instructions having authority over system operations according to the applicable APIG authority structure.

---

# 9. Identity Verification

High-impact instructions should require appropriate requester verification.

---

# 10. Impersonation Protection

APIG must not treat an unverified person as an authorized principal merely because the person claims to be one.

---

# 11. Message Interpretation

A message must be interpreted according to its actual content and the identity and authority of its sender.

---

# 12. Natural Language

Task requests may be expressed in ordinary language.

---

# 13. Intent Extraction

AI may extract the intended task from natural-language instructions.

---

# 14. Intent Uncertainty

If the intended task is materially ambiguous, the AI should not invent missing authority, objectives, or constraints.

---

# 15. Task Classification

Tasks should be classified according to their function.

Examples include:

- Research
- Analysis
- Communication
- Data processing
- Content creation
- Website operation
- Maintenance
- Monitoring
- Administration
- Development
- Resource management
- Security
- Review
- Verification.

---

# 16. Task Scope

The task should define what the AI is expected to accomplish.

---

# 17. Task Boundaries

The AI should not expand the task beyond its authorized scope without appropriate authority.

---

# 18. Required Resources

The system should determine what resources are required before execution.

---

# 19. Resource Types

Resources may include:

- AI computation
- Human attention
- Software
- APIs
- Storage
- Network access
- Financial resources
- Time
- External services
- Data.

---

# 20. Resource Protection

Core operational functions must be protected from nonessential tasks.

---

# 21. Priority

Tasks should receive a priority classification.

Possible classifications include:

- Emergency
- Priority
- Normal
- Deferred
- Background.

---

# 22. Explicit Priority

When an authorized requester explicitly establishes priority, the system should recognize that priority.

---

# 23. Priority Keyword

If APIG establishes a specific keyword or command indicating priority, that keyword should be documented in the applicable operational specification.

---

# 24. Priority Override

An authorized priority instruction may cause available resources to be redirected toward the priority task.

---

# 25. Core Function Protection

Priority does not authorize interruption of essential functions when doing so would materially impair the operation or security of the APIG system.

---

# 26. Resource Allocation

After protecting required core functions, remaining available resources should be allocated according to task priority.

---

# 27. Resource Exhaustion

If available resources are insufficient, APIG should determine whether to:

- Queue the task
- Reduce task scope
- Assign another resource
- Use another AI
- Defer the task
- Request additional authorization.

---

# 28. Priority Queue

Tasks may be maintained in a priority queue.

---

# 29. Queue Ordering

Queue ordering should account for:

- Priority
- Required deadlines
- Resource requirements
- Dependencies
- Safety
- Core-function protection.

---

# 30. Priority Does Not Mean Unlimited Resources

A priority task receives preferential resource allocation only within the limits of available and authorized resources.

---

# 31. Concurrent Tasks

Multiple tasks may execute concurrently when resources permit.

---

# 32. Task Isolation

One task should not unintentionally alter another task's data, state, or resources.

---

# 33. Task Dependencies

A task may depend on completion of another task.

---

# 34. Dependency Graph

Dependencies should be represented where material.

---

# 35. Blocked Task

A task is blocked when required conditions or resources are unavailable.

---

# 36. Failed Task

A task has failed when execution did not achieve its required objective.

---

# 37. Partial Completion

A task may be partially completed.

The completed portion and remaining portion should be recorded.

---

# 38. Completed Task

A task is complete when its defined objective has been achieved or the authorized requester accepts the resulting output.

---

# 39. Cancelled Task

A task may be cancelled by an authorized actor or according to applicable system rules.

---

# 40. Abandoned Task

A task may be abandoned when continued execution is no longer justified.

The reason should be recorded where material.

---

# 41. Task State

Task states may include:

- Received
- Awaiting authorization
- Authorized
- Queued
- Assigned
- Running
- Blocked
- Paused
- Partially complete
- Completed
- Failed
- Cancelled
- Abandoned.

---

# 42. Assignment

Every executable task should identify the responsible AI, human, system, or combination where practical.

---

# 43. AI Assignment

APIG may assign different AI models according to:

- Capability
- Cost
- Availability
- Speed
- Reliability
- Task requirements.

---

# 44. Free AI Resources

Where APIG intentionally uses free or otherwise low-cost AI resources, those resources may be assigned to appropriate tasks without assuming permanent availability.

---

# 45. AI Substitution

If one AI becomes unavailable, another authorized AI may assume the task where technically and operationally appropriate.

---

# 46. AI Handoff

A task transferred between AI systems should preserve relevant:

- Task definition
- Authority
- Priority
- Inputs
- Outputs
- Sources
- Current state
- Outstanding work
- Constraints.

---

# 47. Provider Independence

The task model must not depend on one specific AI provider.

---

# 48. AI Failure

If an AI fails, APIG should preserve the task state and allow recovery or reassignment where practical.

---

# 49. AI Capability Matching

Tasks should be assigned to systems capable of safely performing them.

---

# 50. AI Restrictions

An AI must not perform actions outside its authorized capabilities.

---

# 51. Tool Authorization

Access to external tools should be limited according to task authority and system permissions.

---

# 52. External Websites

When a task requires interaction with an external website, the AI should identify the required destination and applicable permissions.

---

# 53. External Account Actions

Actions affecting external accounts require appropriate authorization.

---

# 54. External Communication

Messages sent to third parties should require appropriate authority.

---

# 55. Public Communication

Public-facing communications should follow applicable APIG communication rules.

---

# 56. Private Communication

Private communications should follow applicable privacy and authorization rules.

---

# 57. Destructive Actions

Actions that could delete, overwrite, disable, or materially alter information or systems require appropriate authorization.

---

# 58. Irreversible Actions

Irreversible actions require heightened confirmation and authorization where practical.

---

# 59. High-Impact Actions

Actions capable of materially affecting people, organizations, finances, legal status, reputation, or system security require heightened controls.

---

# 60. Confirmation

Where required, the AI should obtain confirmation before executing a high-impact action.

---

# 61. No Unauthorized Expansion

An AI must not convert a task into a broader mission merely because the broader mission appears useful.

---

# 62. Necessary Subtasks

Reasonably necessary subtasks may be performed when they are within the authority and scope of the original task.

---

# 63. Subtask Recording

Material subtasks should remain traceable to the parent task.

---

# 64. Parent Task

A complex task may contain multiple subtasks.

---

# 65. Subtask Dependency

Subtasks may depend on one another.

---

# 66. Task Hierarchy

APIG may represent:

PROJECT
→ TASK
→ SUBTASK
→ ACTION.

---

# 67. Action

An action is an individual operation performed in pursuit of a task.

---

# 68. Action Authorization

Each material action must be covered by the task's authority or separately authorized.

---

# 69. Task Inputs

Task inputs should be identified where practical.

---

# 70. Task Outputs

Task outputs should be identified where practical.

---

# 71. Input Integrity

Important inputs should retain their source and provenance.

---

# 72. Output Integrity

Material outputs should retain their relationship to the task that produced them.

---

# 73. Output Verification

Material outputs should be verified according to the task's requirements.

---

# 74. Verification

Verification should determine whether the task result satisfies the requested objective.

---

# 75. Human Review

Human review may be required for high-impact or uncertain outputs.

---

# 76. AI Review

A second AI may review an output when appropriate.

---

# 77. Independent Review

Where practical, review should not simply repeat the same reasoning without examining the underlying evidence.

---

# 78. Error Detection

APIG should support identification and correction of task errors.

---

# 79. Error Reporting

Material errors should be recorded.

---

# 80. Correction

Corrections should preserve sufficient history to determine what changed.

---

# 81. Task History

Material task activity should remain historically traceable.

---

# 82. Audit Record

Material actions should generate appropriate audit records.

---

# 83. Audit Attribution

Audit records should identify the responsible actor or system where practical.

---

# 84. Timestamp

Material task actions should record time where practical.

---

# 85. Task Provenance

Task outputs should remain linked to their inputs and sources.

---

# 86. Source Preservation

Tasks should not destroy source provenance while transforming information.

---

# 87. Documentation

Material tasks should produce sufficient documentation to allow later reconstruction.

---

# 88. External Code Documentation

When a task causes code to be entered into an external system, APIG should preserve documentation identifying:

- What code was used
- Where it was entered
- Why it was used
- When it was used
- What version was used
- Relevant configuration
- Known dependencies.

---

# 89. Exact External Code

Where practical, the exact code copied into an external system should be preserved separately from explanatory documentation.

---

# 90. External Configuration

Changes to external configurations should be recorded where material.

---

# 91. Rollback

Where practical, material system changes should have a rollback or recovery method.

---

# 92. Recovery

If an operation fails, APIG should attempt recovery according to applicable system rules.

---

# 93. Failure Isolation

Failure of one task should not unnecessarily disable unrelated core functions.

---

# 94. Emergency Tasks

Emergency tasks may receive immediate resource allocation according to APIG emergency rules.

---

# 95. Emergency Override

Emergency handling must still preserve essential security and operational safeguards.

---

# 96. Background Tasks

Background tasks should yield resources when higher-priority tasks require them.

---

# 97. Scheduled Tasks

Scheduled tasks should execute according to their defined schedule unless superseded by authorized priority or operational constraints.

---

# 98. Recurring Tasks

Recurring tasks should retain their defined schedule and execution history.

---

# 99. Conditional Tasks

Conditional tasks should execute only when their defined conditions are satisfied.

---

# 100. Monitoring Tasks

Monitoring tasks may remain active while other tasks execute.

---

# 101. Resource Monitoring

APIG should monitor relevant resource availability where practical.

---

# 102. Resource Reservation

Critical resources may be reserved for essential functions.

---

# 103. Resource Reallocation

Available nonessential resources may be reallocated according to priority.

---

# 104. Core Mission

The APIG core mission takes precedence over nonessential tasks.

---

# 105. Priority Interpretation

A valid priority instruction means:

PROTECT CORE FUNCTIONS
→ USE AVAILABLE REMAINING RESOURCES
→ EXECUTE PRIORITY TASK
→ DO NOT UNNECESSARILY WAIT FOR LOWER-PRIORITY WORK.

---

# 106. Lower-Priority Work

Lower-priority tasks may be delayed when required to satisfy a higher-priority authorized task.

---

# 107. Queue Transparency

Where appropriate, task status should indicate why a task is delayed.

---

# 108. Task Ownership

Each task should have an identifiable owner or responsible execution system where practical.

---

# 109. Responsibility

Responsibility for completing a task should not be confused with authority to authorize the task.

---

# 110. Requester vs Executor

The requester and executor may be different entities.

---

# 111. Approver vs Executor

The person or system approving a task may be different from the person or system executing it.

---

# 112. Separation of Duties

High-impact operations may require separation between authorization, execution, and verification.

---

# 113. Authorization Chain

Where applicable:

REQUESTER
→ AUTHORIZER
→ EXECUTOR
→ REVIEWER.

---

# 114. Authority Verification

The system should determine whether the requester has authority for the requested action.

---

# 115. Scope Verification

The system should determine whether the requested action falls within the requester's authority.

---

# 116. Conflicting Instructions

Conflicting instructions should be resolved according to authority, priority, time, and applicable APIG rules.

---

# 117. Higher Authority

A valid instruction from a higher authority may supersede a conflicting lower-authority instruction, subject to system safeguards and applicable rules.

---

# 118. Unauthorized Override

A requester cannot create authority merely by declaring that their request has priority.

---

# 119. Public Messages

Public messages may provide useful information without creating operational authority.

---

# 120. Public Requests for Action

A public request must be evaluated before execution.

---

# 121. Contributor Instructions

Contributor instructions should be evaluated according to contributor permissions.

---

# 122. Principal Instructions

Principal instructions should be recognized according to the APIG authority model.

---

# 123. Identity Before Priority

Priority should not be applied until the authority of the requester has been appropriately established when identity is material.

---

# 124. Priority Before Execution

Priority should be determined before allocating discretionary resources.

---

# 125. Resource Allocation Before Execution

Required resource allocation should be determined before execution when practical.

---

# 126. Execution

Execution should follow the defined task scope and authorization.

---

# 127. Verification After Execution

Material task results should be verified after execution.

---

# 128. Completion Record

Completed tasks should retain:

- Request
- Requester
- Authority
- Priority
- Assigned executor
- Inputs
- Actions
- Outputs
- Verification
- Completion status
- Relevant sources.

---

# 129. Failed Completion

A task should not be marked completed merely because the AI stopped working.

---

# 130. Partial Completion Record

Partial results should be clearly identified.

---

# 131. User Notification

Where appropriate, the requester should be informed of completion, failure, delay, or required action.

---

# 132. No False Completion

An AI must not claim to have completed an action it did not actually perform.

---

# 133. No False Verification

An AI must not claim that an output was verified when it was not.

---

# 134. No False Tool Use

An AI must not claim to have accessed an external system, website, file, or resource unless it actually did so.

---

# 135. No Invented Results

An AI must not fabricate task results.

---

# 136. Uncertainty

If execution or verification is uncertain, the task record should preserve that uncertainty.

---

# 137. Escalation

Tasks should be escalated when:

- Authority is uncertain
- Identity is uncertain
- Required resources are unavailable
- The task exceeds authorized scope
- Evidence is insufficient
- A high-impact decision requires review
- Conflicting instructions cannot be resolved.

---

# 138. Escalation Target

Escalation should be directed to the appropriate authority or reviewer.

---

# 139. Escalation Record

Material escalations should be recorded.

---

# 140. Human Intervention

The system should allow human intervention when AI execution cannot safely or reliably continue.

---

# 141. AI-to-AI Handoff

AI systems may transfer tasks to another AI when authorized.

---

# 142. Handoff Completeness

A handoff should include enough context for the receiving AI to continue without unnecessarily reconstructing the entire task.

---

# 143. Handoff Provenance

The receiving AI must be able to identify the origin of important information.

---

# 144. Handoff Authority

The receiving AI must be able to determine the authority under which it is continuing the task.

---

# 145. Handoff Priority

The receiving AI must preserve the task's applicable priority.

---

# 146. Handoff State

The receiving AI must know what has already been completed and what remains.

---

# 147. Provider Migration

A task must remain portable across AI providers.

---

# 148. Provider Failure

The failure or removal of one AI provider must not destroy APIG's task history.

---

# 149. Resource Folder Integration

Task execution should use the APIG resource hierarchy to locate applicable specifications, procedures, documentation, and other resources.

---

# 150. Start Here

The root APIG resource document should identify where an AI should begin when entering the resource hierarchy.

---

# 151. Specification Discovery

An AI should use the root resource document to determine which specifications are relevant to the task.

---

# 152. Task-Specific Resources

An AI should read only the resources necessary to understand and safely execute the task when the task does not require the entire APIG framework.

---

# 153. Full Framework Review

An AI should review additional specifications when the task involves authority, governance, resource management, security, accountability, data structure, or other areas requiring broader context.

---

# 154. Resource Independence

Task execution must not depend on the continued availability of a particular AI conversation.

---

# 155. External Resource Storage

Important operational documentation should be stored in persistent resources accessible to authorized replacement AI systems.

---

# 156. Portable Documentation

Documentation should use portable formats where practical.

---

# 157. Markdown

Markdown files may be used for specifications, instructions, procedures, and other machine-readable documentation.

---

# 158. PDF Resources

PDFs may be used for finalized reference documents, archival materials, formal records, or human-readable documentation.

---

# 159. Exact Operational Records

Where exact reproduction matters, the underlying text or structured data should be preserved rather than relying exclusively on PDF conversion.

---

# 160. Resource Versioning

Material changes to task instructions or procedures should be versioned.

---

# 161. Current Procedure

The currently active procedure should be distinguishable from historical procedures.

---

# 162. Draft Procedure

Draft procedures must not be treated as active procedures unless authorized.

---

# 163. Task Templates

Recurring tasks may use standardized templates.

---

# 164. Template Versioning

Task templates should be versioned when material.

---

# 165. Task Automation

Tasks may be automated where the automation remains within authorized scope.

---

# 166. Automation Limits

Automation should not silently expand the authority of the system.

---

# 167. Automated Actions

Automated actions should remain attributable to the system performing them.

---

# 168. Scheduled Automation

Scheduled automated tasks should retain their schedule and authorization source.

---

# 169. Conditional Automation

Conditional automation should retain the condition that caused execution.

---

# 170. Monitoring Automation

Automated monitoring should record relevant alerts and material actions.

---

# 171. Auditability

The system should make material task execution reconstructable.

---

# 172. Accountability

Task records should make it possible to determine:

- Who requested the task
- Who authorized it
- Who executed it
- What system was used
- What resources were used
- What occurred
- What result was produced.

---

# 173. Resource Accountability

Material resource use should be attributable where practical.

---

# 174. AI Accountability

An AI system is accountable for following its assigned task and applicable system rules, but responsibility for authorization remains with the appropriate human or governing authority.

---

# 175. Human Authority

AI execution does not replace the authority of the human or organization that authorized the task.

---

# 176. No Authority by Execution

An AI does not gain additional authority merely because it successfully performed a previous task.

---

# 177. No Authority by Capability

An AI's technical capability does not itself establish authorization.

---

# 178. No Authority by Access

Having access to a system does not automatically authorize every action available through that access.

---

# 179. Least Necessary Access

AI systems should receive only the access reasonably necessary for their assigned functions where practical.

---

# 180. Security

Task execution must follow applicable security requirements.

---

# 181. Privacy

Task execution must follow applicable privacy requirements.

---

# 182. Legal Compliance

Task execution must follow applicable law and governing requirements.

---

# 183. Organizational Compliance

Task execution must follow applicable organizational policies and procedures.

---

# 184. Conflict Resolution

Where task instructions conflict with higher-level legal, security, or system requirements, the higher requirement controls.

---

# 185. Unsafe Task

An unsafe task should not be executed merely because it was requested.

---

# 186. Unauthorized Task

An unauthorized task should not be executed merely because it appears beneficial.

---

# 187. Impossible Task

An impossible task should not be represented as completed.

---

# 188. Unsupported Task

A task requiring capabilities unavailable to the assigned system should be reassigned, escalated, or deferred.

---

# 189. Task Cancellation

Cancellation should preserve sufficient history to explain what happened.

---

# 190. Task Resumption

Paused or interrupted tasks should resume from their recorded state where practical.

---

# 191. Checkpointing

Long-running tasks should use checkpoints where practical.

---

# 192. Recovery Checkpoints

Checkpoints should preserve enough information to continue after interruption.

---

# 193. Work Product

Material task outputs should be stored in an appropriate persistent location.

---

# 194. Work Product Provenance

Work products should identify the task and sources from which they originated where practical.

---

# 195. Final Review

Before declaring a consequential task complete, the system should confirm:

- Correct task
- Correct authority
- Correct scope
- Correct resources
- Correct execution
- Correct output
- Required verification
- Required documentation.

---

# 196. Completion Sequence

REQUEST
→ IDENTITY
→ AUTHORITY
→ PRIORITY
→ RESOURCES
→ ASSIGNMENT
→ EXECUTION
→ VERIFICATION
→ DOCUMENTATION
→ COMPLETION.

---

# 197. Priority Execution Sequence

AUTHORIZED PRIORITY REQUEST
→ PROTECT CORE FUNCTIONS
→ IDENTIFY AVAILABLE RESOURCES
→ PAUSE / DELAY LOWER PRIORITY WORK IF NECESSARY
→ ALLOCATE AVAILABLE RESOURCES
→ EXECUTE
→ VERIFY
→ RECORD.

---

# 198. AI Replacement Sequence

TASK STATE
→ AUTHORITY
→ PRIORITY
→ INPUTS
→ SOURCES
→ COMPLETED WORK
→ REMAINING WORK
→ NEW AI
→ REVIEW REQUIRED RESOURCES
→ CONTINUE.

---

# 199. Core Principles

1. Every task must have an identifiable request or authority.
2. Requester identity matters.
3. Public messages do not automatically create operational authority.
4. Contributor authority depends on defined permissions.
5. Principal authority must be recognized according to the APIG authority model.
6. Priority does not override identity verification.
7. Priority does not override core-function protection.
8. Available resources should be used according to authorized priority.
9. Lower-priority work may be delayed for higher-priority authorized work.
10. An AI may not expand its authority merely because a task appears useful.
11. Capability does not equal authority.
12. Access does not equal authorization.
13. Every material task should remain traceable.
14. AI-to-AI handoffs must preserve authority, priority, provenance, and task state.
15. AI-provider changes must not destroy task history.
16. Material outputs should be verified.
17. An AI must never claim work it did not perform.
18. An AI must never claim verification it did not perform.
19. An AI must never fabricate results.
20. High-impact actions require heightened controls.
21. Destructive or irreversible actions require appropriate authorization.
22. Core APIG functions take precedence over nonessential work.
23. Resource allocation must protect essential system functions.
24. Task state must survive interruption where practical.
25. Material task history must remain auditable.
26. Operational documentation must remain portable.
27. The resource hierarchy must allow replacement AI systems to locate applicable instructions.
28. Task execution must remain independent of any single AI provider.
29. Authorization, execution, and verification should be separated when appropriate.
30. The task system must preserve enough information for another authorized AI to continue the work.

---

# 200. Change Control

This document may be modified as APIG develops.

Substantive changes should:

- Update the version.
- Record the change.
- Preserve previous versions where practical.
- Update the root resource document if the resource location changes.
- Identify specifications that require corresponding changes.

---

# END OF APIG-21