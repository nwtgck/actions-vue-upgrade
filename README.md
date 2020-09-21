# vue-upgrade
Update dependencies with `vue upgrade` and make pull requests

## Usage

```yml
name: vue upgrade

on:
  push:
    branches:
      - master

jobs:
  vue_upgrade:
    runs-on: ubuntu-18.04
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-node@v1
        with:
          node-version: 12.x
      # NOTE: Important! you should install dependencies before vue upgrade
      - run: npm ci
      - uses: nwtgck/actions-vue-upgrade@develop
```


## Sample pull request
Here is a sample pull request made by with this action.  
<https://github.com/nwtgck/piping-ui-web/pull/595>
