# minigrep

A simple command-line tool that searches for text patterns in files, inspired by the classic `grep` utility. Built with Rust as a learning project.

## Features

- Search for text patterns in files
- Case-sensitive search (default)
- Case-insensitive search (via environment variable)
- Clean, readable output

## Installation

Make sure you have [Rust](https://www.rust-lang.org/tools/install) installed, then clone and build the project:

```bash
git clone sudosayonara/minigrep
cd minigrep
cargo build --release
```

## Usage

Basic search (case-sensitive):

```bash
cargo run -- <search_term> <file_path>
```

Example:

```bash
cargo run -- nobody poem.txt
```

Case-insensitive search:

```bash
IGNORE_CASE=1 cargo run -- <search_term> <file_path>
```

Example:

```bash
IGNORE_CASE=1 cargo run -- NOBODY poem.txt
```

## How It Works

minigrep reads the specified file and searches for lines containing the search term. By default, the search is case-sensitive. Set the `IGNORE_CASE` environment variable to enable case-insensitive matching.

## Testing

Run the test suite with:

```bash
cargo test
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
