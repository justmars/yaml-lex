# YAML Lex Formatter

yaml-lex is a Python tool for reformatting YAML files with specific wrapping rules.

It is designed to make YAML files more readable and maintainable, particularly for content-heavy nodes like content, caption, and title.

## Features

- Reformat content nodes using block scalar (|-), unless they contain Markdown tables.
- Wrap caption and title nodes if their effective length exceeds a configurable character limit.
- Wrap long single-line strings for other keys.
- Recursive formatting of folders containing YAML files.
- In-place formatting or output to a separate file.
- Rich logging using rich.
- Fully compatible with doctest-style examples for testing.
- Supports CI/CD workflows with testing, linting, pre-commit hooks, and docs building.
