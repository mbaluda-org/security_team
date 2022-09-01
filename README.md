# security_team
The repo provides a reusable workflow [`.github/workflows/code_analysis.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/code_analysis.yml) to centralize the configuration for CodeQL scans but allowing for a per-repo custom build script.

# Usage: 
Push the default files to every repo which is part of the roll-out
- [`.github/workflows/codeql-analysis.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/workflows/codeql.yml)
- [`.github/actions/custom_build/action.yml`](https://github.com/mbaluda-org/security_team/blob/main/.github/actions/custom_build/action.yml)

Customize the action when needed (e.g. [mbaluda-org/dev_team](https://github.com/mbaluda-org/dev_team/blob/main/.github/actions/custom_build/action.yml))
