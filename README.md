# capability-ci-caller

Test repository for validating that environment protection rules in the caller repo trigger when a reusable workflow in another repo declares `environment:`.

## Setup

1. Create a `production` environment in Settings > Environments
2. Add required reviewers to the `production` environment
3. Trigger the Release workflow via workflow_dispatch

## Workflows

- `release.yml` — Calls callee's release workflow with `environment: production`
- `security-scan.yml` — Calls callee's security scan workflow
- `example.yml` — Dummy CI workflow
