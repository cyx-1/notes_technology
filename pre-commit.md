# Pre-commit

- pre-commit maintains code quality prior to committing code
- pre-commit is typically installed via [uv tool](uv.md)
- pre-commit for each project is configured via a file called ```.pre-commit-config.yaml```, which typically contains content like this:

```
repos:
-   repo: https://github.com/astral-sh/ruff-pre-commit
    rev: v0.12.11 # Latest as of Aug 28, 2025
    hooks:
      - id: ruff-check
        args: [--fix]
      - id: ruff-format
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v6.0.0  # Latest as of August 9, 2025
    hooks:
    - id: check-merge-conflict
    - id: check-json
      exclude: \.vscode/launch\.json$
    - id: check-yaml
    - id: trailing-whitespace
```

- To make sure pre-commit start to work for a project, run this command in the project folder:

```
pre-commit install

output should say: pre-commit installed at .git\hooks\pre-commit
```

- next time prior to committing code via git, you will see checks like this:

```
ruff check...............................................................Passed
ruff format..............................................................Passed
check for merge conflicts................................................Passed
check json...............................................................Passed
check yaml...............................................................Passed
trim trailing whitespace.................................................Passed
```

Back to [index](index.md)