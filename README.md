# modify-file-action

This repo implements a reusable github action workflow that lets you replace a target string with another in a given file.

## Inputs

This workflow expects you to provide following inputs:

* inputs.file-path: Path to the file within your repository for the file you want to modify.
* inputs.target-string: String that you would like to replace.
* inputs.replacer-string: String that you would like to use instead of the target string.

## Usage Example

```
jobs:
  use-reusable-modify-file:
    uses: damiel/modify-file-action/.github/workflows/modify-file.yml@main
    with:
      file-path: demo.txt
      target-string: ${{ vars.TARGET_STRING }}
      replacer-string: ${{ vars.REPLACER_STRING }}
```
