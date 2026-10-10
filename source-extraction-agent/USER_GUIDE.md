# User Guide — prompts, agents, memory and handoffs

Start every session by asking: “Read source-extraction-agent/README.md, AGENTS.md, EXTRACTION_RULES.md, EXTRACTION_AGENT_SPEC.md, USER_GUIDE.md, TARGET_PROJECT_STATE.md, project-control/NEXT_ACTION.md, VERIFICATION_STATE.md and project-control/WORKLOG.md. Inspect existing project-control, plans, sessions, manifests and raw evidence. Recover the actual checkpoint; do not repeat completed work or delete history.”

## Stage prompts
1. Recover branch/HEAD and classify completed, pending, blocked and awaiting-evidence.
2. Pin upstream commit/root tree and inspect licensing/provenance.
3. Map architecture and inventory every capability, including business logic, UI, data, tests and runtime.
4. Perform dependency closure plus an independent second pass; reconcile all candidates.
5. Present gate evidence; do not copy until controller authorization.
6. Copy byte-for-byte only after PASS; preserve Git object identity, modes and symlinks.
7. Run the real verifier and record exact command, exit code, raw output and artifacts.
8. Append worklog, update next action/verification/continuity and hand off.

Roles: investigator, exact-copy implementer, independent verifier/reconciler, controller. Keep these as separate passes if only one agent is available; the controller alone declares PASS.

Durable memory is Git plus raw evidence, not chat memory. TARGET_PROJECT_STATE stores repo facts; WORKLOG is append-only history; NEXT_ACTION is the immediate task; VERIFICATION_STATE records actual checks; CHAT_CONTINUITY helps resume. Preserve completed docs and mark them completed/superseded rather than deleting. Never store secrets.

Continue safe independent work while CI runs if requested, but never fabricate evidence, skip extraction gates, modify pinned source, or merge/deploy without authorization.
