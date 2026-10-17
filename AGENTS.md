# Documentation project instructions

## About this project

- This is the documentation site for **Neuron**, a runtime for building and operating complex software systems from composable, executable capabilities.
- Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json`.
- Brand theme is dark monochrome with light mode support.

## Terminology

- Use **capability runtime** (never "executor" or "module").
- Use `capability runtime` (with a space) for the CLI command, never `capability-runtime`.
- `neuron run` is **synchronous** — it sends one `POST /v1/run` request and prints the result. It does not stream events or create instances.
- Build records live at `.neuron/builds/<fingerprint>/build.json` with a mutable pointer at `.neuron/current.json`. The legacy `.neuron/register.json` is obsolete.
- The project is in active development (v0.1.0). Mark experimental features with subtle `<Note type="info">` badges.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements: Click **Settings**.
- Code formatting for file names, commands, paths, and code references.
- No marketing language ("powerful", "seamless", "robust", "cutting-edge").
- No filler phrases ("it's important to note", "in order to").

## Content boundaries

- Document the public API surface: CLI commands, HTTP API, SDK, capability runtime protocol.
- Do not document internal Go package structure or implementation details.
- Do not document the legacy global daemon model except where still relevant.
- Do not document `neuron instance` commands (not registered in the CLI).