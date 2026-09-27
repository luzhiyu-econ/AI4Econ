# AI4Econ

An online book tutorial on AI workflows for economics research. Read it at **https://zhiyulu.org/AI4Econ/**.

The current edition walks through a policy-text annotation example: defining the observation unit, writing an annotation rule, evaluating labels, and using the resulting measure in economic analysis.

## Edit and preview locally

This project uses MkDocs Material and `uv`. On the research NFS mount, the project environment belongs on local SSD; `.envrc` sets `UV_PROJECT_ENVIRONMENT` to `$HOME/.venvs/AI4Econ` when `direnv` is enabled.

```sh
direnv allow
uv sync --locked
uv run --no-sync mkdocs serve
```

Open the local URL printed by MkDocs. Without `direnv`, set `UV_PROJECT_ENVIRONMENT="$HOME/.venvs/AI4Econ"` in your shell before running `uv`.

## Publish

Edit Markdown files in `docs/` and the navigation in `mkdocs.yml`. A push to `main` runs a strict build and deploys the generated `site/` directory through GitHub Actions. Pull requests run the build without deploying. The repository's **Settings → Pages → Build and deployment → Source** must be set to **GitHub Actions**.

Build locally with:

```sh
uv run --no-sync mkdocs build --strict
```

The generated `site/` directory is ignored by Git. The source files and `uv.lock` are committed, so local builds and CI use the same resolved dependencies.
