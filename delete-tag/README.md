# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonnyvargasarias/actions/delete-tag

## Description

This GitHub Action allows you to delete a tag in your repository.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Delete Tag
  uses: jhonnyvargasarias/actions/delete-tag@main
  with:
    build-version: '1.0.0'
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

Make sure to replace `1.0.0` with the desired tag name.

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `version`      | Required | The version number for the pre-release.                                                                                                          |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |

## Outputs

This action doesn't have any outputs.

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
