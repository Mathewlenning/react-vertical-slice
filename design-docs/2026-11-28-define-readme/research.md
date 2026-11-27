# Research Summary

## Scope and Intent

- This full RPIE cycle covers the repository README only.
- The repository is intended to be a lean Git submodule for React applications.
- Its planned `frontend-architecture.md` will define binding vertical-slice architecture standards.
- The architecture document is not present yet and is outside this cycle's deliverables.
- The README should position this repository as guidance, not a starter kit, component library, or package.
- Main benefits to emphasize: consistency across features, easier AI-assisted implementation, and
  maintainability.
- The standards apply to any React app and should be adopted in both new and existing apps; existing
  codebases can adopt them incrementally.

## README Requirements from Q&A

- Use a concise, action-oriented quick-start style with usage instructions and practical examples.
- Include a short plain-language vertical-slice overview; keep detailed technical standards in the
  architecture document.
- Show how to add the submodule at the host project's root as `react-vertical-slice`, alongside
  files such as `package.json` and `src/`.
- Use the SSH GitHub URL in the `git submodule add` example.
- Explain commit pinning, updating the submodule, and committing the updated submodule pointer in the
  host project.
- Explain initialization when cloning, including `--recurse-submodules` and the command for an
  already-cloned host project.
- Git is the only prerequisite. Include no application build or runtime setup.
- Include copy-pasteable, alternative examples for `.github/copilot-instructions.md` and `AGENTS.md`;
  do not recommend maintaining both by default.
- AI instructions should apply to all frontend work in the host React app, explicitly follow this
  frontend architecture, read its root-level document before planning or changing code, and treat
  it as binding. Require explicit user approval for deviations and surface conflicts or gaps.
- Include a one-time example prompt for an AI chat.
- Include brief contribution guidance and a license section linking to the existing GPL-3.0
  `LICENSE`.
- Mention the RPIE repository as an optional companion by link only, not as a prerequisite or setup
  step.

## Relevant Repository Context

- The current tracked files do not include `README.md` or `frontend-architecture.md`.
- The existing `.gitmodules` identifies the optional RPIE repository as
  `https://github.com/Mathewlenning/rpie`.
- The current root `LICENSE` is GNU GPL version 3.

## Related Documents

- `README.md` — the planned consumer-facing quick start and usage guide.
- `frontend-architecture.md` — planned root-level source of binding frontend architecture
  standards; outside this cycle's deliverables.
- `LICENSE` — existing repository license, to be linked from the README.
- `.gitmodules` — records the existing RPIE submodule source URL.
- `rpie/rpie.md` — authoritative RPIE process rules followed for this cycle.
- `.github/copilot-instructions.md` — points contributors to the authoritative RPIE rules.