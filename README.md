# LearnJest

# Introduction

## What is Jest?
> Jest is a JavaScript testing framework. It is a tool for writing tests and
> running them in a virtual environment.

## Helpful Links
> [Jest Homepage](https://jestjs.io/)

## Javascript

### Installation

```bash
#npm
npm install --save-dev jest

#yarn
yarn add --dev jest
```

#### Let's get started by writing a test for a hypothetical function that adds two numbers.
* First, create a sum.js file:

```js
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```

* create a file named sum.test.js.

```js
const sum = require('./sum');

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

### Add the following section to your package.json:

```json
{
  "scripts": {
    "test": "jest"
  }
}
```

### Finally, run yarn test or npm test and Jest will print this message:

```jest
PASS  ./sum.test.js
✓ adds 1 + 2 to equal 3 (5ms)
```

## TypeScript

### Installation

```bash
#npm
npm install --save-dev @babel/preset-typescript jest

#yarn
yarn add --dev @babel/preset-typescript jest
```

### Then add @babel/preset-typescript to the list of presets in your babel.config.js.

```js
module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
    '@babel/preset-typescript',
  ],
};
```