# recore-config

ESLint and TSConfig for @recore projects

```sh
npm i -D eslint prettier @recore/config
```

提交之前检查规范

```sh
npm i -D husky lint-staged
```

package.json
```json
{
  "scripts": {
    "lint": "eslint src --fix --ext .ts --ext .tsx"
  },
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "src/**/*.{ts,tsx}": [
      "npm run lint"
    ]
  }
}
```
