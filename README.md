# React Vertical Slice

A lightweight architecture-guidance repository for React applications. Use it as a Git submodule
to help keep features consistent, maintainable, and easier to build with generative AI.

This repository provides architecture guidance, not a starter kit, component library, or executable
package. The planned root-level `frontend-architecture.md` will define the binding standards for
organizing React features into vertical slices. It is not included yet; the AI examples below assume
that file is available in the checked-out submodule.

A vertical slice groups the code that supports one user-facing feature, rather than organizing the
whole app only by technical layer.

## Add the submodule

Git is the only tooling prerequisite. The command uses SSH, so GitHub SSH authentication must
already be configured.

From the root of your React project, add the submodule:

```sh
git submodule add git@github.com:Mathewlenning/react-vertical-slice.git react-vertical-slice
```

Once the planned architecture document is added to this repository, it will be available at
`react-vertical-slice/frontend-architecture.md`. Commit the submodule configuration and pinned
revision to your project:

```sh
git add .gitmodules react-vertical-slice
git commit -m "Add React architecture submodule"
```

### Clone or initialize submodules

Clone a project that already uses submodules:

```sh
git clone --recurse-submodules <host-repository-url>
```

For an existing clone, initialize its submodules with:

```sh
git submodule update --init --recursive
```

### Update the architecture

The host project pins the submodule to a specific commit. To update it to the latest commit on its
configured remote branch, run:

```sh
git submodule update --remote react-vertical-slice
git diff --submodule
git add react-vertical-slice
git commit -m "Update React architecture submodule"
```

Review the change before committing. The host project's commit records the new submodule revision,
so other contributors receive that same version when they update the host project.

## Use with AI coding assistants

The architecture conventions are intended to apply to all frontend work in the host React app.
Treat them as binding: do not depart from them without explicit user approval. If the architecture
is missing or conflicts with another requirement, ask for clarification instead of silently
inventing a convention.

The architecture document is forthcoming. Add one of the following alternatives to your host
project once `react-vertical-slice/frontend-architecture.md` is available. Use the instruction-file
convention supported by your AI tool; you do not need both.

### GitHub Copilot

Add this to `.github/copilot-instructions.md`:

```md
## Frontend architecture

Before planning or changing frontend code, read
`react-vertical-slice/frontend-architecture.md`.
This is the binding frontend architecture for this React app. Follow it for all frontend work.
Do not deviate without my explicit approval. If it conflicts with another requirement or lacks
needed guidance, pause and ask me rather than inventing a convention.
```

### Other AI coding assistants

Add this to `AGENTS.md`:

```md
## Frontend architecture

Before planning or changing frontend code, read
`react-vertical-slice/frontend-architecture.md`.
This is the binding frontend architecture for this React app. Follow it for all frontend work.
Do not deviate without my explicit approval. If it conflicts with another requirement or lacks
needed guidance, pause and ask me rather than inventing a convention.
```

You can also use this prompt in an AI chat:

> Before planning or changing frontend code in this React app, read
> `react-vertical-slice/frontend-architecture.md`. Treat it as binding for all frontend work.
> Do not deviate without my explicit approval. If the file is missing, or its guidance conflicts
> with another requirement or is incomplete, pause and ask me.

For existing apps, adopt the conventions incrementally and have the AI surface conflicts with
current code before proceeding.

## Contributing

Suggestions to improve the architecture guidance are welcome. Open an issue to discuss a change or
submit a pull request with the proposed update.

## Optional development workflow

For a structured process for generative-AI development, see the
[RPIE repository](https://github.com/Mathewlenning/rpie). It is optional and is not required to use
this React architecture.

## License

This project is distributed under the [GNU General Public License v3.0](LICENSE).
