# CalVersion

This action generates a UTC-based [CalVer](https://calver.org/) in the format YYYY.0M0D.MICRO

## Usage

See [action.yml](action.yml).

## Examples

### Generate a New Version

```yaml
---
name: My Workflow

on:
  push:
    branches:
      - master

jobs:
  release:
    name: Release
    runs-on: [ ubuntu ]
    steps:
      - name: Checkout source code
        uses: actions/checkout@v3

      - name: Generate Version
        id: version
        uses: phoenixTW/cal-version@master
```
