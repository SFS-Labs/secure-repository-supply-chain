# Dependency updates in this folder

`minimist` was upgraded from 1.2.5 to 1.2.8 by Dependabot in
[PR #2](https://github.com/SFS-Labs/secure-repository-supply-chain/pull/2),
remediating [alert #5](https://github.com/SFS-Labs/secure-repository-supply-chain/security/dependabot/5)
(GHSA-xvch-5gv4-984h / CVE-2021-44906, prototype pollution). `package.json` now
requires `^1.2.8` and the lockfile pins 1.2.8.

This file also provides the second push that the course workflow needs:
`2-dependabot-alerts.yml` gates its `find_exercise` job on
`github.run_number != 1`, so the first run on `main` is skipped by design. The
fork lost the template's initial no-op run because Actions were disabled when it
was created, so a later push is required to reach the real check.
