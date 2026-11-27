# Evaluation: Repository README

## Summary of Changes

- Added a root `README.md` describing the repository's purpose and intended React audience.
- Documented submodule setup, cloning, initialization, pinning, and updates.
- Added frontend-specific AI instruction examples, contribution guidance, an optional RPIE reference,
  and a license link.
- Clearly identified `frontend-architecture.md` as forthcoming and outside this cycle's deliverables.

## Automated Tests

- No application test suite applies to this documentation-only change.
- `git diff --check main...HEAD` passed.
- PowerShell acceptance checks passed for the 120-character line limit, local Markdown links,
  required setup and AI references, and the planned architecture file's expected absence.

## Manual Testing Instructions

1. Review the submodule commands and paths against the host-project root layout in the README.
2. Review the Copilot, `AGENTS.md`, and one-time prompt examples for frontend-specific scope,
   binding requirements, and handling of missing or conflicting guidance.
3. Check the README's local and external references, including the license and optional RPIE link.
4. Confirm the README does not present the planned architecture document as currently available.

### Manual Test Results

- Passed: the add command uses the selected SSH URL and root-level `react-vertical-slice/` path.
- Passed: clone, initialize, pinning, and update instructions describe the expected Git workflow.
- Passed: all three AI examples apply binding frontend standards and request approval for deviations.
- Passed: the architecture document is described as forthcoming; its future path is given as code,
  not as a broken Markdown link.
- Passed: the GPL-3.0 license link resolves locally, and the RPIE companion is linked as optional.

## Code Quality Review

- Documentation-only change; no application or source code was modified.
- Whitespace and line-length checks passed.

## Performance Review

- Not applicable. The change adds no executable code or runtime behavior.

## Security Review

- The README contains no credentials, secrets, or executable scripts.
- The Git commands operate on the explicitly documented submodule path. The SSH requirement is
  stated next to the setup command.

## Documentation and Acceptance Review

- Passed: the repository's purpose, audience, benefits, and non-package scope are clear.
- Passed: all requested setup, AI-assistant, contribution, optional RPIE, and license guidance is
  present.
- Passed: the architecture document's forthcoming status is explicit and AI usage is conditioned
  on its availability.
- `context_map.md` was absent. Its creation was authorized by the user to satisfy the RPIE
  evaluation requirement; the feature reference will be added before evaluation is finalized.

## Success Criteria

- Passed: README content meets the approved PRD and all lines are no longer than 120 characters.
- Passed: submodule examples use the expected SSH URL and `react-vertical-slice/` path.
- Passed: AI examples consistently apply the architecture to all frontend work and require approval
  for deviations.
- Passed: existing local references resolve; the forthcoming architecture document is clearly
  identified.
- Passed: documentation checks report no whitespace or formatting errors.
