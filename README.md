# Node.JS TypeScript Library Template

[![NPM Version][npm-image]][npm-url]
[![Downloads Stats][npm-downloads]][npm-url]

This is a template repository meant to be used as a starting point for new
Node.JS projects written in TypeScript. Testing is done with
[`mocha`](https://mochajs.org/) and [`chai`](https://www.chaijs.com/).
Documentation is generated with [`TypeDoc`](https://typedoc.org/), and linting
is provided by [`ESLint`](https://eslint.org/).

## Usage

Copy the template to a new folder and initialize a new git repository with `git
init .`, then configure `package.json` with your specific project details. Add
code to `./src`, and it will be built to `./dist` which is the entry point in
the manifest by default.

### GitHub Pages

To enable Github Pages, access the repository settings and configure the Pages
settings to use the `main` (or `master`) branch and the `./docs` folder.

### Scripts

Available scripts are:

- `npm run docs`: generate HTML documentation in `./docs`
- `test`: run mocha on all tests in `./src/tests`
- `test:coverage`: run mocha and generate a coverage report in `./coverage`
- `build`: build to JS in `./dist`
- `lint`: run `eslint` on all files in `./src`
- `update-deps`: update all dependencies
- `update-version`: updates the CHANGELOG.md, bumps the version, commits & tags
- `release`: lints, tests, builds, generates docs, runs `update-version` and
  pushes.

### Publishing

Publishing to the [NPM Registry](http://npmjs.com/) is done automatically with
a [GitHub Workflow](./.github/workflows/npm-publish.yml) that runs when a new
tag is pushed. You must add an NPM auth token with publish permissions as a
secret named `npm_token`.

## Release History

See _[CHANGELOG.md](./CHANGELOG.md)_ for more information.

## License

Distributed under the **MIT** license. See [LICENSE.md](./LICENSE.md) for more
information.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

[npm-image]: https://img.shields.io/npm/v/@f3rno64/node-ts-lib-template.svg?style=flat-square
[npm-url]: https://npmjs.org/package/@f3rno64/node-ts-lib-template
[npm-downloads]: https://img.shields.io/npm/dm/@f3rno64/node-ts-lib-template.svg?style=flat-square
