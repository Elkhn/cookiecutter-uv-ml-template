# cookiecutter-uv-ml-template


## Getting started (uv)
```code
# generate a project (no global install needed)
uvx cookiecutter gh:Elkhn/cookiecutter-uv-ml-template

cd <your-new-project>
uv sync
```

## GitHub CI workflow check
#### Run GitHub CI (Ruff linter) on push and pull requests to the `main` branch
```yaml
# Lint with Ruff; GitHub-style annotations on PRs
- name: Ruff check
  run: uvx ruff check --output-format=github .
```

## Code quality (ruff, isort, black via uvx)
### Run tools in ephemeral envs — no dev dependencies added to your project.

#### Lint (no changes)
```bash
# Lint entire repo
uvx ruff check .
```

#### Auto-fix
```bash
# 1) Sort imports
uvx isort .

# 2) Format code
uvx black .

# 3) Apply Ruff’s safe fixes (entire repo)
uvx ruff check --fix .
```
> Also remove unused imports/variables:
> ```bash
> uvx ruff check --fix --unsafe-fixes .
> ```


