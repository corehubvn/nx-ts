# Codehub

## Code Convention

This repository uses [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) for commit messages. This allows for automatic changelog generation and semantic versioning.

The commit messages are validated using [husky](https://typicode.github.io/husky/#/) and [lint-staged](https://github.com/lint-staged/lint-staged), are linted using [commitlint](https://commitlint.js.org/#/), and are formatted using [commitizen](https://github.com/commitizen/cz-cli).

There are 3 Git hooks that are used to enforce the commit convention:

- `pre-commit` - Runs `lint-staged` to fix lint errors and format files that are staged for commit automatically.
- `commit-msg` - Runs `commitlint` to validate commit messages.
- `prepare-commit-msg` - Runs `commitizen` to format commit messages.

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
  style:    Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
  refactor: A code change that neither fixes a bug nor adds a feature
  perf:     A code change that improves performance
  test:     Adding missing tests or correcting existing tests
(Move up and down to reveal more choices)
```

If you want to skip the prompts, you can run `git commit -m "your commit message"`. This will skip the `commitlint` and `commitizen` checks.

If you want to skip the commitlint check, but still use commitizen, you can run `npm run commit -- --no-verify`.

If you want to skip the commitizen check, but still use commitlint, you can run `git commit -m "your commit message" --no-verify`.
