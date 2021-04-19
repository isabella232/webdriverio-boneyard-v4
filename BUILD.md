Things are getting old and creaky, and to prevent false positive on depencency scanners, we are not including the build tooling in package.json

Here's how the latest build worked out:

1. Install build dependencies:

```
npm i \
  babel-cli \
  babel-plugin-add-module-exports \
  babel-plugin-array-includes \
  babel-plugin-transform-runtime \
  babel-preset-env \
  babel-preset-stage-0 \
  cpx \
  npm-run-all \
  rimraf
```

In case the latest of these don't work, at the last build the tags were:

```
  "devDependencies": {
    "babel-cli": "^6.26.0",
    "babel-plugin-add-module-exports": "^1.0.4",
    "babel-plugin-array-includes": "^2.0.3",
    "babel-plugin-transform-runtime": "^6.23.0",
    "babel-preset-env": "^1.7.0",
    "babel-preset-stage-0": "^6.24.1",
    "cpx": "^1.5.0",
    "mocha": "^9.1.3",
    "npm-run-all": "^4.1.5",
    "rimraf": "^3.0.2"
  },
```

2. `npm run build`

3. `npm pack` for a tarball

