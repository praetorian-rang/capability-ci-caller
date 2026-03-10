# capability-ci-caller

Test repository simulating a consumer repo (like Trajan) that calls reusable workflows from capability-ci-callee.

## Purpose

Validates that:
1. Environment protection rules in THIS repo trigger when the callee's reusable workflow runs
2. The security scan workflow runs correctly via reusable workflow call

## Setup required

1. Create a `production` environment in this repo's Settings > Environments
2. Add required reviewers to the `production` environment
3. Trigger the Release workflow via workflow_dispatch to test

## Workflows

- `release.yml` — Calls callee's release workflow with `environment: production`
- `security-scan.yml` — Calls callee's security scan workflow
- `example.yml` — Dummy workflow so Trajan has something to scan
