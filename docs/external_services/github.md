# GitHub

This is our repository for the team on GitHub:

* [IS 7 Github team](https://github.com/orgs/cyncly-engineering/teams/ideal-spaces)

## Git Settings

Everyone that commits to git should have their username (real name, not GitHub username) / email address setup in the Git settings to easier find people to contact:  

```
git config --global user.name "Your Name"
git config --global user.email "youremail@cyncly.com"
```

To confirm or check before
```
git config --list
```

We use the `rebase` option when **pulling** changes from remote to avoid unnecessary merge commits.

This is not about [git rebase](https://git-scm.com/docs/git-rebase) but only about how to incorporate remote changes with a [git pull --rebase](https://git-scm.com/docs/git-pull#Documentation/git-pull.txt---rebasefalsetruemergespreserveinteractive)

This is what happens in IntelliJ IDEA when you do a "Git -> Update project" in the morning (`CTRL t`).

Merging a pull request into master (e.g. via GitHub) will still be a regular merge commit.

There are two ways to make this configuration permanent:
1. IntelliJ IDEA: Settings -> Version Control -> Git -> Update method: "Rebase" or when updating the project, choose `rebase ...`
1. git CLI: Update git config in home directory `~/.gitconfig`:
```
[pull]
  rebase=true
```

## Integrations


### Sentry

* Connect from Sentry to GitHub
* see our [Sentry documentation](./sentry)

### Slack

* Can notify about pull requests, commits, ...
* We use it to notify about status changes for pull requests (new, merged)

### Configuration

## GitHub Dependabot

We use the dependabot to keep dependencies for non-Kotlin projects up-to-date. 

See [Dependency Updates / Dependabot](../../tooling/dependency-update-check/#github-dependabot) for details.

## GitHub Actions

We use the [Actions](https://github.com/features/actions) to run tests or simple non-deployment tasks. The Workflows are defined under `.github/workflows` in each repository

* Actions can consist of predefined or own / scripted steps

