# powerd6 .github

A central repository for the powerd6 project

## Workflows

- [![Sync Repositories](https://github.com/powerd6/.github/actions/workflows/sync-repositories.yml/badge.svg)](https://github.com/powerd6/.github/actions/workflows/sync-repositories.yml)

  - Responsible for keeping repositories in sync in terms of configurations
    - List of repositories is set on the workflow definition
    - Responsible for settings up github repositories with the same settings and branch protection rules
      - Settings are set on the workflow definition
      - Configuration for each label is stored on `.github/labels.yml`
    - Responsible for setting a standard group of labels across all repositories
      - List of repositories is set on the workflow definition

- [![Check PR](https://github.com/powerd6/.github/actions/workflows/check-pr.yml/badge.svg)](https://github.com/powerd6/.github/actions/workflows/check-pr.yml)
  - Responsible for checking the quality of PR titles

### Re-usable workflows

- PR Lint

  - Responsible for checking the quality of PR titles
  - Usage:

    ```yaml
    jobs:
      lint-pr:
        uses: powerd6/.github/.github/workflows/pr-lint.yml@main
        secrets:
          REVIEWER_TOKEN: ${{ secrets.REVIEWER_TOKEN }}
    ```
