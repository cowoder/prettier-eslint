## Quick guide to combining Prettier and Eslint

### Add Eslint and Prettier to dev deps

`npm i -D eslint prettier`

### Add the packages to combine Eslint and Prettier to dev deps

`npm i -D eslint-config-prettier eslint-plugin-prettier`

### Add Airbnb styleguide to dev deps **__(choose one)__**

#### This includes packages only relevant for React projects:
`npx install-peerdeps -D eslint-config-airbnb`

#### Use this for projects without React:
`npx install-peerdeps -D eslint-config-airbnb-base`

### Create eslint config file in project root: .eslintrc.json
Optional: run `npx eslint --init` instead

Example config, add/remove rules as desired:

```json
{
  "env": {
    "browser": true,
    "node": true,
    "jest": true
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

```json
{
  "semi": true,
  "trailingComma": "all",
  "singleQuote": true,
  "printWidth": 100
}
```
