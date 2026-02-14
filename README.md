# setup-jake

## Set up and install `jake`

[Jake](https://github.com/AstraBert/jake) is a make-like command line utility to execute tasks on Unix OS.

## Example Usage

```yml
name: Update LlamaAgent Deployment

on:
  push:
    branches:
        - main

jobs:
  update-deployment:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Set up Jake
        uses: AstraBert/setup-jake@v0.1.0
```

## How does it work

This action works by:

- Setting up cargo (through `dtolnay/rust-toolchain@stable`)
- Installing `jake` through `cargo install jake`.

## License

The code is provided under the [MIT License](./LICENSE)
