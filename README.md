# Node.JS TypeScript Library Template

This is a template repository meant to be used as a starting point for new
[**`Node.JS`**][nodejs-url] projects written in
[**`TypeScript`**][typescript-url].

As this is a highly opinionated template, many tools are included and
pre-configured with sane and strict defaults to enforce a standard level of
code quality and a consistent style across projects.

With this in mind, feel free to edit the various config files to your liking.

## Prerequisites

To view static documentation and coverage reports,
[**`http-server`**][http-server-url] is recommended; it is included as a
development dependency for the **`serve:*`** commands, but for manual CLI
usage, install it with **`npm i -g http-server`**.

## Setup

[**`pnpm`**][pnpm-url] is used as the package manager; install it with
**`npm i -g pnpm`** if you do not already have it.

Then, to get started, simply install dependencies with **`pnpm i`**.

### Building Sources and Documentation

Three npm scripts are provided to build
[**`TypeScript`**][typescript-url] sources and generate documentation with
[**`TypeDoc`**][typedoc-url]:

- **`build`** -- runs both **`build:ts`** and **`build:docs`**.
- **`build:ts`** -- builds [**`TypeScript`**][typescript-url] sources from
    [**`./src`**](/src) to native JavaScript files in [**`./dist`**](/dist).
- **`build:docs`** -- builds documentation with
    [**`TypeDoc`**][typedoc-url] in [**`./docs`**](/docs). Both
    [**`LICENSE.md`**](/LICENSE.md) and [**`CHANGELOG.md`**](/CHANGELOG.md) are
    copied into [**`./docs`**](/docs).

#### Viewing Documentation Site

