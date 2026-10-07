# GitHub Actions Demo

This repository is a simple demonstration of GitHub Actions. It shows how a workflow can trigger automatically on a push event, run commands in a hosted Ubuntu runner, inspect repository context, and display job status.

## Overview

The project includes a single GitHub Actions workflow defined in:

- `.github/workflows/github-actions-demo.yml`

The workflow is configured to run on every push and performs the following tasks:

- Prints the event name that triggered the workflow
- Displays the operating system of the runner
- Shows the current branch and repository name
- Checks out the repository code
- Lists the files in the workspace
- Prints the final job status

## Project structure

```text
.github/
  workflows/
    github-actions-demo.yml
README.md
```

## Workflow trigger

```yaml
on: [push]
```

This means the workflow runs automatically whenever changes are pushed to the repository.

## Runner

```yaml
runs-on: ubuntu-latest
```

GitHub Actions executes the steps on a hosted Ubuntu virtual machine.

## Example output

The workflow emits messages like:

- "The job was automatically triggered by a push event."
- "This job is now running on an Ubuntu server hosted by GitHub!"
- "The repository has been cloned to the runner."
- "The workflow is now ready to test your code on the runner."

## Getting started

1. Push changes to the repository.
2. Open the GitHub Actions tab in the repository.
3. Select the workflow run.
4. Review the logs to see the job output.

## Notes

This repository is intentionally minimal and is intended for learning and demonstration purposes. It does not include application code, tests, or a build pipeline beyond the GitHub Actions example.
