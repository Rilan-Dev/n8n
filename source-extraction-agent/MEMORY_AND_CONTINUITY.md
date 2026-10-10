# Memory and continuity protocol

Authority: Git objects/raw evidence > existing project-control, plans, sessions, manifests and worklogs > this folder's state docs > chat/model memory.

At session start inspect branch, HEAD, working tree, latest worklog, current next action, source pin, prior handoff and raw verifier output. Classify completed, pending, blocked and awaiting-evidence. Do not repeat completed work merely because a new chat starts.

At session end append a dated worklog entry; update next action and verification to reality; preserve historical plans and mark them completed/superseded instead of deleting; record commands, exit codes, artifact paths, commit SHAs, limitations and assumptions; write a short resume note. Never store credentials.

If a narrative says PASS but evidence is missing, stale or for another source pin, mark current status unverified and explain the discrepancy. Correct current summaries only; preserve history.
