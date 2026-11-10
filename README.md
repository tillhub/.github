# tillhub/.github

Organization-wide defaults for every repository in the `tillhub` GitHub organization.

GitHub uses the files here for any repository that does not have its own file of the same type. This repository has to be public for that to work. It holds no internal repository names, credentials or customer data, and it must stay that way.

## Pull request template

[`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) pre-fills the description of every new pull request in a repository without a template of its own.

It has four sections to fill in, plus a checklist:

| Section | What to write |
|---|---|
| Summary | Two to four sentences on what the PR does and why, with the Jira ticket link. |
| Changes | One bullet per meaningful change. |
| Testing | How you verified it: commands, manual steps, screenshots, a CI run link. |
| Risks / Rollout | Migrations, feature flags, breaking changes, how to roll back. Write "None" if there are none. |

Start the PR title with the Jira key, for example `UNTIL-1234: Retry failed order exports`.

### Using a different template in one repository

Add `.github/pull_request_template.md` to that repository. GitHub then uses it instead of this one. Use `##` headings for its sections, so tooling can tell them apart.

## Changing these defaults

Open a pull request against this repository. A change here affects every repository in the organization, so describe the reason in the PR.
