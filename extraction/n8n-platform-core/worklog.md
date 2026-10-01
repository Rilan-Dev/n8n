# Extraction Worklog

## 2026-10-01 — Mechanical inventory checkpoint

### Completed

- Pinned the extraction to commit `31b6649d783ded919757ccd64259ea8a891c0955`.
- Independently verified the commit root tree as `e8d7c3aaa9d88e32d40876194f8cd9c6d69b6b0a`.
- Enumerated the complete recursive Git tree: 36,795 entries / 29,873 blobs / 6,922 trees.
- Counted 97 `package.json` files.
- Confirmed workspace configuration uses `packages/*`, `packages/@n8n/*`, `packages/frontend/**`, `packages/modules/**`, `packages/extensions/**`, and `packages/testing/**`.
- Confirmed catalog-based dependency resolution is part of the pinned workspace model.
- Verified the key AI/agent, workflow-builder, MCP browser, computer-use and Python task-runner package manifests against the pinned commit.
- Created this additive extraction branch from the pinned commit.

### Important findings

- `@n8n/agents` exposes agent SDK, catalog, sandbox and vector-store entry points and contains a broad multi-provider AI SDK dependency surface.
- `@n8n/ai-workflow-builder` contains agent/workflow construction and evaluation tooling and is licensed as `LicenseRef-n8n-sustainable-use`.
- `@n8n/mcp-browser` is a first-party MCP/browser subsystem with Playwright/agent-browser/WebDriver-related runtime dependencies.
- `@n8n/computer-use` is a separate local gateway with filesystem/shell/screenshot/input/browser capabilities and depends on the MCP browser subsystem.
- `@n8n/task-runner-python` is a first-party Python runtime requiring Python >=3.13 with a separately managed Python dependency graph.
- The root workspace catalog explicitly includes many AI providers, MCP packages, vector stores, telemetry and browser dependencies.

### Not completed

- Full first-party package dependency graph.
- Source import graph and second-order dependency closure.
- Complete capability-to-source map.
- Complete legal/restricted-source scan.
- Blob-by-blob extraction manifest.
- Immutable-source verifier.
- Capability closure verifier.
- Final COPY_TO_ANY_PROJECT guide.

### Next work

Build reproducible machine-readable repository/package/source indexes from the pinned Git tree, then resolve first-party dependency closure and external dependency inventory. Do not copy or modify source until those indexes identify the exact closure.
