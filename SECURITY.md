# Security Workflows

This repository includes several security-focused workflows to ensure code quality and security:

## 1. PR Checks (ci.yml)
- Runs on every pull request
- Performs linting and testing
- Uses local composite actions for consistent setup
- Includes dependency caching for faster builds

## 2. Secret scanning
- Use [GitHub secret scanning](https://docs.github.com/en/code-security/concepts/secret-security/about-secret-scanning) (repository Security tab).
- Scans entire Git history, branches, issues, and PRs for exposed credentials; alerts appear on the Security tab.

## 3. CodeQL (optional, not in default setup)
CodeQL workflow files exist in `workflows/` for reference but are not deployed by the setup scripts. To use, copy `codeql-analysis.yml` into a repo’s `.github/workflows/` manually.

## Setup Required

### GitHub Token
- Workflows use the default `github.token` - no PAT_TOKEN needed
- All dependencies are public and accessible without additional authentication
