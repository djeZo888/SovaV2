# SovaV2

SovaV2 is the successor to [Sova V1](https://github.com/djeZo888/mixed-memory-llm-api-server), a locally hosted agentic system for technical research and engineering work.

**Status: initialization and milestone planning. Implementation has not begun.** V1 ended before delivering the requested complete system. V2 will start from a reviewed architecture, clear configuration and communication contracts, and tests for small independently working components. Reuse is assessed component by component.

## V2 requirements

- Run from one ordinary user instance on a single headless Linux system. Additional hosts and particular accelerators are optional deployment choices.
- Use the open-source Codex engine as the agent foundation. The Sova administrator can define compatible open-source models, runtimes, capabilities and routing policy; models are not hard-coded into the product.
- Keep ordinary chat simple, with automatic model and tool selection. Operator configuration is separate from the chat experience.
- Preserve original histories and artifacts, make runs survive browser disconnects, and qualify compaction and restart recovery through real workflows.
- Make text, recognition and generation independently usable and recoverable, with shared-resource restrictions only where a real conflict exists.
- Keep personal information, credentials, access inventories, private histories and deployment-specific details outside this repository.

The ordered work and completion gates are in [Milestones](docs/MILESTONES.md). This is the current planning index; historical V1 inputs are evidence for review, not current deployment instructions.

## Design inputs

- [Final V1 documentation](https://github.com/djeZo888/mixed-memory-llm-api-server/tree/main), merged into the default branch on 4 October 2026 ([PR #12](https://github.com/djeZo888/mixed-memory-llm-api-server/pull/12)).
- [User vision](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/9481c1fda160b03d414a05c6ae741c34d2bb4dcf/docs/VISION.md).
- [Candid V1 postmortem](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/9481c1fda160b03d414a05c6ae741c34d2bb4dcf/docs/POSTMORTEM.md).
- [Reuse inventory](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/9481c1fda160b03d414a05c6ae741c34d2bb4dcf/docs/REUSE-INVENTORY.md), [V2 design input](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/9481c1fda160b03d414a05c6ae741c34d2bb4dcf/docs/V2-DESIGN-INPUT.md) and [backlog](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/9481c1fda160b03d414a05c6ae741c34d2bb4dcf/TODO.md).
- [CodexTandem](https://github.com/djeZo888/CodexTandem): development coordination across an orchestrator and separate physical workers.

Detailed planning comes first, followed by independent component implementation and tests, inter-module integration and tests, then full-system implementation and acceptance. The architecture and implementation plan require user review before rebuild execution. Historical V1 test results do not establish V2 acceptance.
