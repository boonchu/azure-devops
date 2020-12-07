#### [Github Action](https://docs.github.com/en/free-pro-team@latest/actions/guides/building-and-testing-python)

   * Learn [Github Action CI](https://docs.microsoft.com/en-us/learn/modules/github-actions-ci/?WT.mc_id=udacity_learn-wwl)
   * Learn [Github PR](https://docs.microsoft.com/en-us/learn/modules/manage-changes-pull-requests-github/?WT.mc_id=udacity_learn-wwl)
   * Learn [Github conflict resolution](https://docs.microsoft.com/en-us/learn/modules/resolve-merge-conflicts-github/?WT.mc_id=udacity_learn-wwl)
   * Learn [Github release workflow process](https://docs.microsoft.com/en-us/learn/modules/release-based-workflow-github/?WT.mc_id=udacity_learn-wwl)
   * Learn [Implement pipeline](https://docs.microsoft.com/en-us/learn/modules/implement-code-workflow/?WT.mc_id=udacity_learn-wwl)
   * Learn [Maintain github security - best practice](https://docs.microsoft.com/en-us/learn/modules/implement-code-workflow/?WT.mc_id=udacity_learn-wwl)
   * The 'status badge' is a great way to communicate with your team.

![CI](https://github.com/boonchu/azure-devops/workflows/CI/badge.svg)

```
- Use Github actions 
- Select latest CI build job and click Button '...'
- Create Statu Badge -> 'Copy status badge markdown'
- Add 'badge status' to README.md
```

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
