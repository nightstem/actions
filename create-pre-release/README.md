# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonny17/actions/create-pre-release

## Description

This GitHub Action allows you to create a pre-release for your repository. It can be useful for publishing pre-release versions of your software.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Create Pre-release
  uses: jhonny17/actions/create-pre-release@main
  with:
    version: '1.0.0'
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

Make sure to replace `1.0.0` with the desired version number.

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `version`      | Required | The version number for the pre-release.                                                                                                          |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |

## Outputs

| Output       | Description                        |
| ------------ | ---------------------------------- |
| `release_id` | The ID of the created pre-release. |

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
