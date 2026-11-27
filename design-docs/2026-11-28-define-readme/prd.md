# Product Requirements Document: Repository README

## Description

Create a root-level `README.md` that explains how to consume this repository as a Git submodule
providing frontend architecture guidance for React applications.

## Purpose

Help developers establish consistent, maintainable vertical slices across React features and help
generative AI tools follow the same frontend architecture conventions.

## Usage

Readers use the README to add the submodule to a host project, initialize or update it, and configure
their AI coding assistant to follow the architecture standards. It serves both new and existing
React applications; existing applications may adopt the conventions incrementally.

## Build Approach

This is a documentation-only change. The README will be a concise, action-oriented quick start with
copy-pasteable Git commands, AI instruction examples, and links or references to related project
resources. It will introduce vertical-slice architecture briefly and defer detailed technical
standards to the planned root-level `frontend-architecture.md`.

## Feature Requirements

1. Identify the repository as a guidance submodule for any React application, not an executable
   starter kit, component library, or package.
2. Emphasize consistency across features, easier AI-assisted implementation, and maintainability.
3. Give a brief plain-language overview of vertical-slice architecture without duplicating detailed
   standards.
4. Show how to add the submodule at the host project's root in a folder named `react-vertical-slice`,
   using the SSH URL:
   `git@github.com:Mathewlenning/react-vertical-slice.git`.
5. Explain how to clone a host repository with submodules and how to initialize submodules in an
   existing clone.
6. Explain that the host repository pins a submodule commit, and show how to update the submodule,
   review the change, and commit the updated pointer in the host repository.
7. Provide copy-pasteable alternatives for `.github/copilot-instructions.md` and `AGENTS.md`. Do not
   recommend maintaining both by default. The examples must:
   - Directly identify the referenced file as the frontend architecture for the host React app.
   - Tell the AI to read it before planning or changing frontend code and apply it to all frontend
     work.
   - Treat the architecture conventions as binding and require explicit user approval before
     deviating.
   - Tell the AI to raise conflicts or missing guidance rather than inventing a convention silently.
8. Include a one-time example prompt for an AI chat that reinforces the same frontend-specific
   behavior.
9. Recommend the RPIE repository as an optional companion for structuring generative-AI development,
   with a link only and no installation steps.
10. Include brief contribution guidance and a license section linking to the existing GPL-3.0
    `LICENSE`.
11. State that Git is the only prerequisite. Do not add runtime setup, package installation, or
    build instructions.
12. Keep README content within the repository's 120-character line limit.

## Technical Design

- The README will live at the repository root.
- The consumer-side submodule path is `react-vertical-slice/`, alongside the host project's
  `package.json` and `src/`.
- AI instruction examples will refer to
  `react-vertical-slice/frontend-architecture.md`.
- The architecture document is planned but absent and is not a deliverable of this cycle. The README
  must not imply that the detailed standards are already included in this repository until that
  document exists.
- The optional RPIE companion URL is `https://github.com/Mathewlenning/rpie`.
- The existing root `LICENSE` is GNU GPL version 3.

## Implementation Steps

1. Create the root `README.md` with the project overview, setup and update guidance, AI examples,
   contribution guidance, and license reference.

## Dependencies

- Git is required for submodule operations.
- An AI coding assistant is optional and is needed only to use the AI instruction examples.
- `frontend-architecture.md` is a planned companion document; creating it is outside this cycle.

## Acceptance Criteria

- A reader can tell what the repository provides and that it is guidance rather than executable
  application code.
- The add command places the submodule at `react-vertical-slice/` in the host project's root and
  uses the specified SSH URL.
- Clone, initialize, pinning, and update instructions include the correct submodule workflows and
  explain the host repository's responsibility to commit the updated pointer.
- The Copilot, `AGENTS.md`, and one-time prompt examples are copy-pasteable and consistently
  frontend-specific. They apply the architecture as binding guidance to all host-app frontend work.
- Contribution, optional RPIE companion, and GPL-3.0 license information are present.
- No application dependencies, build steps, or runtime claims are introduced.
- Markdown renders cleanly, the line-length requirement is met, and references are accurate for
  current or clearly identified planned documents.
