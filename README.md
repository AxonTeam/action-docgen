# action-docgen

Action to generate docs on a repo and commit the changes automatically.  

This ation was inspired from [discordjs](https://github.com/discordjs/action-docs/).  

This action will run the `docgen` npm script in the repo package.json. It will then commi tthe changes to the current branch.  
Example of config:  

```yaml
name: Docgen

on:
  push:
    branches:
    - master

jobs:
  docgen:
    name: Docgen
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@master

      - name: Install Node v12
        uses: actions/setup-node@master
        with:
          node-version: 12

      - name: Install dependencies
        run: yarn install

      - name: Build and deploy documentation
        uses: axonteam/action-docgen@master
```
