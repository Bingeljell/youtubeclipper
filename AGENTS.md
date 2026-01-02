# Repository Guidelines

## Project Overview
This repository currently contains the MVP product spec for a local YouTube clipping CLI. The implementation is not yet present; use `spec.md` as the source of truth for scope, flags, and behavior.

## Project Structure & Module Organization
- `spec.md`: MVP requirements, CLI UX, and architecture notes.
- Source code, tests, and assets are not yet in the repo. When implementation lands, document the actual locations here (for example, `src/`, `tests/`, or `assets/`).

## Build, Test, and Development Commands
No build/test commands are defined yet because the codebase is not implemented. When the CLI is added, include runnable examples here, such as the planned interface from the spec:

```bash
youtubeclipper <url> <start> <end>
youtubeclipper <url> --clips "10-30,120-150" --outdir ./clips
```

## Coding Style & Naming Conventions
Until a codebase exists, follow these guidelines for consistency with the Python 3.11+ recommendation in `spec.md`:
- Indentation: 4 spaces, no tabs.
- Naming: `snake_case` for functions/variables, `PascalCase` for classes.
- Files: lowercase with underscores (e.g., `clipper.py`).
- Keep CLI parsing separate from download/clip logic to match the architecture notes.

## Testing Guidelines
Tests are not present yet. When added, prefer `pytest` and place tests under `tests/` with names like `test_cli.py`. Aim to cover input validation, clip range parsing, and fast vs precise modes.

## Commit & Pull Request Guidelines
There is no Git history to infer conventions. Use clear, imperative commit messages (e.g., "Add clip range parser"). For PRs, include:
- A short summary of changes.
- Testing notes (commands run or “not run”).
- Linked issues if applicable.
- Screenshots or GIFs for any future UI work.

## Security & Configuration Tips
This tool is intended for local use. Be explicit about dependencies (e.g., `ffmpeg`, `yt-dlp`), handle missing binaries with clear errors, and avoid logging sensitive URLs beyond what is necessary.
