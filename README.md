# CLI Data Pipeline

Starter repository for the **Python for Engineers** capstone on [DutchEngineer](https://dutchengineer.org).

## What you will build

A command-line data pipeline that reads a CSV file, validates each row, transforms the values, and writes cleaned output — with structured error reporting and a tested interface.

The goal is not a script you run once. It is a tool another engineer can install, run on an unfamiliar dataset, and extend without reading your notes.

## Requirements

1. **Memory-safe reading** — the pipeline must not load the entire input file into memory at once. Peak memory usage must not scale with file size.
2. **Type-safe transformation layer** — all public functions carry type annotations. A strict type checker must pass with zero errors.
3. **Structured error handling** — validation failures and transformation failures must be distinguishable by type. Catching the base error type must catch both. Error messages must identify where in the input the failure occurred.
4. **CLI with correct exit codes** — the pipeline is invocable from the command line with input and output paths as arguments. It exits 0 on success, 1 when validation failures occur, 2 on unexpected errors. It prints a summary of rows processed and errors encountered.
5. **Test suite** — tests cover: multiple invalid row formats via a single parametrized case, a temporary file fixture, and verification that reading does not materialise the full file. All tests pass from a clean install.

## Getting started

1. Fork this repository
2. Clone your fork: `git clone https://github.com/<your-username>/cli-pipeline-starter`
3. Install dependencies: `uv sync`
4. Run the tests: `uv run pytest`

## Submitting

Push your completed work to your fork. Paste the repository URL into the capstone submission form in your dashboard.
