# Template usage examples

This directory contains a few examples using the Coq-community 
[template](https://github.com/coq-community/templates).

## How to use
- `Makefile.common` includes generic configuration to build from template.
    + `TEMPLATES` variable indicates the directory where templates are stored.
- Each example subdirectory has a `Makefile` that includes `Makefile.common`.
    + Running `make` in subdirectory builds all targets specified there.
    + `chapar/Makefile` also shows how to build OPAM file for extracted program.
- Running `make` at top level builds all examples.
