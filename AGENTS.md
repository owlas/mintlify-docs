# Documentation project instructions

## About this project

- This is the public documentation for Rainbow Machine, built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- The audience is an engineer whose repo runs on Rainbow Machine: a repo owner editing `rainbow.toml`, or a developer opening environments from a pull request or a coding agent.

## Terminology

- An **environment** is the product object: a running copy of the app at a URL. Never "instance", "sandbox", "preview env", or "VM". A VM is the mechanism and is not mentioned.
- The **parent** is the warm environment of the default branch that every environment is forked from.
- A **fork** is a copy of a live environment or of the parent.
- The **recipe** is `rainbow.toml`. Use the file name when pointing at the file, "recipe" when talking about what it declares.
- A **rung** is one `[[tier]]` entry. The list of rungs is the **ladder**.
- **Secrets** are names in the recipe with values set on the dashboard.
- **Dashboard** for dashboard.rainbowmachine.ai. **Tools** for the MCP tools an agent calls.

## Style

- Active voice, present tense, second person. One idea per sentence.
- Sentence case for headings. Task-oriented headings in guides ("Add a service"), noun phrases in reference pages.
- Bold for UI elements: click **Add secret**. Code formatting for keys, file names, commands, and tool names.
- Say what a thing does and when you need it, then show it. Every table is introduced by a sentence.
- Numbers are measured and dated where they matter; prefer "a few hundred milliseconds" over a precise figure that drifts.

## Content boundaries

- Document only what a repo owner or developer can see or do: the recipe, the dashboard, the pull request comment and status, the MCP tools, the environment's URL and states.
- Do not document platform internals: hosts, the image compiler, snapshot mechanics, the reaper, the ingress, networking, the operator CLI, or the control plane. If a page needs an internal fact to explain a behavior, state the behavior and its consequence, not the mechanism.
- Do not link to internal repositories or design documents.
- Every claim must be checkable by a user against the product. If it is not, cut it or sharpen it.
