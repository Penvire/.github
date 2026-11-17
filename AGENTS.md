# Penvire .github

Organization-wide defaults: the org profile, the default security policy and the reusable Conventional Commits workflow that every repository calls.

## Repository map

```text
profile/README.md                               organization front page
SECURITY.md                                     default security policy
.github/workflows/conventional-commits.yml      reusable check (workflow_call)
.github/workflows/commits.yml                   this repository's own caller
```

## Development environment

Enter the environment with `devenv shell`, or run `direnv allow` once. It provides actionlint. Always run tools through it.

Git hooks run automatically: a commit-msg hook rejects messages that are not Conventional Commits (the same rule as CI), and actionlint checks workflow files.

Changes to `conventional-commits.yml` affect every repository at once; test the script locally against good and bad messages first.

## Rules

- Never push to `main`. Create a branch (`feat/`, `fix/` or `chore/`), push it and open a pull request. The maintainer merges.
- Pull requests are squash-merged. The PR title becomes the commit on `main`, so it must be a Conventional Commit; mark breaking changes with `!`.
- Commits are GPG-signed; `main` rejects unsigned commits.
- PR body: a one-paragraph summary, then a `## Test plan` section.

## Agent docs

- [Issue tracker](docs/agents/issue-tracker.md): GitHub Issues for `Penvire/.github`
- [Triage labels](docs/agents/triage-labels.md)
- [Domain docs](docs/agents/domain.md): where the glossary and ADRs live

## Related repositories

- `~/Projects/penvire/prod/contracts`: [penvire-contracts](https://github.com/Penvire/penvire-contracts)
- `~/Projects/penvire/prod/backend`: [penvire-backend](https://github.com/Penvire/penvire-backend)
- `~/Projects/penvire/prod/clients`: [penvire-clients](https://github.com/Penvire/penvire-clients)
- `~/Projects/penvire/prod/docs`: [penvire-docs](https://github.com/Penvire/penvire-docs), the product documentation
