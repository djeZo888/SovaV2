# SovaV2

SovaV2 is the successor to [Sova V1](https://github.com/djeZo888/mixed-memory-llm-api-server), a locally hosted agentic system for technical research and engineering work.

**Status: planning.** V1 ended before delivering the requested complete system. V2 will start from a reviewed architecture, clear configuration and communication contracts, and executable tests for small independently working components. Reuse is assessed component by component.

## Design inputs

- [V1 closeout review](https://github.com/djeZo888/mixed-memory-llm-api-server/pull/12), pending user approval.
- [User vision](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/a1c5395046413a1876803e1df423e82d0388074e/docs/VISION.md).
- [Candid V1 postmortem](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/a1c5395046413a1876803e1df423e82d0388074e/docs/POSTMORTEM.md).
- [Reuse inventory](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/a1c5395046413a1876803e1df423e82d0388074e/docs/REUSE-INVENTORY.md), [V2 design input](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/a1c5395046413a1876803e1df423e82d0388074e/docs/V2-DESIGN-INPUT.md) and [backlog](https://github.com/djeZo888/mixed-memory-llm-api-server/blob/a1c5395046413a1876803e1df423e82d0388074e/TODO.md).
- [CodexTandem](https://github.com/djeZo888/CodexTandem): development coordination across an orchestrator and separate physical workers.

## Foundation work

1. Draw the current architecture and execution flows, with clear state and component ownership.
2. Define configuration files, schemas, precedence, validation and update behavior.
3. Define versioned communication protocols and their failure, reconnect and cancellation behavior.
4. Catalogue tests, implement them and provide a reproducible execution system.

The first useful release targets one user and a clean chat interface. Sova selects models and tools automatically. Durable server-owned work, reliable context compaction and independent specialist services must pass ordinary user workflows, including follow-ups and reconnects. Required model instances must support concurrent operation within measured capacity.

The architecture and implementation plan require user review before rebuild execution. These inputs preserve lessons and requirements; historical V1 test results do not establish V2 acceptance.
