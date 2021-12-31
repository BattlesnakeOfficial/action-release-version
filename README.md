# GitHub Action: Release VERSION.txt
Simple GitHub Action to write VERSION.txt and include it in each release. Note this force updates the release tag, such that the tagged commit contains the new VERSION.txt file.

## Usage
```yaml
name: Release

on:
  release:
    types: [published]
    branches: [main]

jobs:
  version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: BattlesnakeOfficial/action-release-version@v1
```
