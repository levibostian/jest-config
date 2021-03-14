# jest-config

Opinionated jest config for my projects. 

# Usage 

* Install config file:

```
npm install --D @levibostian/jest-config
```

If you need to set multiple `preset` options in Jest (example if you are using `ts-jest`), you need to install those dependencies yourself:

```
npm install --D ts-jest
```

* In your `jest.config.js` file, setup Jest to use the present. The code sample below allows you to use 2 preset options for Jest. Jest only allows 1 string for `preset` in the jest config file so we do a manual merge instead. 

```js
/* eslint-disable */

const tsPreset = require("ts-jest/jest-preset")
const customPreset = require("@levibostian/jest-config/jest-preset")

// If you want to override any settings, feel free! This is just an object like any other in a jest config file. 
module.exports = {
  ...tsPreset,
  ...customPreset  
}
```

*Note: This project is currently setup with only 1 config file: `jest-preset.js`. I write all of my projects in Typescript with `tsc` with the same set of defaults. In the future, if I decide to make another configuration for something like Javascript, I may create a new jest preset and you will need to use a long form to find this config. Something like this: `./node_modules/@levibostian/jest-config/javascript/node.js`*

> [Learn more](https://jestjs.io/docs/configuration#preset-string) about sharable configurations for Jest.

# Contributing 

I am always open to collaboration, questions, and help on projects. However, this project is opinionated for projects that I develop. I may not accept pull requests into this project. 