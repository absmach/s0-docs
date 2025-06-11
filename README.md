# S0 Documentation

This repo collects the collaborative work on S0 documentation.

Documentation is auto-generated from Markdown files in this repo.

[MkDocs](https://www.mkdocs.org/) is used to serve the docs locally with different theming.

## Install

Doc repo can be fetched from GitHub:

```bash
git clone https://github.com/absmach/s0-docs.git
```

## Prerequisites

[Python](https://www.python.org/downloads/) 3.11 or higher is required to run MkDocs.

1. Create a virtual environment:

   ```bash
   python -m venv venv
   ```

2. Activate the virtual environment:

   ```bash
   source venv/bin/activate
   ```

3. Install [MkDocs](https://www.mkdocs.org/#installation)

   ```bash
   pip install mkdocs
   ```

4. Additionally, install [Material theme](https://squidfunk.github.io/mkdocs-material/):

   ```bash
   pip install mkdocs-material
   ```

## Usage

Use MkDocs to serve documentation:

```bash
mkdocs serve
```

Then just point the browser to [http://127.0.0.1:8000](http://127.0.0.1:8000).
