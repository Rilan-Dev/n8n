# n8n Platform Core Extraction

## Source of truth

- Repository: Rilan-Dev/n8n
- Pinned commit: 31b6649d783ded919757ccd64259ea8a891c0955
- Pinned root tree: e8d7c3aaa9d88e32d40876194f8cd9c6d69b6b0a
- Source branch for this extraction: extraction/n8n-platform-core
- Upstream source remains immutable; extraction metadata is additive only.

## Current phase

Phase 0/1 mechanical inventory is established. The complete Git tree has been enumerated from the pinned commit and package/workspace metadata has been inspected.

## Inventory snapshot

- Git tree entries: 36,795
- Blob entries: 29,873
- Tree entries: 6,922
- package.json files: 97
- Implementation/config-like files (selected extensions): 27,858

These counts are inventory measurements at the pinned commit, not extraction PASS criteria.

## Major platform surfaces identified

AI/agent runtime, multi-provider model adapters, AI workflow builder, tools/tool registry, memory/vector stores, RAG/knowledge, MCP and MCP Apps, browser automation, computer use/local gateway, workflow SDK/engine, task runners including native Python, chat hub, CRDT collaboration, credentials/integrations/nodes, persistence/blob storage, telemetry/tracing, evaluation/testing, frontend/editor surfaces, extensions, scheduling and queue execution.

## Rules

1. Never alter source files for extraction convenience.
2. Do not duplicate source into capability directories.
3. Capability manifests must point to exact source paths.
4. External packages are inventory-only unless first-party source is actually present.
5. Restricted/EE source must be explicitly classified and legally reviewed.
6. Extraction is not VERIFIED until Git identity, byte integrity, dependency closure, capability closure, legal classification and machine verification all pass.
