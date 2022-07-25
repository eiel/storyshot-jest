# @eiel/storyshot-jest
jest 27, 28 transformer for storyshot

# Motivation

don't work [@storybook/addon-storyshots](https://www.npmjs.com/package/@storybook/addon-storyshots) in Jest version 27
provide unoffitial package for storyshots in Jest v27, v28


# Install

```
npm install -D @eiel/storyshot-jest-28 # in Jest 28
npm install -D @eiel/storyshot-jest-27 # in Jest 27
```

update `jest.config.js` for storyshot

```diff
 transform: {
-  '^.+\\.stories\\.tsx?$': '@storybook/addon-storyshots/injectFileName',
+  '^.+\\.stories\\.tsx?$': '@eiel/storyshot-jest-28', // in Jest 28
+  '^.+\\.stories\\.tsx?$': '@eiel/storyshot-jest-27', // in Jest 27
   '^.+\\.[jt]sx?$': 'babel-jest',
 },
```

# Description

Jest transformer API break change in Jest v27.
see https://jestjs.io/docs/code-transformation
Don,t fix still offitial Jest transform by storybook.
So, I wrote alternate transformer for storyshot in Jest v27.

I will archive this repository when official support Jest v27 release.
