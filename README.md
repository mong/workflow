# Our git workflow

We will use a workflow similar to [GitHub flow](https://guides.github.com/introduction/flow/).

## KISS (keep it simple, stupid)

Few of us are experts in git, so we have to keep the workflow simple. Thus, **no** complicated branching scheme such as [git-flow](https://nvie.com/posts/a-successful-git-branching-model/).

## Master is king

We only have one long-lived branch, which is `master`.

## Use PR

All changes goes into `master` through **pull requests (PR)** and never by direct commits.

The PR is automatically tested (CI) and reviewed by one colleague before it is merged into `master`.

The PR goes mainly into `master` through **Squash and merge**, to keep the git history linear.

## Use SemVer

We are using [Semantic Versioning](https://semver.org/) to versioning our softwares. 



