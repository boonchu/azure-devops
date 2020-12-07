#### [Github Action](https://docs.github.com/en/free-pro-team@latest/actions/guides/building-and-testing-python)

![CI](https://github.com/boonchu/azure-devops/workflows/CI/badge.svg)

   * Select python version 3.9 for testing
   
```
jobs:
  build:

    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: [3.9]

    ...

    steps:
    ...

      - name: Set up Python ${{ matrix.python-version }}
        uses: actions/setup-python@v2
        with:
            python-version: ${{ matrix.python-version }}

```
