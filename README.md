# norminette-action@v2

This GitHub Action checks if your code passes the 42School's norminette linter, after each push.  
See a demo on [alexandregv/norminette-action-demo](https://github.com/alexandregv/norminette-action-demo).

**/!\\ This version (`@v2`) is for Norm version 2, if you want Norm version 3 please use [norminette-action@v3](https://github.com/alexandregv/norminette-action/tree/v3) /!\\**

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
    name: norminette
    steps:
    - uses: actions/checkout@v2
    - uses: alexandregv/norminette-action@v2
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

* [norminette-action-demo](https://github.com/alexandregv/norminette-action-demo) - Demo repository for this action.
* [norminette-docker](https://github.com/alexandregv/norminette-docker) - Docker image for norminette (used by this action).
* [norminette-vim](https://github.com/alexandregv/norminette-vim) - Vim integration for norminette. Displays norm errors directly inside Vim.

All of these are compatible with Norm version 2 and 3.
