# CodeQL Setup for Security Teams
The repo stores a [reusable workflow](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/code_analysis.yml) and a default [CodeQL configuration file](https://github.com/mbaluda-org/security_team/blob/main/codeql-config.yml) to centralize the configuration for CodeQL scans.
It allows customizing build scripts and CodeQL configurations on a per-repo basis.

Examples:
- https://github.com/mbaluda-org/dev_team_default/actions
- https://github.com/mbaluda-org/dev_team_custom/actions

## Using the Default Configuration: 
- Push the [workflow file](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/codeql.yml) to every repo which is part of the roll-out
(e.g. [mbaluda-org/dev_team_default](https://github.com/mbaluda-org/dev_team_default/blob/main/.github/workflows))
- [OPTIONAL] Customize the centralized [CodeQL configuration file](https://github.com/mbaluda-org/security_team/blob/main/codeql-config.yml)
- [OPTIONAL] Add the workflow and the configuration files to `CODEOWNERS` (e.g. [mbaluda-org/dev_team_default](https://github.com/mbaluda-org/dev_team_default/blob/main/.github/CODEOWNERS))

## Repo-specific Custom Configuration:
- Customize the repo-specific build creating a local action named `custom_build` (e.g. [mbaluda-org/dev_team_custom](https://github.com/mbaluda-org/dev_team_custom/blob/main/.github/actions/custom_build/action.yml))
- Customize the repo-specific CodeQL config in `.github/codeql/codeql-config.yml` (e.g. [mbaluda-org/dev_team_custom](https://github.com/mbaluda-org/dev_team_custom/blob/main/.github/codeql/codeql-config.yml))
- Add the workflow and the configuration files to `CODEOWNERS` (e.g. [mbaluda-org/dev_team_custom](https://github.com/mbaluda-org/dev_team_custom/blob/main/.github/CODEOWNERS))
