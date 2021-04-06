# eslint-config

My personal ESLint config settings.

* Uses [ESLint's recommended settings][eslint-recommended] as the base configuration.
* Includes the [clean-regex][clean-regex] plugin.
* `.eslintrc.base.yml`: Rules relating to syntax errors, logic errors, variables, and best practices. Suitable for use on teams.
* `.eslintrc.style.js`: Rules relating to stylistic choices. Highly opinionated and subjective; not suitable for use on teams.

To use:

1. Copy the configuration files to your project.
2. Remove `.base` and `.style` from the filenames.
3. Add `extends: './.eslintrc.yml'` to the stylistic rules.

Because `.js` extensions take precedence over `.yml` extensions when ESLint determines the config file to use, this allows you to add the stylistic rules to your `.gitignore` so that only the base rules are shared with other developers.

Rules that you wish to share with other developers should be added to `.base` and personal rules should be added to `.style`:

* shared rules: `.eslintrc.base.yml`
* personal rules: `.eslintrc.style.js`

<!-- LINKS -->
[clean-regex]:        https://github.com/RunDevelopment/eslint-plugin-clean-regex
[eslint-recommended]: https://eslint.org/docs/user-guide/configuring/configuration-files#using-eslintrecommended
