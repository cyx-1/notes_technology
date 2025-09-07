# Pre-commit

- pre-commit maintains code quality prior to committing code
- pre-commit is typically installed via [uv tool](uv.md)
- pre-commit for each project is configured via a file called ```.pre-commit-config.yaml```, which typically contains content like this:

```
repos:
-   repo: https://github.com/psf/black
    rev: 25.1.0  # Latest as of July 2025
    hooks:
    - id: black
      # specifies which Python intepreter version should be used to run this hook
      # it should be consistent with the python version used to install pre-commit in pipx
      language_version: python3.11
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v5.0.0  # Latest as of July 2025
    hooks:
    - id: check-merge-conflict
    - id: check-json
```

- To make sure pre-commit start to work for a project, run this command in the project folder:

```
pre-commit install

output should say: pre-commit installed at .git\hooks\pre-commit
```

- next time prior to committing code via git, you will see checks like this:

```
black....................................................................Passed
check for merge conflicts................................................Passed
fix double quoted strings................................................Passed
check json...........................................(no files to check)Skipped
check yaml...............................................................Passed
trim trailing whitespace.................................................Passed
flake8...................................................................Passed
seed isort known_third_party.............................................Passed
isort....................................................................Passed
```

Back to [index](index.md)