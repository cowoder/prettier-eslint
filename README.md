## Quick guide to combining Prettier and Eslint

### Add Eslint and Prettier to dev deps

`npm install -D eslint prettier`

### Add the packages to combine Eslint and Prettier to dev deps

`npm install -D eslint-config-prettier eslint-plugin-prettier`

### Add Airbnb styleguide to dev deps (choose one)

#### This includes packages only relevant for React projects:
`npx install-peerdeps --dev eslint-config-airbnb`

#### Use this for projects without React:
`npx install-peerdeps --dev eslint-config-airbnb-base`

### Create eslint config file in project root: .eslintrc.json

Example config, add/remove rules as desired:

```
{
  "env": {
    "browser": true,
    "node": true
  },
  "extends": ["airbnb-base", "prettier"], // or use airbnb without base for React based projects
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": ["error"]
  }
}
```

### Create prettier config file in project root: .prettierrc

Example config, add/remove rules as desired:

```
{
  "semi": true,
  "trailingComma": "all",
  "singleQuote": true,
  "printWidth": 100
}
```
