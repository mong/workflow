# Our git workflow

We will use a workflow similar to [GitHub flow](https://guides.github.com/introduction/flow/).

Few of us are experts in git, so we have to keep the workflow simple.
Thus, *no* complicated branching scheme such as [git-flow](https://nvie.com/posts/a-successful-git-branching-model/).

### Master is king

We only have one long-lived branch, which is `master`.

### Use PR

All changes goes into `master` through **pull requests (PR)** and never by direct commits.

- The PR is automatically tested (CI) and reviewed by one colleague before it is merged into `master`.
- The PR goes mainly into `master` through **Squash and merge**, to keep the git history linear.
- Each PR should be small and simple, to make it easier to review.
- Each PR is *not* a mix of several new features.



### Use SemVer

We are using [Semantic Versioning](https://semver.org/) to versioning our softwares. 


## In more details

When we want to add a new feature or fix a bug, we

1. make a branch out of `master`

```sh
git checkout master # make sure we are on master
git pull --rebase # make sure master is up-to-date
git checkout -b <branchname> # make a new branch
```

2. do the coding
3. commit changes and push them up to github

```sh
git commit -m 'Clear and concise commit message' # commit changes
git push -u origin <branchname> # push changes to github
```

4. go to github, open a pull request, wait for all the tests to pass and let someone else look at the code.
5. do some more coding and commits

```sh
git commit -m 'Clear and concise commit message 2'
git commit -m 'Clear and concise commit message 3'
git pull --rebase # just in case someone else did some changes to this branch
git push # push to github (only use "-u origin <branchname>" for the first push)
```
