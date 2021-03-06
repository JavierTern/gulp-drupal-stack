## Config

All is easily configurable by changing values in your `gulpfile.yml` file in your project. These values are merged into the `gulpfile.default.yml` file.

For example, you can enable SCSS and JS like this:
```yml
css:
  enabled: true
js:
  enabled: true
```

You can find all the available options and defaults settings inside the `gulpfile.default.yml` file.


## Commands

- `gulp` - Run all compile tasks, and watch for changes
- `gulp compile` or `gulp build` - Run all compile tasks
- `gulp test` - Run all tests tasks (unit tests, ...)
- `gulp validate` - Run all validate tasks (eslint, ...)
- `gulp watch` - Watch for changes
- `gulp clean` - Run all clean tasks

## Specifics Commands

You can launch specifics tasks, for example "lint CSS files": `gulp validate:css`.

All the documentation can be found inside the [Features](features/css.md) section.

---

### Babel

In order to use Babel, you need to create a `.babelrc` into your project, with the presets that you want installed.

**Example:**

Run:
```bash
$ npm install --save-dev babel-preset-es2015
```
And create a `.babelrc` file:
```json
{
  "presets": ["es2015"]
}
```

### ESLint

You need to create a `.eslintrc.js` file, and specify whitch rules that you want (`eslint-config-drupal` is recommanded).

**Example:**

Run:
```bash
$ npm install --save-dev babel-eslint
$ npm install --save-dev eslint-config-drupal
```
And create a `.eslintrc.js` file:
```javascript
'use strict';
// rule reference: http://eslint.org/docs/rules
// individual rule reference: http://eslint.org/docs/rules/NAME-OF-RULE

module.exports = {
  extends: 'eslint-config-drupal'
};
```

### StyleLint

You need to create a `.stylelintrc.js` file, and specify whitch rules that you want (`stylelint-config-drupal` is recommanded).

**Example:**

Run:
```bash
$ npm install --save-dev stylelint-scss
$ npm install --save-dev stylelint-config-drupal
```
And create a `.stylelintrc.js` file:
```javascript
'use strict';

module.exports = {
  'extends': 'stylelint-config-drupal'
};
```

### CSScombx

The module follows the rules from [Drupal](https://www.drupal.org/docs/develop/standards/css/csscomb-settings-for-drupal-css-formatting-and-sort-tool).

---
