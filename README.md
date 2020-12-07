#### [Github Action](https://docs.github.com/en/free-pro-team@latest/actions/guides/building-and-testing-python)

   * Select python version
   
```
jobs:
  build:

    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: [3.8, 3.9]
```
