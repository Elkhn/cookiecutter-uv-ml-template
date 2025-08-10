# {{ cookiecutter.project_name }}

{{ cookiecutter.description }}

## Structure
- `data/` – external → interim → processed
- `src/` – data, features, models, visualization
- `notebooks/` – analysis notebooks
- `reports/figures/` – generated outputs

## Getting started (uv)
```bash
# create venv and sync (will create uv.lock)
uv sync

# add a runtime dependency
uv add numpy

# run code
uv run python -m {{ cookiecutter.package_name }}.models.train_model
```

## Getting started (uv)
```code
# generate a project (no global install needed)
uvx cookiecutter gh:your-user/cookiecutter-uv-ml-template

cd <your-new-project>
uv sync
```