After building the static HTML documentation with **`build:docs`**,
run `pnpm serve:docs` or `http-server docs` and navigate to
[**`localhost:8080`**](http://localhost:8080).

### Deploy Documentation On GitHub Pages

To enable Github Pages, access the repository settings and configure the Pages
settings to use the `main` (or `master`) branch and the `./docs` folder.

### Testing

**Testing** is done with [**`mocha`**][mocha-url] and [**`chai`**][chai-url].
[**`nyc`**][nyc-url] is used to generate coverage reports. The following npm
scripts are provided:

- **`test`** -- runs mocha on all TypeScript sources
- **`test:coverage`** -- like **`test`** but runs
    [**`nyc`**][nyc-url] to generate an HTML coverage report in *`/coverage`*.
- **`test:watch`** -- runs [**`nyc`**][nyc-url] and [**`mocha`**][mocha-url]
    continuously, re-running tests when any sources change.

#### Viewing Test Coverage Report

After generating an HTML coverage report with **`test:coverage`**, view it by
running either **`serve:coverage`** or `http-server ./coverage` and navigating
to [**`localhost:8080`**](http://localhost:8080).

### Linting

**Linting** is provided by [**`ESLint`**][eslint-url] and
[**`markdownlint`**][markdownlint-url]. The following npm scripts are provided:

- **`lint:eslint`** -- runs [**`ESLint`**][eslint-url] on
    [**`./package.json`**](/package.json) and [**`./src/**/*`**](/src) and
    prints any errors.
- **`lint:markdownlint`** -- runs
    [**`markdownlint`**][markdownlint-url] on [**`README.md`**](/README.md)
    and prints any errors.
- **`lint:eslint:fix`** -- like **`lint:eslint`** but automatically fixes
    linter errors where possible.
- **`lint:markdownlint:fix`** -- like **`lint:markdownlint`** but automatically
    fixes linter errors where possible.

- **`lint`** -- runs both **`lint:eslint`** and **`lint:markdownlint`**.
- **`lint:fix`** -- runs both **`lint:eslint:fix`** and
    **`lint:markdownlint:fix`**

#### [**`ESLint`**][eslint-url] Config & Plugins

A strict [**`ESLint`**][eslint-url] config is provided with many
plugins, the full list is below:

- [**`eslint-plugin-chai-expect`**][ep-chai-expect-url] --
    [**`ESLint`**][eslint-url] plugin that checks for common chai.js expect() mistakes.
- [**`eslint-plugin-eslint-comments`**][ep-eslint-comments-url] --
    [**`ESLint`**][eslint-url] rules for JavaScript comments.
- [**`eslint-plugin-github`**][ep-github-url] -- An opinionated collection of
    [**`ESLint`**][eslint-url] rules used by GitHub.
- [**`eslint-plugin-immutable`**][ep-immutable-url] -- This is an
    [**`ESLint`**][eslint-url] plugin to disable all mutation in JavaScript.
- [**`eslint-plugin-json-format`**][ep-json-format-url] --
    [**`ESLint`**][eslint-url] plugin for JSON files.
- [**`eslint-plugin-jsonc`**][ep-jsonc-url] -- This
    [**`ESLint`**][eslint-url] plugin provides linting rules relate to better
    ways to help you avoid problems when using [**`JSON`**][json-url],
    [**`JSONC`**][jsonc-url] and [**`JSON5`**][json5-url].
- [**`eslint-plugin-lodash`**][ep-lodash-url] -- Lodash-specific linting rules
    for [**`ESLint`**][eslint-url].
- [**`eslint-plugin-mocha`**][ep-mocha-url] -- [**`ESLint`**][eslint-url]
    rules for mocha.
- [**`eslint-plugin-no-secrets`**][ep-no-secrets-url] -- An
    [**`ESLint`**][eslint-url] rule that searches for potential secrets/keys in
    code and JSON files.
- [**`eslint-plugin-optimize-regex`**][ep-optimize-regex-url] -- Optimize regex literals.
- [**`eslint-plugin-promise`**][ep-promise-url] -- Enforce best practices for
    JavaScript promises.
- [**`eslint-plugin-pure`**][ep-pure-url] -- Enforce rules to make your code purely
    functional by disallowing some language constructs.
- [**`eslint-plugin-regexp`**][ep-regexp-url] -- An [**`ESLint`**][eslint-url]
    plugin for finding RegExp mistakes and RegExp style guide violations.
- [**`eslint-plugin-sonarjs`**][ep-sonarjs-url] -- [**`SonarJS`**][sonarjs-url]
    rules for [**`ESLint`**][eslint-url] to help developers produce
    [**`Clean Code`**][clean-code-url] by detecting bugs and suspicious patterns.
- [**`eslint-plugin-switch-case`**][ep-switch-case-url] -- Switch-case-specific
    linting rules for [**`ESLint`**][eslint-url].
- [**`eslint-plugin-tsdoc`**][ep-tsdoc-url] -- This [**`ESLint`**][eslint-url]
    plugin provides a rule for validating that TypeScript doc comments conform
    to the [**`TSDoc`**][tsdoc-url] specification.
- [**`eslint-plugin-unicorn`**][ep-unicorn-url] -- More than 100 powerful
    [**`ESLint`**][eslint-url] rules
- [**`eslint-plugin-write-good-comments`**][ep-write-good-comments-url] -- Enforce
    good writing style in your comments.

### Formatting

[**`Prettier`**][prettier-url] is included to automatically format sources in
order to enforce a consistent and standardized code style. It automatically
verifies that sources conform to the standard style as part of the
[**`Husky`**][husky-url] **pre-commit** hook.

Two scripts are provided:

- **`format`** -- runs [**`Prettier`**][prettier-url] and formats files
    in-place.
- **`format:check`** -- runs [**`Prettier`**][prettier-url] in **check** mode,
    reporting any files that do not match the standard style. To fix any
    reported issues, use the **`format`** script.

### [**`Husky`**][husky-url]

> [**`Husky`**][husky-url] hooks are automatically
> installed when `pnpm i` is run.

[**`Husky`**][husky-url] is included and configured
with two commit hooks:

- **pre-commit**: runs
    [**`lint-staged`**][lint-staged-url] which runs
    [**`markdownlint`**][markdownlint-url] and [**`ESLint`**][eslint-url] on
    [*README.md*](/README.md) and project sources in [**`src/**`**](/src).
- **commit-msg**: runs [**`commitlint`**][commitlint-url] on commit messages
    to enforce the [**`conventional commit`**][conventional-commit-url]
    standard.

## Creating A New Project

To start a new project with this repository as a template, clone it and delete
the **.git** folder, then run **`git init .`** to start a new git project and
commit history.

Then, configure [**`package.json`**](/package.json) with your project name,
description, keywords, repository URL, version number, and any other details
you wish to change.

Add code to [**`./src`**](/src), and it will be built to [**`./dist`**](/dist).
[**`./src/index.ts`**](/src/index.ts) will be built as the project entry point
at [**`./dist/index.js`**](/dist/index.js) as defined in the
[**`manifest`**](/package.json).

### CI

After each push to the **`main`** branch, the
[**`CI Github Action`**](/.github/workflows/ci.yml) runs to ensure all checks
pass.

### Releasing

To release a new version of your package, the **`release`** npm script is
provided. It does the following:

- runs **`pnpm format:check`**
- runs **`pnpm lint`**
- runs **`pnpm test`**
- runs **`pnpm build`**,
- runs **`git add docs`**
- Updates the [**`package.json`**](/package.json) version appropriately based
    on the commits made since the last release.
- Updates the [**`CHANGELOG.md`**](/CHANGELOG.md).
- Commits all changes and tags the commit with the new version number.
- Pushes **`main`** with the new **tag** to **origin**.
- Triggers the [**`NPM Publish`**](/.github/workflows/publish.yml) workflow to
    automatically publish the new version on the **NPM Registry**.

Available scripts are:

- `pnpm docs`: generate HTML documentation in `./docs`
- `test`: run mocha on all tests in `./src/tests`
- `test:coverage`: run mocha and generate a coverage report in `./coverage`
- `build`: build to JS in `./dist`
- `lint`: run `eslint` on all files in `./src`
- `update-deps`: update all dependencies
- `update-version`: updates the CHANGELOG.md, bumps the version, commits & tags
- `release`: lints, tests, builds, generates docs, runs `update-version` and
  pushes.

### Publishing

Publishing to the [**`NPM Registry`**][npm-registry-url] is done automatically
with a [**`NPM Publish Github Action`**](./.github/workflows/npm-publish.yml)
that runs when a new tag is pushed. For this to work, you must add a secret
named **`NPM_TOKEN`** to the repository settings.

## Release History

See [**`CHANGELOG.md`**](./CHANGELOG.md) for more information.

## License

Distributed under the **MIT** license. See [**`LICENSE.md`**](./LICENSE.md)
for more information.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

[eslint-url]: https://eslint.org/
[sonarjs-url]: https://github.com/SonarSource/SonarJS
[clean-code-url]: https://www.sonarsource.com/solutions/clean-code/
[json-url]: https://www.json.org/json-en.html
[jsonc-url]: https://github.com/microsoft/node-jsonc-parser
[json5-url]: https://json5.org/
[tsdoc-url]: https://tsdoc.org/
[typescript-url]: https://www.typescriptlang.org/
[nodejs-url]: https://nodejs.org/en
[http-server-url]: https://www.npmjs.com/package/http-server
[pnpm-url]: https://pnpm.io/
[typedoc-url]: https://typedoc.org/
[mocha-url]: https://mochajs.org/
[chai-url]: https://www.chaijs.com/
[nyc-url]: https://github.com/istanbuljs/nyc
[markdownlint-url]: https://github.com/markdownlint/markdownlint
[prettier-url]: https://prettier.io/
[husky-url]: https://typicode.github.io/husky/
[lint-staged-url]: https://github.com/lint-staged/lint-staged
[commitlint-url]: https://commitlint.js.org/
[conventional-commit-url]: https://www.conventionalcommits.org/
[npm-registry-url]: http://npmjs.com/

[ep-chai-expect-url]: https://npmjs.com/package/eslint-plugin-chai-expect
[ep-eslint-comments-url]: https://npmjs.com/package/eslint-plugin-eslint-comments
[ep-github-url]: https://npmjs.com/package/eslint-plugin-github
[ep-immutable-url]: https://npmjs.com/package/eslint-plugin-immutable
[ep-json-format-url]: https://npmjs.com/package/eslint-plugin-json-format
[ep-jsonc-url]: https://npmjs.com/package/eslint-plugin-jsonc
[ep-lodash-url]: https://npmjs.com/package/eslint-plugin-lodash
[ep-mocha-url]: https://npmjs.com/package/eslint-plugin-mocha
[ep-no-secrets-url]: https://npmjs.com/package/eslint-plugin-no-secrets
[ep-optimize-regex-url]: https://npmjs.com/package/eslint-plugin-optimize-regex
[ep-promise-url]: https://npmjs.com/package/eslint-plugin-promise
[ep-pure-url]: https://github.com/purely-functional/eslint-plugin-pure
[ep-regexp-url]: https://npmjs.com/package/eslint-plugin-regexp
[ep-sonarjs-url]: https://npmjs.com/package/eslint-plugin-sonarjs
[ep-switch-case-url]: https://npmjs.com/package/eslint-plugin-switch-case
[ep-tsdoc-url]: https://npmjs.com/package/eslint-plugin-tsdoc
[ep-unicorn-url]: https://npmjs.com/package/eslint-plugin-unicorn
[ep-write-good-comments-url]: https://npmjs.com/package/eslint-plugin-write-good-comments
