# eslint-plugin-artefactor

A comprehensive linting solution that sweeps your code clean. Fly through your codebase with ease and precision!

## Table of Contents

<!-- toc -->

- [Installation](#installation)
- [Usage](#usage)

<!-- tocstop -->

### Installation

You'll first need to install [ESLint](https://eslint.org/):

```sh
npm i eslint --save-dev
npm i typescript
```

Next, install `eslint-plugin-artefactor`:

```sh
npm install eslint-plugin-artefactor --save-dev
```

Next, install all peerDependencies for this plugin:

```sh
npx install-peerdeps eslint-plugin-artefactor
```

### Usage

1. Add `artefactor` to the extends or plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:
   ```json
   {
      "parser": "@typescript-eslint/parser",
      "parserOptions": {
        "ecmaVersion": 13,
        "sourceType": "module",
        "ecmaFeatures": {
          "jsx": true,
          "modules": true,
          "experimentalObjectRestSpread": true
        }
      },
      "ignorePatterns": [
        "**/*",
        "node_modules"
      ],
      "settings": {
        "react": {
          "pragma": "React",
          "fragment": "Fragment",
          "version": "detect"
        },
        "import/resolver": {
          "typescript": {
            "alwaysTryTypes": true
          }
        }
      },
      "extends": [
        "plugin:artefactor/recommended"
      ],
      "plugins": [
        "artefactor"
      ]
    }
    ```

2. If you don't have a `.prettierrc` config, please add it

    ```prettier
    {
      "singleQuote": true,
      "printWidth": 140,
      "useTabs": false,
      "tabWidth": 2,
      "trailingComma": "all",
      "semi": false
    }
    ```
