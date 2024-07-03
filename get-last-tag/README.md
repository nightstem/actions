# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonny17/actions/get-last-tag

## Description

This GitHub Action is designed to retrieve the last tag from a repository. It can be used to automate versioning or to gather information about the latest release.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Get Last Tag
  uses: jhonny17/actions/get-last-tag@main
  with:
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

## Inputs

| Input          | Required | Description                                                                                                                                      |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `github_token` | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub. |

## Outputs

| Output     | Description                                                                        |
| ---------- | ---------------------------------------------------------------------------------- |
| `last_tag` | The last tag found in the repository.<br/>It will output the value in JSON format. |

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
