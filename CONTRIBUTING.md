# Contributing

:raised_hands::tada: First off all, thanks for taking the time to contribute! :tada::raised_hands:

The following is a set of guidelines for contributing to @material-ui/pickers. The purpose of these
guidelines is to maintain a high quality of code _and_ traceability. Please respect these
guidelines.

## Setting up

Please make sure that we are using `develop` branch for active development. So your branches must be created from _develop_ and not from the ~~master~~. Here is a short step-by-step guide how to get started

1. Fork the @material-ui/pickers repository on Github
2. Clone your fork to your local machine `git clone git@github.com:<yourname>/@material-ui/pickers.git`
3. Checkout develop `git checkout develop`
4. Create a branch `git checkout -b feature/my-topic-branch`
5. Make your changes, lint, run tests, then push to to GitHub with `git push --set-upstream origin my-topic-branch`.
6. Visit GitHub and make your pull request.

If you have an existing local repository, please update it before you start, to minimise the chance of merge conflicts.

```sh
Ugit remote add upstream git@github.com:mui-org/@material-ui/pickers.git
git checkout develop
git pull upstream develop
git checkout -b my-topic-branch
```

## Dev environment

We are using lerna for development environment so it should be enough to make

```sh
npm install
npm start
```

To start development environment and be sure the `lib` folder is linked properly to the `docs` and your changes will be applied to the docs website. If you faced some problems with symlinking please do the following:

```sh
npx lerna clean
npx lerna bootstrap
```

## General

This repository use tests and a linter as automatic tools to maintain the quality of the code.
These two tasks are run locally on your machine before every commit (as a pre-commit git hook),
if any test fail or the linter gives an error the commit will not be created. They are also run on
a Travis CI machine when you create a pull request, and the PR will not be merged unless Travis
says all tests and the linting pass.

## Git Commit Messages

- Use the imperative mood ("Move pointer to..." not "Moves pointer to...")
  - Think of it as you are _commanding_ what your commit is doing
  - Git itself uses the imperative whenever it creates a commit on your behalf, so it makes sense
    for you to use it too
- Use the body to explain _what_ and _why_
  - If the commit is non-trivial, please provide more detailed information in the commit body
    message
  - _How_ you made the change is visible in the code and is therefore rarely necessary to include
    in the commit body message, but _why_ you made the change is often harder to guess and is
    therefore useful to include in the commit body message

[Here's a nice blog post on how to write great git messages.](http://chris.beams.io/posts/git-commit/)

## Pull Requests

- Follow the current code style
- Write tests for your changes
- Document your changes in the README if it's needed
- End files with a newline
- There's no need to create a new build for each pull request, we (the maintainers) do this when we
  release a new version

## Issues

- Please be descriptive when you fill in the issue template, this will greatly help us maintainers
  in helping you which will lead to your issue being resolved faster
- Feature requests are very welcomed, but not every feature that is requested can be guaranteed
  to be implemented
