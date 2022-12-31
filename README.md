# Overview

[![Deploy to Pages](https://github.com/IgKniteDev/docs/actions/workflows/deploy.yml/badge.svg)](https://github.com/IgKniteDev/docs/actions/workflows/deploy.yml)

This is the repository for the official documentation of IgKnite. Read about all-things IgKnite [by clicking here!](https://igknitedev.github.io/docs)

<br>

## Requirements

Building this documentation from thin air requires the [mdbook (Rust)](https://rust-lang.github.io/mdBook/) package.

```bash
# install it globally using cargo

$ cargo install mdbook --vers [version-num]
```

## Build

To build the documentation, type:

```bash
$ mdbook build
```

The rendered copy will be located in the `book` subdirectory.