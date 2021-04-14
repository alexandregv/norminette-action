# norminette-action@v3

This GitHub Action checks if your code passes the 42School's norminette linter, after each push.
See a demo on [alexandregv/norminette-action-demo](https://github.com/alexandregv/norminette-action-demo).

**/!\\ This version (`@v3`) is for Norm version 3, if you want Norm version 2 please use [norminette-action@v2](https://github.com/alexandregv/norminette-action/tree/v2) /!\\**

## Inputs

### `flags`

Description: Flags passed to norminette.
Format: `[options] <path>`
Default: `.` (all files)

## Example usage

```yml
# .github/workflows/main.yml
on: [push, pull_request]

jobs:
  norminette_job:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: [ '3.7', '3.8', '3.9' ]
    name: norminette
    steps:
    - uses: actions/checkout@v2
    - name: Setup python
        uses: actions/setup-python@v2
        with:
          python-version: ${{ matrix.python-version }}
          architecture: x64
    - uses: alexandregv/norminette-action@v3
      with:
        flags: '.'
```

## Badge

You can add a badge (![norminette](https://github.com/alexandregv/norminette-action-demo/workflows/norminette/badge.svg)) to show current norminette status by adding this markdown code to your README.md:

```md
![norminette](https://github.com/<OWNER>/<REPOSITORY>/workflows/<WORKFLOW_NAME_OR_FILE>/badge.svg)
```

More infos on [GitHub Docs](https://docs.github.com/en/free-pro-team@latest/actions/managing-workflow-runs/adding-a-workflow-status-badge).

## See also

- [norminette-action-demo](https://github.com/alexandregv/norminette-action-demo) - Demo repository for this action.
- [norminette-docker](https://github.com/alexandregv/norminette-docker) - Docker image for norminette (used by this action).
- [norminette-vim](https://github.com/alexandregv/norminette-vim) - Vim integration for norminette. Displays norm errors directly inside Vim.

All of these are compatible with Norm version 2 and 3.
