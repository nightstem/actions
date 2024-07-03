# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonny17/actions/delete-release

## Description

This GitHub Action allows you to delete a release in your repository.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Delete release
  uses: jhonny17/actions/delete-release@main
  with:
    release_id: 354353
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

Make sure to replace 354353 with the release ID to delete.

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `release_id`   | Required | The ID for the release.                                                                                                                          |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |

## Outputs

This action doesn't have any outputs.

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
