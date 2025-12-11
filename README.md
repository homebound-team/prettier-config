# @homebound/prettier-config

Shared Prettier configuration for Homebound projects.

## Installation

```bash
yarn add -D @homebound/prettier-config prettier
```

## Usage

Add to your `package.json`:

```json
{
  "prettier": "@homebound/prettier-config"
}
```

### Extending the config

To override settings, create a `.prettierrc.js` file:

```js
const homeboundConfig = require("@homebound/prettier-config");

module.exports = {
  ...homeboundConfig,
  // your overrides here
};
```

## Configuration

This config includes:

- `trailingComma: "all"`
- `printWidth: 120`
- [prettier-plugin-organize-imports](https://github.com/simonhaenisch/prettier-plugin-organize-imports) for automatic import sorting

## CI Integration

Add a check step to your CI:

```bash
prettier --check .
```

Or format all files:

```bash
prettier --write .
```
