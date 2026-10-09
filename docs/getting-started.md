# Getting started

## Installation

```console
uv tool install git+https://github.com/ahojukka5/sqlfence
```

For a project dependency:

```console
uv add --dev 'sqlfence @ git+https://github.com/ahojukka5/sqlfence'
```

DuckDB support is available through the optional extra:

```console
uv add 'sqlfence[duckdb] @ git+https://github.com/ahojukka5/sqlfence'
```

These git URLs are the install path until the first PyPI upload. See
[Releasing](releasing.md).

## Render a document

```console
sqlfence input.md --output output.md
```

Use an in-memory SQLite database by default. Blocks in the same document share
one connection, so setup statements are visible to later queries.

## Validate in CI

```console
sqlfence docs/database.md --check
```

The command exits non-zero when parsing or SQL execution fails.
