# Ways of Working

## Daily stand-up meeting

## Weekly Care Taking

### Rotation and daily assignment

### Tasks

## Live deployments are not gated by manual intervention

### Requirements to enable this

#### Every team member is responsible for the quality of the product.

#### Database changes must be backward compatible

TODO

#### Prefer to fix forward over rollback

TODO

#### We have confidence in our automated tests.

If a live deployment leads to a bug, it reveals that we are missing a test. As part of the bug fix it is essential to add a test which covers the bug and protects us from this regression to happen again.

#### We have confidence in our monitoring and alerting.

If a live deployment leads to a bug this is ideally discovered by the team itself based on the monitoring and alerting. Less good, but also possible, is that the bug is reported to the team from outside. As part of the bug fix we will check if there is a gap in our monitoring and alerting which would have alerted us about the bug as early as possible.

#### We believe blameless postmortems are an essential part of a learning culture.


## Code

### Git

* Have proper commit messages
    * guideline: [The seven rules of a great Git commit message](https://chris.beams.io/posts/git-commit/)
* Use [these git settings](../../external_services/github/#git-settings)
    * Identify yourself for your team-mates
    * Use `git pull --rebase` to avoid unnecessary merge commits 
    * Example: "CBS-111: Add tests for American Express Centurion Card"

### Style / coding convention

* [Javascript / Node.JS](../../tech/javascript/)
* [Javascript / Node.JS](../../tech/kotlin/)