# powerd6 .github

A central repository for the powerd6 project 

## Workflows

- [![Sync Labels](https://github.com/powerd6/.github/actions/workflows/sync-labels.yml/badge.svg)](https://github.com/powerd6/.github/actions/workflows/sync-labels.yml)
  - Responsible for setting a standard group of labels across all repositories
    - List of repositories is set on the workflow definition
    - Configuration for each label is stored on `.github/labels.yml`
- [![Sync Settings](https://github.com/powerd6/.github/actions/workflows/sync-settings.yml/badge.svg)](https://github.com/powerd6/.github/actions/workflows/sync-settings.yml)
  - Responsible for settings up github repositories with the same settings and branch protection rules
    - List of repositories is set on the workflow definition
    - Settings are set on the workflow definition
