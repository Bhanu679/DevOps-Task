# Gitleaks

```
┌─○───┐
│ │╲  │
│ │ ○ │
│ ○ ░ │
└─░───┘
```

[license]: ./LICENSE
[badge-license]: https://img.shields.io/github/license/gitleaks/gitleaks.svg
[go-docs-badge]: https://pkg.go.dev/badge/github.com/gitleaks/gitleaks/v8?status
[go-docs]: https://pkg.go.dev/github.com/zricethezav/gitleaks/v8
[badge-build]: https://github.com/gitleaks/gitleaks/actions/workflows/test.yml/badge.svg
[build]: https://github.com/gitleaks/gitleaks/actions/workflows/test.yml
[go-report-card-badge]: https://goreportcard.com/badge/github.com/gitleaks/gitleaks/v8
[go-report-card]: https://goreportcard.com/report/github.com/gitleaks/gitleaks/v8
[dockerhub]: https://hub.docker.com/r/zricethezav/gitleaks
[dockerhub-badge]: https://img.shields.io/docker/pulls/zricethezav/gitleaks.svg
# Task 15 – Detect Secrets with Gitleaks

## Objective
Detect secrets in a Git repository using Gitleaks, remove the secrets, and verify that the repository is clean.

## Tools Used
- Git
- Gitleaks
- Ubuntu
- GitHub

## Steps Performed

1. Installed Gitleaks.
2. Created a Git repository.
3. Added a sample secret for testing.
4. Ran Gitleaks to detect the secret.
5. Generated a scan report.
6. Removed the secret from the repository.
7. Re-ran Gitleaks to verify that no secrets remained.

## Commands Used

```bash
git init
git add .
git commit -m "Add test secret"
gitleaks detect
gitleaks dir .
```

## Result

- Gitleaks successfully detected the secret.
- The secret was removed.
- The repository was scanned again and confirmed to be free of secrets.
