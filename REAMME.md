# 描述

> 参考 mock , lodash 库
> 本仓库主要是学习使用

## 约束

> 首字母大写全为`type`, `interface`, `整合包[待弃用]`
>

```json
{
  "name": "rh-ts-methods",
  "version": "0.0.2",
  "description": "方法包",
  "main": "dist/index.js",
  "scripts": {
    "build": "tsc",
    "dev": "ts-node-dev --respawn --transpile-only ./src/test/index.ts",
    "dev_test": "ts-node-dev --respawn --transpile-only ./src/__test__/test_rh.ts",
    "test": "jest",
    "test-c": "jest --coverage",
    "restart": "rimraf dist && npm run build && npm start",
    "start": "node ./dist/index.js",
    "prod": "npm run build && npm run start",
    "pub": "npm publish",
    "prepare": "husky install",
    "lint": "eslint ./src --ext .jsx,.js,.ts,.tsx",
    "lint:fix": "eslint ./src --ext .jsx,.js,.ts,.tsx --fix --quiet",
    "lint:format": "prettier  --loglevel warn --write \"./**/*.{js,jsx,ts,tsx,css,md,json}\" ",
    "lint:style": "stylelint src/**/*.{css,less,scss} --fix ",
    "commit": "cz"
  },
  "keywords": [
    "typescript",
    "ts"
  ],
  "author": "ruihuag",
  "license": "ISC",
  "dependencies": {
    "reflect-metadata": "^0.1.13"
  },
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    },
    "cz-customizable": {
      "config": ".cz-config.js"
    }
  },
  "lint-staged": {
    "*.{ts,js,tsx}": [
      "eslint",
      "echo 'no error'"
    ]
  },
  "devDependencies": {
    "@commitlint/cli": "^12.1.4",
    "@commitlint/config-conventional": "^12.1.4",
    "@types/jest": "^27.4.0",
    "@types/node": "^16.11.22",
    "@typescript-eslint/eslint-plugin": "^5.12.0",
    "@typescript-eslint/parser": "^5.12.0",
    "commitizen": "^4.2.4",
    "commitlint-config-cz": "^0.13.3",
    "cz-conventional-changelog": "^3.3.0",
    "cz-customizable": "^6.3.0",
    "eslint": "^8.9.0",
    "eslint-config-prettier": "^8.3.0",
    "eslint-plugin-import": "^2.23.4",
    "eslint-plugin-jest": "^26.1.0",
    "eslint-plugin-jsx-a11y": "^6.4.1",
    "eslint-plugin-prettier": "^3.4.0",
    "eslint-plugin-react": "^7.24.0",
    "eslint-plugin-react-hooks": "^4.2.0",
    "eslint-plugin-simple-import-sort": "^7.0.0",
    "husky": "^7.0.4",
    "jest": "^27.5.1",
    "lint-staged": "^12.3.4",
    "node-notifier": "^8.0.2",
    "prettier": "^2.5.1",
    "rh-js-methods": "^1.0.2",
    "rimraf": "^3.0.2",
    "ts-jest": "^27.1.3",
    "ts-node-dev": "^1.1.8",
    "typescript": "^4.5.5"
  }
}
```
