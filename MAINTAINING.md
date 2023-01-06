# Maintaining

> This guide is intended for maintainers (anybody with commit access).

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Code of Conduct](#code-of-conduct)
- [Installation](#installation)
- [Local Development](#local-development)
  - [Testing](#testing)
  - [NPM commands](#npm-commands)
- [FAQ](#faq)
  - [Q: How to manually run githooks triggers](#q-how-to-manually-run-githooks-triggers)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Code of Conduct

Please make sure you're familiar with and follow the [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## Installation

1.  **Clone the repo**

    ```bash
    git clone git@github.com:okayd/.github.git
    ```

1.  **Navigate into the site’s directory**

    ```bash
    cd .github/
    ```

1.  **Install dependencies**

    ```bash
    npm install
    ```

## Local Development

After `npm` has installed the needed dependencies, `lefthook` will install git-hooks which will trigger various formatting and linting commands on commit.

### Testing

To verify that the content is correctly formatted simply run the `test` script:

```bash
npm test

#OR

npm run test
```

### NPM commands

| Command                       | Description                                                        |
| ----------------------------- | ------------------------------------------------------------------ |
| `npm run format`              | Runs all project formatters (will alter files)                     |
| `npm run format:doctoc`       | Run DocToc formatters on .md files                                 |
| `npm run format:package-json` | Run 'package.json' formatter                                       |
| `npm run format:prettier`     | Run Prettier                                                       |
| `npm run lint`                | Run all project linters                                            |
| `npm run lint:markdown`       | Run Markdown linter                                                |
| `npm run lint:package-json`   | Run package.json linter                                            |
| `npm run prepare`             | Command automatically run by NPM at install, installs [_lefthook_] |
| `npm run test`                | Run all linters - ⚠️ _used by CI to validate builds_ ⚠️            |

## FAQ

### Q: How to manually run githooks triggers

You can manually run _lefthook_ triggers via:

```bash
lefthook run pre-commit
```
