# ruff

An extremely fast Python linter, written in Rust.

- backed by https://astral.sh/
- used by FastAPI, Pandas, SciPy, and many others...
- docs at https://beta.ruff.rs/docs
- playground at https://play.ruff.rs/

---

# ruff?

## kitchen sink python linter

 - 10-100x faster than existing linters
 - support for automatic error correction
 - over 500 built-in rules
 - easy integrations for IDEs and ships an LSP
 - documentation, testing, code complexity

## what does it replace?

- `flake8`
- dozens of `flake8` plugins like bugbear, tryceratops
- `isort`
- `pydocstyle`
- `eradicate`
- `pyupgrade`
- `autoflake`

## use it with?

 - use `ruff` in conjunction with type checking and formatting tools
 - `mypy` and `black` are my go-tos for typing and formatting

---

# Basic usage

## `pip install ruff`

 - `ruff` enables `pycodestyle` and `flake8` by default
 - full default configuration can be found here:
https://beta.ruff.rs/docs/configuration/#using-pyprojecttoml
 - can use `pyproject.toml` or `ruff.toml` files for configuration,  
 configuration files can be cascading in cases of large repos

## `ruff check . --fix`

 - 🔥 __FAST__ 🔥
 - results are cached locally in `.ruff_cache`
 - fixes "fixable" errors, not all errors are fixable
 - lots of other options like `--show-source` or `--diff`

## `ruff rule <RULE>`

 - provides rust-style explanation of the given rule
 - sometimes includes an example of before/after

---

# `ruff --help`

```
Ruff: An extremely fast Python linter.

Usage: ruff [OPTIONS] <COMMAND>

Commands:
  check   Run Ruff on the given files or directories (default)
  rule    Explain a rule
  config  List or describe the available configuration options
  linter  List all supported upstream linters
  clean   Clear any caches in the current directory and any subdirectories
  help    Print this message or the help of the given subcommand(s)

Options:
  -h, --help     Print help
  -V, --version  Print version

Log levels:
  -v, --verbose  Enable verbose logging
  -q, --quiet    Print lint violations, but nothing else
  -s, --silent   Disable all logging (but still exit with status code "1" upon detecting lint violations)
```

---

# Downsides?

 - potentially a lot of knobs to tweak in configurations
 - young, still in "beta" like `mypy`

`#worth`