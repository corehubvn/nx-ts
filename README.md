# NX-TS

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

This repository uses [Nx](https://nx.dev) as a workspace manager. Nx is a set of extensible dev tools for monorepos, which helps you develop like Google, Facebook, and Microsoft. We create **a minimal, integrated repo style with typescript preset** as a starting point for any TypeScript-based projects.

```bash
npx create-nx-workspace@latest nx-ts --preset=ts
```

This repository also uses [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#summary) as a commit message convention. Conventional Commits is a specification for adding human and machine readable meaning to commit messages. Using the convention leads to more readable messages that are easy to follow when looking through the project history. Also, it enables generating CHANGELOGs automatically.

## What is included?

- [Nx](https://nx.dev) as a workspace manager
- [TypeScript](https://www.typescriptlang.org/) as a strongly typed programming language that builds on JavaScript, giving you better tooling at any scale.
- [Prettier](https://prettier.io/) as a code formatter.
- [Commitlint](https://commitlint.js.org/#/) as a commit message linter.
- [Commitizen](https://github.com/commitizen/cz-cli) as a commit message formatter.
- [Husky](https://typicode.github.io/husky/#/) as a Git hook.
- [Lint-staged](https://github.com/lint-staged/lint-staged) as a pre-commit linter.

### Convention

There are 3 Git hooks that are used to enforce the convention:

- `pre-commit` - Automatically runs `lint-staged` to fix lint errors and format files that are staged for commit.
- `commit-msg` - Automatically runs `commitlint` to validate commit messages.
- `prepare-commit-msg` - Automatically runs `commitizen` to format commit messages.

## Getting Started

You could quickly create a new repo from this template by clicking the `Use this template` button on the top right corner of this page.
See more: [Creating a repository from a template](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template)

To commit, run the below command:

```bash
# Using git
git commit

# Or
npm run commit
```

Follow the prompts to create your commit message. This will ensure that the commit message is formatted correctly.

```bash
? Select the type of change that you're committing: (Use arrow keys)
❯ feat:     A new feature
  fix:      A bug fix
  docs:     Documentation only changes
  style:    Changes that do not affect the meaning of the code (white space, formatting, missing semi-colons, etc)
  refactor: A code change that neither fixes a bug nor adds a feature
  perf:     A code change that improves performance
  test:     Adding missing tests or correcting existing tests
(Move up and down to reveal more choices)
```

Happy coding! 🎉🙌
