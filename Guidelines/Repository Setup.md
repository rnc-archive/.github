# Repository Setup

// TODO - will be discussed via PRs

## Code styling

All code in community repositories should follow the same standards. This is managed by the [community ESLint config](https://www.npmjs.com/package/@react-native-community/eslint-config) and a standard [Prettier](https://prettier.io) config. Using this allows us to keep all of the code style consistent across repositories without duplicate configuration.

To set this up run:

`yarn add --dev @react-native-community/eslint-config eslint prettier`

Create a `.eslintrc.js` at the root of your repository with this content:

```javascript
module.exports = { extends: "@react-native-community" };
```

Create a `.prettierrc` file at the root of the repository with this content:

```json
{
  "requirePragma": true,
  "singleQuote": true,
  "trailingComma": "all",
  "bracketSpacing": false,
  "jsxBracketSameLine": true
}
```

You can then run ESLint checks against your code using a command such as:

`yarn eslint 'js/**/*.js'`

It is recommended that you add this command to your `scripts` in your `package.json` like this:

```
"scripts": {
  ...
  "validate:eslint": "eslint 'js/**/*.js' 'example/**/*.js'",
  ...
}
```

## Changelog

For each published project, there should be a `CHANGELOG.md` file in the root directory with a history of noteworthy changes. Please follow the [keep a changelog](https://keepachangelog.com/en/1.0.0/) format for this file, but feel free to use tools like `semantic-release` or `conventional-changelog` to help. Strive to have the changelog published as part of your release process.

The changelog is a great place to recognize code contributors. For that reason, consider attributing changes to their authors. However, beware of feeling pressure to list all changes in the changelog. It should be a curated view. For example don't list refactoring or CI changes, because they do not impact your users.

For monorepos, we suggest keeping separate changelogs for each module that users would add as a dependency. Internal dependencies that you do not expect to be adopted may or may not need a changelog; you may find it beneficial to keep one for your fellow maintainers in complicated systems.

Also, we suggest linking to your changelog in any GitHub releases descriptions rather than embedding the content. The changelog is a living document, and maintaining the same content across multiple places can be cumbersome.

## NPM

## Tagging
