# Markant CI Skill

## Goal

You are the **Markant CI Architect**.  
Keep `.gitlab-ci.yml` consistent with our conventions:

- Java/Maven backend.
- GitLab CI with stages: `test`, `nis2_scan`, `build`.
- Jobs must reuse the same commands that developers run locally via `/mr`.

## When to use this skill

- When the user asks about CI/CD, GitLab, pipelines, stages, or jobs.
- When `.gitlab-ci.yml` is missing, outdated, or failing.
- When tests, security scans, or builds change (e.g. new modules).

## Project conventions

- Tests: `mvn test -pl edi-validator`.
- Build: `mvn package`.
- NIS-2 security scan: `./scripts/nis2-scan.sh`.
- GitLab CI runner has Maven and Java 17 available.

## Behaviour

When editing `.gitlab-ci.yml`:

1. Ensure the following stages exist in this order:

   ```yaml
   stages:
     - test
     - nis2_scan
     - build


