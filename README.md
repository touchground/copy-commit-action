# copy-commit-action
Copy files from source path to taget path, then commit changes in local branch.
* Just git commmit when source path defined.

```yaml
on:
  workflow_dispatch:

jobs:
  copy-commit:
    runs-on: ubuntu-latest

    steps:
      - uses: touchground/copy-commit-action@main
        with:
          source: './src/app'
          taget: './dst/app'
          message: "auto commit"
```
output: True = changes to manifest files (commit to local branch), False = No change.
