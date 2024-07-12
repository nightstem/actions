# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonnyvargasarias/actions/clear-ref-cache

## Description

This GitHub Action allows you to clear all the cache keys that have been created for a ref.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Clear Ref Cache
  uses: jhonnyvargasarias/actions/clear-ref-cache@main
  with:
    github_token: ${{ secrets.GITHUB_TOKEN }}
    ref: refs/heads/main
```

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |
| `ref`          | Optional | The branch or tag ref where the cache is stored.                                                                                                 |

## Outputs

This action doesn't have any outputs.

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
