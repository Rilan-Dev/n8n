# Risks — n8n Extraction

- Accidentally restarting completed work because the current chat lacks its checkpoint.
- Treating an uninspected default branch as the intended source.
- Overwriting existing extraction artifacts or conflating source and target roles.
- Mitigation: recover Git history and project-control first; preserve existing files; pin source identity before inventory.
