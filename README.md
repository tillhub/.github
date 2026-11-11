# tillhub/.github

Organization-wide defaults for every repository in the `tillhub` GitHub organization.

GitHub uses the files here for any repository that does not have its own file of the same type. This repository has to be public for that to work. It holds no internal repository names, credentials or customer data, and it must stay that way.

## Pull request template

[`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) pre-fills the description of every new pull request in a repository without a template of its own.

It has six sections to fill in, an optional diagram section and a checklist:

| Section | What to write |
|---|---|
| Jira Ticket | A link to the ticket, for example `[UNTIL-1234](https://unz.atlassian.net/browse/UNTIL-1234)`. |
| Summary | What the PR does and why, in two to four sentences or bullets. |
| Changes | One bullet per meaningful change, naming the components, services or modules affected. |
| User Journey / Data Flow (optional) | A Mermaid diagram of the user journey or data flow, when it helps reviewers follow the change. Delete the section if it does not apply. |
| Acceptance Criteria Coverage | The ticket's acceptance criteria, ticked where this PR covers them. Write "N/A" for purely technical work. |
| Test Plan | What you ran and the result: commands, environment (INT/TEST), manual steps. A ticked box on its own is not evidence. |
| Risks / Rollout | Migrations, feature flags, breaking changes, how to roll back. Write "None" if there are none. |

### Pull request title

Write the title in the same format as a commit message: `type(JIRA-KEY): short description`, for example `feat(UNTIL-1234): retry failed order exports`. Without a ticket, leave out the scope, for example `chore: update code owners`.

The type is one of `feat`, `fix`, `perf`, `chore`, `refactor`, `docs`, `test`, `ci`, `build`, `style` or `revert`, in lower case.

The type matters because a squash merge of a pull request with several commits uses the title as the commit message. Repositories that release with semantic-release read the type from that commit to decide whether to publish a version, and which one. A title without a type publishes nothing in those repositories, so the change is not deployed.

### Using a different template in one repository

Add `.github/pull_request_template.md` to that repository. GitHub then uses it instead of this one. Use `##` headings for its sections, so tooling can tell them apart.

## Changing these defaults

Open a pull request against this repository. A change here affects every repository in the organization, so describe the reason in the PR.
