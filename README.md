This repo aims at setting up a quick example of how you can properly keep a commit message convention and tools to enforce the messages. These tools also help generate a changelog very easily from these nicely crafted commit messages.

## Getting Started

First ensure you have Node installed.

Install local node modules: `npm install`.

Install [`commitizen`](https://github.com/commitizen/cz-cli) - `npm install -g commitizen`.

This will set you up for following a [commit message convention](https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#heading=h.t7ifoyph8bd3) (linked is the commit message convention for AngularJS).

## Why?

This aims at enforcing commit messages so we get beautiful easy to read [changelogs](./CHANGELOG.md)!

### The what

* [`commitizen`](https://github.com/commitizen/cz-cli) - prompts to fill out any required commit fields at commit time
* [`cz-conventional-changelog`](https://github.com/commitizen/cz-conventional-changelog) - commitizen adapter for the angular preset of conventional-changelog
* [`Husky`](https://github.com/typicode/husky) - running git hooks from npm made easy
* [`validate-commit-msg`](https://github.com/kentcdodds/validate-commit-msg) - git hooks to validate git commit messages based on convention(s)

### The How

If you type `git cz`, you will be prompted with steps to guide you along to crafting a nice commit message that follows the convention.

If you do not, there will be git hooks that run (via the npm run script `commitmsg` that runs `validate-commit-msg`) and be alerted with a warning to correct your commit message.

### The Changelog

To generate the changelog, type `npm run changelog`, and [view the changelog](./CHANGELOG.md).

Enjoy!
