# Contributing to PlayerHub Pipeline

Thank you for contributing to the PlayerHub Pipeline ecosystem! This guide outlines our engineering workflow, code standards, and PR requirements.

---

## 🛠️ Development Workflow

1. **Branching Strategy:**
   - Always branch from `main`:
     - `feat/<short-description>` for new capabilities
     - `fix/<issue-id>-<description>` for bug fixes
     - `refactor/<area>` for code restructuring
     - `docs/<topic>` for documentation improvements
   - Keep branch names lowercase, hyphenated, and descriptive.

2. **Commit Conventions:**
   - We strictly adhere to [Conventional Commits](https://www.conventionalcommits.org/):
     - `feat:` Introduces a new feature
     - `fix:` Patches a bug
     - `refactor:` Code changes that neither fix a bug nor add a feature
     - `perf:` Performance improvements
     - `test:` Adding or correcting tests
     - `docs:` Documentation only changes
     - `ci:` Changes to CI/CD workflows and automation scripts
   - When collaborating, include co-authorship:
     ```
     Co-authored-by: Omar Mohamed <omarmo.abdelsalam@gmail.com>
     ```

3. **Code Quality & Testing:**
   - Format and lint all Python code with `ruff`:
     ```bash
     uv run ruff check --fix
     uv run ruff format
     ```
   - Ensure all unit, integration, and contract tests pass before pushing:
     ```bash
     uv run pytest
     ```

4. **Pull Requests & Code Reviews:**
   - Fill in the PR template completely with description and verification steps.
   - All CI checks must be 100% green before any PR can be merged.
   - We enforce squash-and-merge with linear commit history on `main`.

5. **Secrets & Security:**
   - Never commit API keys, database credentials, or private certificates.
   - Report security vulnerabilities according to our [SECURITY.md](SECURITY.md) policy.
