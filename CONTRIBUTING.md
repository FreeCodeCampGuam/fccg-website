# Contributing

## General Workflow

1. Clone the repo.
1. Cut a namespaced feature branch from origin master.
1. Make commits to your feature branch.
1. Pull Request
    - If you want to start a conversation about the feature you're working on, submit a pull request to origin master with [WIP]  prefixed.
    - If you want to submit a pull request to merge your feature branch's code into master, first make sure your feature branch is up-to-date by merging master's changes into yours.
    - Include a description of your changes.
1. Your pull request will be reviewed by another maintainer. The point of code reviews is to help keep the codebase clean and of high quality and, equally as important, to help you grow as a programmer. If your code reviewer requests you make a change you don't understand, ask them why.
1. Fix any issues raised by your code reviwer, and push your fixes.
1. Once the pull request has been reviewed, it will be merged by another member of the team. Do not merge your own commits.

## Detailed Workflow

### Cut a namespaced feature branch from master

Your branch should follow this naming convention:
  - bug/improper-API-endpoint
  - feat/login
  - refactor/callback-style-to-promises
  - doc/readme
  - test/...

This command will help you do this:

``` bash
# Creates your branch and brings you there
git checkout -b `your-branch-name`
```

### Make commits to your feature branch. 

Prefix each commit like so
  - (feat) Store user's login session to conditionally render Login Component on next visit
  - (fix) Fix inconsistent tests [Fixes #0]
  - (refactor) ...
  - (doc) ...
  - (test) ...

Make changes and commits on your branch, and make sure that you
only make changes that are relevant to this branch. If you find
yourself making unrelated changes, make a new branch for those
changes.

#### Commit Message Guidelines

- Commit messages should be written in the present tense; e.g. "Fix continuous integration script".
- The first line of your commit message should be a brief summary of what the commit changes. Aim for about 70 characters max. Remember: This is a summary, not a detailed description of everything that changed.
- If you want to explain the commit in more depth, following the first line should be a blank line and then a more detailed description of the commit. This can be as detailed as you want, so dig into details here and keep the first line short.

### Merge upstream changes into your branch

Once you are done making changes, you can begin the process of getting
your code merged into the main repo. Step 1 is to merge
changes to the master branch into yours by running this command
from your branch:

```bash
git pull origin master
```

This will start the merge process. You must commit all of your changes
before doing this. If there are no conflicts, this should prompt you to make a merge commit message.

If there are conflicting changes, git will start yelling at you part way
through the merging process. Git will pause merging to allow you to sort
out the conflicts. You do this
by checking all of the files git says have been changed in both histories
and picking the versions you want. Be aware that these changes will show
up in your pull request, so try and incorporate upstream changes as often
as possible.

### Make a pull request

Make a clear pull request from your fork and branch to the upstream master
branch, detailing exactly what changes you made and what feature this
should add. The clearer your pull request is the faster you can get
your changes incorporated into this repo.

At least one other person MUST give your changes a code review, and once
they are satisfied they will merge your changes into upstream. Alternatively,
they may have some requested changes. You should make more commits to your
branch to fix these, then follow this process again.

Once you get back here, make a comment requesting further review and
someone will look at your code again. If they like it, it will get merged,
else, just repeat again.

Thanks for contributing!

### Guidelines

1. Uphold the current code standard:
    - Keep your code [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
    - Apply the [boy scout rule](http://programmer.97things.oreilly.com/wiki/index.php/The_Boy_Scout_Rule).
    - Follow [STYLE-GUIDE.md](STYLE-GUIDE.md)
1. Run the [tests][] before submitting a pull request.
1. Tests are very, very important. Submit tests if your pull request contains
   new, testable behavior.

## Checklist:

This is just to help you organize your process

- [ ] Did I cut my work branch off of master (didn't cut new branches from existing feature brances)?
- [ ] Did I follow the correct naming convention for my branch?
- [ ] Is my branch focused on a single feature?
  - [ ] Do all of my commits directly relate to this feature?
- [ ] Did I update my branch with master's changes?
- [ ] Did I write a clear pull request message detailing what changes I made?
- [ ] Did I get a code review?
  - [ ] Did I make any requested changes from that code review?

If you follow all of these guidelines and make good changes, you should have
no problem getting your changes merged in.
