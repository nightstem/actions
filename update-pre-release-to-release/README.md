# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonny17/actions/update-pre-release-to-release

## Description

This GitHub Action updates the state of a pre-release to be release. It can be useful for publishing pre-release versions of your software.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Update Pre-release to Release
  uses: jhonny17/actions/update-pre-release-to-release@main
  with:
    release_id: 12345
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

Make sure to replace `12345` with the correct release ID.

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `release_id`   | Required | The ID for the pre-release.                                                                                                                      |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |

## Outputs

This action doesn't have any outputs.

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
