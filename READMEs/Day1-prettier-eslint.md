# Day1: Setup Prettier and ESLint

## Install
```bash
yarn add --dev @typescript-eslint/eslint-plugin
yarn add --dev prettier eslint-config-prettier
```

## Setup Prettier
- Create a `.prettierrc.json` file
```json
{
	"printWidth": 100,
	"tabWidth": 2,
	"semi": false,
	"singleQuote": true,
	"bracketSameLine": false,
	"trailingComma": "es5",
	"bracketSpacing": true,
	"arrowParens": "avoid",
	"parser": "typescript"
}
```

## Setup ESLint
- Change your `.eslintrc.json` as below
```json
{
  "plugins": ["@typescript-eslint"],
  "extends": [
    "next/core-web-vitals",
    "plugin:@typescript-eslint/recommended",
    "prettier"
  ],
  "rules": {
    "@typescript-eslint/no-unused-vars": "error",
    "@typescript-eslint/no-explicit-any": "error"
  }
}
```