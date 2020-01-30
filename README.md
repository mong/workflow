# Our git workflow

## Keep it simple

Few of us are experts in git, so we have to keep the workflow simple. Thus, no complicated branching scheme.

## Master is king

We only have one long-lived branch, which is `master`.

## Use PR

All changes goes into `master` through **pull requests (PR)** and never by direct commits.

The PR is automatically tested (CI) and reviewed by one colleague before it is merged into `master`.

The PR goes mainly into `master` through **Squash and merge**, to keep the git history linear.

## Use SemVer

We are using [Semantic Versioning](https://semver.org/) to versioning our softwares. 



