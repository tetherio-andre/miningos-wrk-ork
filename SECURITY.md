# Security Workflows

This repository includes several security-focused workflows to ensure code quality and security:

## 1. PR Checks (ci.yml)
- Runs on every pull request
- Performs linting and testing
- Uses local composite actions for consistent setup
- Includes dependency caching for faster builds

## 2. Secrets Scanning (git-secrets action)
- Runs as part of the CI workflow
- Uses git-secrets to detect committed credentials
- Prevents sensitive information from entering the repository

## 3. CodeQL Analysis (codeql-analysis.yml)
- Runs nightly at 2 AM UTC
- Analyzes JavaScript code for:
  - Security vulnerabilities
  - Code quality issues
  - Logic bugs
- Results appear in GitHub Security tab

## Setup Required

### GitHub Token
- Workflows use the default `github.token` - no PAT_TOKEN needed
- All dependencies are public and accessible without additional authentication
