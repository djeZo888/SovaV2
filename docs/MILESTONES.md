# SovaV2 milestones

Status: planning branch `plan` established; the [initial entity proposal](planning/ENTITIES.md) is published for discussion. Detailed M1–M5 planning remains incomplete; implementation has not begun.

The delivery order is detailed planning, independently working components, inter-module integration, and complete-system qualification. Completion depends on the stated behavior and evidence, not the quantity of code or passing fixtures. No dates or execution timeboxes are imposed by this list.

## Initialization

| ID | Milestone | Completion gate |
| --- | --- | --- |
| M0 | Project readiness | Review V2 and V1 inputs; verify orchestrator and three workers with actual delegated tasks and repository read/write checks; inspect available test targets; record access or policy gaps privately. Establish a clean public repository and keep access profiles and operational evidence outside Git. |

## Detailed planning

M1–M5 are pure planning: design documents and GitHub planning records. M5 defines the future tests and execution system; it does not implement a runner. Work is integrated into `plan` without waiting for user PR review. The first deliverable is the entity list and basic connection map, before the complete plan is expanded.

| ID | Milestone | Completion gate |
| --- | --- | --- |
| M1 | Requirements and release scope | Agree first-release user workflows and measurable acceptance; preserve single-user, single-instance headless Linux operation and administrator-managed open-source models. Decide required modalities, tools and supported context targets; identify deferred extensions. |
| M2 | Component architecture, ownership and reuse | Define every logical component, dependencies, state/resource ownership and execution flows. Choose the smallest process arrangement that meets the requirements. Select a Codex upstream baseline and upgrade/compatibility boundary. Review V1 reuse and first-party, runtime and model licensing before importing source or assets. |
| M3 | Configuration and model management | Define versioned schemas, defaults, precedence, validation, effective configuration, migrations and rollback. Cover administrator-defined model/runtime identities, capabilities, limits, resource placement and automatic routing; distinguish reload from restart and reference protected secrets without embedding them. |
| M4 | Communication, persistence and tool contracts | Define versioned requests, events, identifiers, errors, authentication, authorization and artifact access. Specify idempotency, durable run states, reconnect cursors, restart reconciliation, deadlines, retries, cancellation and confirmed settlement. Separate native turn termination from user task fulfillment. |
| M5 | Test catalogue and development workflow | Map each requirement to unit/contract, direct-component, real-model, integration and full-workflow checks. Define reproducible runners, fixtures, expected results, evidence levels, failure cases, resource bounds and cleanup. Establish worker ownership and submission/review rules without exposing infrastructure. |

Complete M1–M5 before rebuild execution. Planning must explain how every component can be tested directly and how the components fit together. Publication of a proposal is distinct from acceptance of its design; implementation requires the next project instruction.

## Individual component implementation and testing

| ID | Milestone | Completion gate |
| --- | --- | --- |
| M6 | Platform components | Implement and directly test configuration, model registry/service interfaces, history and artifact storage, lifecycle controls, health observation and resource accounting. Waiting operations hold no shared mutation lock; observation remains independent. |
| M7 | Agent and run components | Implement and directly test the Codex adapter, local text-model connection, routing/admission, durable run ownership and agreed shell/file/research tools. Qualify compatible provider protocols, complete answers/tool results, child requests, cancellation and failures. |
| M8 | Memory and chat components | Implement and directly test original-history retention/retrieval, compaction, continuation, clean chat presentation and reconnect. Cover manual, genuine automatic and repeated compaction, exact technical recall, source retrieval and cold resume within the selected model's qualified limits. |
| M9 | Specialist components | Implement and directly test the agreed recognition/document parsing and image generation/editing capabilities, plus any modalities accepted at M1. Require real inputs and saved outputs. Startup, health and recovery of each capability work independently. |

Each component passes its own meaningful direct gate before integration. Model-dependent behavior requires evidence from the selected compatible model/runtime, in addition to deterministic checks. Logical components need not be separate services.

## Inter-module implementation and testing

| ID | Milestone | Completion gate |
| --- | --- | --- |
| M10 | Incremental integration | Integrate reviewed components through the agreed contracts. Verify complete text/tool flows first, then specialist routing, history/artifacts and memory; exercise failure, cancellation, reconnect and restart at each relevant boundary. Keep the minimal real chat/tool workflow passing as modules are added. |

## Full-system implementation and testing

| ID | Milestone | Completion gate |
| --- | --- | --- |
| M11 | Complete-system acceptance | Assemble and run SovaV2 on a single headless Linux user instance with an explicitly configured local model profile. Pass ordinary answer/research, files, recognition, generation/editing, follow-up, disconnect/reconnect, client sleep/reconnect, cancellation, service failure and restart workflows for the agreed release scope. Measure supported context, memory, capacity and overlapping workloads; verify actual outputs and resource settlement. |
| M12 | Release and operation qualification | Qualify installation, configuration, start/stop, upgrade, backup/restore and rollback under the ordinary Linux user. Review dependency/model licensing and provenance, publish concise operating documentation, and deliver a readiness record with remaining limits explicit. |

## Evidence and scope rules

- Distinguish source, hosted CI, direct component, real model and complete workflow evidence. Keep PASS, FAIL, PARTIAL, UNKNOWN and NOT_TESTED outcomes explicit; preserve original failures.
- A final event, launch receipt, idle resource inventory or fixture result does not establish completed product behavior.
- Administrator model choice is configurable; compatibility and capability limits are validated and measured. Historical V1 models, context sizes and deployment allocations do not become V2 defaults automatically.
- Keep one authoritative current plan and a small task ledger. The orchestrator owns interfaces, review and serial integration; workers own isolated, clearly assigned tasks. This development arrangement is separate from SovaV2's single-instance deployment requirement.
- Keep credentials, personal information, private data, access profiles, host addresses and specific deployment hardware out of Git. Repository examples use generic placeholders.

The milestone order follows the requested approach. The refinement is continuous verification of the smallest real workflow during integration, so later additions cannot conceal ordinary product regressions.
