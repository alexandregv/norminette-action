# norminette-action@v3

This GitHub Action checks if your code passes the 42School's norminette linter, after each push.  
See a demo on [alexandregv/norminette-action-demo](https://github.com/alexandregv/norminette-action-demo).

/!\\ This Action supports all norminette versions. You should specify the exact version, for example `v3.3.51`. Check your campus rules to find the version you should use.  
`@v3` always refers to the latest v3.x.y.  

For v2 use [norminette-action@v2](https://github.com/alexandregv/norminette-action/tree/v2)

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

* [norminette-action-demo](https://github.com/alexandregv/norminette-action-demo) - Demo repository for this action.
* [norminette-docker](https://github.com/alexandregv/norminette-docker) - Docker image for norminette (used by this action).
* [norminette-vim](https://github.com/alexandregv/norminette-vim) - Vim integration for norminette. Displays norm errors directly inside Vim.

All of these are compatible with Norm version 2 and 3.

## Stargazers over time
[![Stargazers over time](https://starchart.cc/alexandregv/norminette-action.svg?variant=adaptive)](https://starchart.cc/alexandregv/norminette-action)
