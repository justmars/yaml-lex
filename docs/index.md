# yaml-lex

Reformat YAML files with specific wrapping rules for content, caption, and title.

Supports:

- content → always wrapped as block scalar (|-), unless Markdown table
- caption & title → wrap as block scalar if effective length exceeds char_limit
- other strings → wrap single-line long strings
- file or folder input, recursive processing, in-place editing, optional output file
- rich logging

Example usage:

    python src/format.py input.yml --inplace
    python src/format.py /path/to/folder --inplace
    python src/format.py input.yml --output formatted.yml --char-limit 100

## Doctest examples

    >>> wrap_value("caption", "This is a very long caption that should be wrapped because it exceeds the default limit", 20)
    'This is a very long\\ncaption that should\\nbe wrapped because\\nit exceeds the\\ndefault limit'

    >>> wrap_value("title", "Short title", 20)
    'Short title'

## Documentation

::: src.format
