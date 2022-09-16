# Centralized reusable Code Scanning workflow
Code Scanning workflows are usually owned and managed by developer teams, but larger organizations often prefer a model where a central security team is in control of the configuration of the analysis

This repo contains:
1. a centralized [reusable workflow](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/code_analysis.yml) owned by the security team
2. a centralized [CodeQL configuration file](https://github.com/mbaluda-org/security_team/blob/main/codeql-config.yml)
3. a standardized [CodeQL workflow](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/codeql.yml) that is pushed to all the interested repos

Repository-specific customiziations are possible adding a local build action in `.github/actions/custom_build/action.yml` and CodeQL configuration in `.github/codeql/codeql-config.yml`.

Customization changes can be controlled using the `CODEOWNERS` file.

Examples:
- https://github.com/mbaluda-org/dev_team_default/actions
- https://github.com/mbaluda-org/WebGoat_custom_build/actions

## Using the Default Configuration: 
- [Push](https://github.com/mario-campos/gh-code-scanning) the [workflow file](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/codeql.yml) to every repo which is part of the roll-out
(e.g. [mbaluda-org/dev_team_default](https://github.com/mbaluda-org/dev_team_default/blob/main/.github/workflows))
- [OPTIONAL] Add the workflow file to `CODEOWNERS` (e.g. [mbaluda-org/dev_team_default](https://github.com/mbaluda-org/dev_team_default/blob/main/.github/CODEOWNERS))

## Repo-specific Custom Configuration:
- Customize the repo-specific build creating a local action named `custom_build` (e.g. [mbaluda-org/WebGoat_custom_build](https://github.com/mbaluda-org/WebGoat_custom_build/blob/main/.github/actions/custom_build/action.yml))
- Customize the repo-specific CodeQL config in `.github/codeql/codeql-config.yml` (e.g. [mbaluda-org/WebGoat_custom_build](https://github.com/mbaluda-org/WebGoat_custom_build/blob/main/.github/codeql/codeql-config.yml))
- The reusable workflow can be diversified in feature branches (e.g. [project Lombok support](https://github.com/mbaluda-org/security_team/blob/lombok/.github/workflows/code_analysis.yml#L79))
  - [OWASP WebGoat without Lombok support](https://github.com/mbaluda-org/WebGoat/security/code-scanning)
  - [OWASP WebGoat with Lombok support](https://github.com/mbaluda-org/WebGoat_delombok/security/code-scanning)
- Add the workflow and the configuration files to `CODEOWNERS` (e.g. [mbaluda-org/WebGoat_custom_build](https://github.com/mbaluda-org/WebGoat_custom_build/blob/main/.github/CODEOWNERS))
