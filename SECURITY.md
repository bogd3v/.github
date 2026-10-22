# Security Policy

This policy applies to every repository of the organisation that has no `SECURITY.md` of its own. A repository can add a file with its own scope and contact; GitHub then shows that one instead.

## Supported versions

Only the latest release line, and the default branch, receive security fixes. Older releases, other branches and older commits don't. If you run an older version, upgrade before reporting.

## Reporting a vulnerability

Report it privately: open the repository, then **Security → Report a vulnerability**. Don't open a public issue, pull request or discussion about it.

If the repository does not offer that button, open an issue that asks for a private channel and contains no details, and a maintainer will reply.

Please include what is affected, steps to reproduce, the impact you expect, and whether it needs an account.

| Step                             | Target               |
| -------------------------------- | -------------------- |
| Acknowledge the report           | 3 days               |
| Triage and severity              | 7 days               |
| Fix for critical / high severity | 14 days after triage |
| Fix for medium / low severity    | next planned release |

You will be credited in the advisory unless you prefer otherwise.

## Scope

In scope: the code and configuration published in the repository you report against, including its workflows and container files. The scope and the security model of each project are described in that repository's `docs/security.md`, where it exists.

Report these upstream instead: vulnerabilities in third-party dependencies and in the platforms we build on belong to their own projects. If you are unsure whether the issue lives in our code or upstream, report it here and we will forward it.

Out of scope: volumetric denial of service, social engineering, reports from automated scanners without a demonstrated impact, missing headers with no exploit, and self-XSS.

## Testing rules

- Test against your own instance, never against a site you do not run.
- Don't run automated scanners or load tests against anyone else's instance.
- Don't access, change or delete data that isn't yours. If you reach real user data, stop and report.

Good-faith research that follows these rules won't be pursued.

## Dependencies

Dependabot opens grouped minor and patch updates weekly. Major versions are upgraded by hand after testing, and an alert that cannot be fixed yet is written down with the reason the risk is accepted.
