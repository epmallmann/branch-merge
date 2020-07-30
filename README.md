# Merge Branch
Automate merging of a source branch into a target branch.

## Usage

```yaml
on:
  push:
    branches:
      - "release/*"
jobs:
  merge-branch:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: everlytic/branch-merge@1.0.2
        with:
          github_token: ${{ github.token }}
          source_ref: ${{ github.ref }}
          target_branch: 'master'
```
