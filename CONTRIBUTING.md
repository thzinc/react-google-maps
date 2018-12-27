# Contributing

We are committed to fostering an open and welcoming environment. Please read our [code of conduct](CODE_OF_CONDUCT.md) before participating in or contributing to this project.

When contributing to this repository, we recommend discussing your feature, bug fix, or other contribution via an issue in this repository. If the change requires direct communication with the maintainers, send an email to open-source@gmvsync.com.

## Development conventions

We use `yarn` for package management, along with its [`yarn.lock`](yarn.lock) file. When updating dependencies, please ensure that the lock file is updated as well.

This project uses code generation templates to stay in sync with the Google Maps API. The templates in [`src/macros/**/*.jsx`](src/macros) are compiled using the Google Maps API documentation into [`src/components/**/*.jsx`](src/components). In order to change this code, make changes to the file in `src/macros`, then run the `build:src` target.

The documentation is generated using [React Styleguidist](https://github.com/styleguidist/react-styleguidist) using Markdown files in [`src/**/*.md`](src) and compiled to [`docs`](docs). To update the files in `docs`, make changes to the Markdown files in `src`, then run the `styleguide:build` target.

It is not necessary to manually change the version number in [`package.json`](package.json). This will be handled when the package is published.

The NPM package is bundled using Webpack using files in [`src`](src) into [`lib`](lib). Files in the `lib` folder should not be changed manually. Typically, the automated build script will run the `semantic-release` target to generate files in `lib` and publish the package to NPM.

## Pull Request Process

1. Fork this repository
2. Make the changes as you wish
3. Submit a pull request back to this repository with a reference to the issue
4. Ensure your pull request message follows the [commit message format][commit-message-format]
    * All pull requests will be squashed prior to merging

### Process for Maintainers

1. Ensure that at least two maintainer reviewers have reviewed and approved the pull request
2. Ensure that pull requests pass all applicable tests and successfully build the project
3. Merge the pull request, and if applicable, clean up any merged branch
    * **Always** squash and merge
    * If necessary, reformat the commit message to follow the [commit message format][commit-message-format]
    * Include `thanks to @commitAuthor` in the message
    * Include `closes #pr-number, #issue-number` in the message, if applicable

[commit-message-format]: (https://github.com/semantic-release/semantic-release#commit-message-format)