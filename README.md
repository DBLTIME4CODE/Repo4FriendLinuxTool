# MyProject

Practical Python project scaffold with a Scrum-friendly workflow where you provide priorities and validation, and coding is delegated to the AI assistant.

## Project Goals

- Keep a clean, scalable file organization.
- Standardize quality checks (formatting, linting, tests).
- Make implementation requests fast and predictable.
- Keep decision-making and review with you.

## Structure

```text
MyProject/
	.github/
		copilot-instructions.md
	.vscode/
		extensions.json
		settings.json
	docs/
		templates/
			backlog-item.md
			sprint-plan.md
			review-checklist.md
	scripts/
		bootstrap.ps1
		check.ps1
		run.ps1
	src/
		myproject/
			__init__.py
			main.py
			settings.py
	tests/
		test_smoke.py
	.env.example
	.gitignore
	pyproject.toml
	requirements.txt
	requirements-dev.txt
	README.md
```

## Quick Start (Windows PowerShell)

1. Create and activate virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate
```

2. Install dependencies:

```powershell
pip install -r requirements.txt
pip install -r requirements-dev.txt
```

3. Copy and edit environment variables:

```powershell
Copy-Item .env.example .env
```

4. Run checks and tests:

```powershell
./scripts/check.ps1
```

5. Run app:

```powershell
./scripts/run.ps1
```

## Scrum Workflow

1. Define work item in `docs/templates/backlog-item.md` format.
2. Ask the assistant to implement the item and include acceptance criteria.
3. Assistant updates code + tests.
4. You validate with `./scripts/check.ps1` and review diffs.
5. Approve or request changes.

## Common Prompts

- `Implement this backlog item from docs/templates/backlog-item.md and add tests.`
- `Refactor module X to improve readability without behavior changes.`
- `Add feature Y and ensure all acceptance criteria pass.`
- `Review this branch for bugs and missing tests.`

## Notes

- Use `.github/copilot-instructions.md` to enforce coding conventions for this repository.
- Keep runtime deps in `requirements.txt` and tooling/test deps in `requirements-dev.txt`.
