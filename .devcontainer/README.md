# Devcontainer Draft

This devcontainer is intended for a fuller Codespaces workshop setup:

- Python workspace container
- PostgreSQL sidecar with seeded `trips` data
- Python packages installed from `requirements.txt`

## What it gives learners

- a reproducible environment
- PostgreSQL already available
- a known PostgreSQL connection URI
- no local PostgreSQL setup required

## Exact manual test

If you want to validate whether Codespaces is the right teaching environment, the test path is:

```bash
python --version
uv --version
python -m pip install -r requirements.txt
python app.py
```

Things to judge while testing:

- how long the codespace build takes
- whether `pip install -r requirements.txt` is painless
- whether Postgres is reliably ready when you need it
- whether the whole flow is simpler than local setup

## Main files

- `devcontainer.json`
- `docker-compose.yml`
- `post-create.sh`
- `postgres/init/01-trips.sql`
