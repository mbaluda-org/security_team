# security_team
The repo provides a reusable workflow [`.github/workflows/code_analysis.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/code_analysis.yml) to centralize the configuration for CodeQL scans but allowing for a per-repo custom build script.

# Usage: 
Push the default files to every repo which is part of the roll-out
- [`.github/workflows/codeql.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/codeql.yml)
- [`.github/actions/custom_build/action.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/actions/custom_build/action.yml)
- [`.github/codeql/codeql-config.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/codeql/codeql-config.yml)

Customize the action when needed (e.g. [mbaluda-org/dev_team](https://github.com/mbaluda-org/dev_team/blob/main/.github/actions/custom_build/action.yml))
Customize the config when needed (e.g. [mbaluda-org/dev_team](https://github.com/mbaluda-org/dev_team/blob/main/.github/codeql/codeql-config.yml))

Add `.github/codeql/codeql.yml` and `.github/workflows/codeql-config.yml` in the `CODEOWNERS` file.
