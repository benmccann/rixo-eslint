Monorepo for all my eslint & prettier stuff, in a easily sharable form.

# Installation

```bash
npm install --dev @rixo/eslint-config
```

A `.eslintrc` and `.prettierrc` will be created in your project by a npm postinstall script. If these files already exists in your project, then they won't be touched.

In some cases, depending on the order you run your `npm install` commands, the files may not be created or may target the wrong variant. In case of problem, refer to the [variants](#variants) section bellow and fix it!

# Usage

Just use eslint, & prettier...

```bash
npx eslint src

npx prettier 'src/**/*'

npx prettier --write 'src/**/*'
```

You can customize your rules in `.eslintrc` too.

# Customization

## Disable plugin

All variants include [eslint-plugin-disable][eslint-plugin-disable] so you can always disable a plugin that was added automatically, if the combination does not work well for you.

`eslint-plugin-disable` supports disabling in `.eslintrc` or on a per-file basis, with a comment:

```js
/* eslint-plugin-disable import, prettier */
```

# Variants

Note: the example bellow use the shortcut form of extends, but feel free to use an array if you want to extend from other config.

Example:

```yml
# .eslintrc
extends:
  - '@rixo'
  - 'plugin:whatever'
```

## Default

```yml
# .eslintrc
extends: '@rixo'
```

## Atom

Specific rules for development of Atom packages.

```yml
# .eslintrc
extends: '@rixo/atom'
```

[eslint-plugin-disable]: https://github.com/mradionov/eslint-plugin-disable
