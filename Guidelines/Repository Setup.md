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
  "jsxBracketSameLine": true,
  "parser": "flow"
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

## NPM

## Tagging
