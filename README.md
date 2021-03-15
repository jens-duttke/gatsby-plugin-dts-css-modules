[![npm version](https://badge.fury.io/js/gatsby-plugin-dts-css-modules.svg)](https://badge.fury.io/js/gatsby-plugin-dts-css-modules)
[![Dependency Status](https://img.shields.io/david/jens-duttke/gatsby-plugin-dts-css-modules)](https://www.npmjs.com/package/gatsby-plugin-dts-css-modules)
[![Known Vulnerabilities](https://snyk.io/test/github/jens-duttke/gatsby-plugin-dts-css-modules/badge.svg?targetFile=package.json)](https://snyk.io/test/github/jens-duttke/gatsby-plugin-dts-css-modules?targetFile=package.json)
[![npm](https://img.shields.io/npm/dm/gatsby-plugin-dts-css-modules.svg?maxAge=2592000)](https://www.npmjs.com/package/gatsby-plugin-dts-css-modules)
[![node](https://img.shields.io/node/v/gatsby-plugin-dts-css-modules)](https://www.npmjs.com/package/gatsby-plugin-dts-css-modules)
[![MIT license](https://img.shields.io/github/license/jens-duttke/gatsby-plugin-dts-css-modules.svg?style=flat)](https://opensource.org/licenses/MIT)

# gatsby-plugin-dts-css-modules

[GatsbyJS](gatsbyjs.org) V2/V3 plugin, which automatically creates TypeScript `*.d.ts` files for your CSS Modules, no matter which CSS preprocessor (Sass, LESS, Stylus etc.) you are using.

If you want to know more about CSS Modules, I recommend the article ["Component-Scoped Styles with CSS Modules" on the GatsbyJS website](https://www.gatsbyjs.com/docs/how-to/styling/css-modules/).

This plugin utilizes the Webpack loader [dts-css-modules-loader](https://github.com/Megaputer/dts-css-modules-loader), which does not make any changes in content of styles, just creates `*.d.ts` file during the work.

## Installation

```sh
npm install gatsby-plugin-dts-css-modules --save-dev
```

Then, add the plugin to your `gatsby-config.js` …

```js
module.exports = {
  // ...
  plugins: [
    // ...
    'gatsby-plugin-dts-css-modules',
    // ...
  ],
  // ...
}
```

## Usage

For CSS files use the extension `.module.css`, for Sass/SCSS use `.modules.sass` or `.module.scss` and so on.

```css
.container {
  margin: 3rem auto;
  max-width: 600px;
}
```

In TypeScript use:
```tsx
import React from 'react';
import * as containerStyles from './container.module.css';

export const Container: React.FunctionComponent = ({ children }) => {
  return (
    <section className={containerStyles.container}>{children}</section>
  );
}
```

As soon as you use the `Container` component in your code, the plugin will create a `container.module.d.ts`, which looks like this one:
```
// This file is automatically generated. Do not modify this file manually -- YOUR CHANGES WILL BE ERASED!
export const container: string;
```

There will be one `export const` for each of your class names.
