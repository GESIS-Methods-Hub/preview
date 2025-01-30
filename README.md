# GESIS Methods Hub Preview as GitHub Action

This is a [GitHub Action](https://github.com/features/actions) to test a GitHub repository for Methods Hub.

## Usage

Create the file `.github/workflows/methods-hub.yml` with

```yaml
name: Test Content for Methods Hub
on:
  push:
    branches:
      - main
jobs:
  test-methods-hub-render:
    runs-on: ubuntu-24.04
    name: Test Methods Hub render
    steps:
      - uses: actions/checkout@v4
      - uses: GESIS-Methods-Hub/preview@v1
        with:
          file: README.md
```