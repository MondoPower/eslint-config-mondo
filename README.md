# eslint-config-mondo
This package is responsible for housing the ubi development teams preferred eslint rules and configuration

## Publishing
This leverages an automation token generated against the npm organisation and is stored in the github secrets. The publish occurs via github action. If you wish to publish a new version of this project to NPM, you will need to increment the version number in the package.json any new commits without incrementing this number will not be published

## Setting up in your repo

- npm i @mondopower/eslint-config-mondo --save-dev
- npm uninstall eslint-config-stickler
- Goto your .eslintrc.js; The extends section array handles configuration extensions, replace eslint-config-stickler with @mondopower/eslint-config-mondo e.g.

```javascript
extends: [
    '@mondopower/eslint-config-mondo',
    'plugin:@typescript-eslint/eslint-recommended',
    'plugin:@typescript-eslint/recommended',
],
```
