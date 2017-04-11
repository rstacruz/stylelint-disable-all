# stylelint-disable-all

> Adds exceptions to all existing Stylelint or Eslint violations

This utility adds `/* stylelint-ignore */` to all files that are currently violating the stylelint rules. As a result, [Stylelint] will only take effect for new styles, leaving old styles un-linted. Also works for [Eslint].

## Installation

```sh
yarn global add stylelint-disable-all   # If using yarnpkg.com
# or
npm install -g stylelint-disable-all
```

## Usage

Run [Stylelint] or [Eslint] with the `-f json` flag (JSON formatter), and pipe it to stylelint-disable-all. **This will modify files right away,** so first make sure you're on a clean Git commit.

```sh
# CSS
./node_modules/.bin/stylelint path/to/css/**/*.css -f json | stylelint-disable-all

# or JavaScript
./node_modules/.bin/eslint path/to/js/**/*.js -f json | stylelint-disable-all
```

When this is done, inspect the mess that it creates.

```sh
git status
```

[Stylelint]: http://stylelint.io/
[Eslint]: http://eslint.org/

## Thanks

**stylelint-disable-all** © 2017+, Rico Sta. Cruz. Released under the [MIT] License.<br>
Authored and maintained by Rico Sta. Cruz with help from contributors ([list][contributors]).

> [ricostacruz.com](http://ricostacruz.com) &nbsp;&middot;&nbsp;
> GitHub [@rstacruz](https://github.com/rstacruz) &nbsp;&middot;&nbsp;
> Twitter [@rstacruz](https://twitter.com/rstacruz)

[![](https://img.shields.io/github/followers/rstacruz.svg?style=social&label=@rstacruz)](https://github.com/rstacruz) &nbsp;
[![](https://img.shields.io/twitter/follow/rstacruz.svg?style=social&label=@rstacruz)](https://twitter.com/rstacruz)

[MIT]: http://mit-license.org/
[contributors]: http://github.com/rstacruz/stylelint-disable-all/contributors
