# <img src="../assets/images/github-actions-logo.png" alt="github actions logo" style="height: 32px"  /> jhonnyvargasarias/actions/generate-next-version

## Description

This GitHub Action is used to automatically generate the next version number for a project. It can be configured to follow different versioning schemes, such as semantic versioning or custom numbering.

## Usage

To use this action, you can include the following step in your workflow:

```yaml
- name: Generate next version
  uses: jhonnyvargasarias/actions/generate-next-version@main
  with:
    github_token: ${{ secrets.GITHUB_TOKEN }}
    max_patch_version: 10
    max_minor_version: 10
    increment_minor_version: false # Optional
    increment_major_version: false # Optional
    is_patch_version_limited: true # Optional
```

## Inputs

| Input                      | Required | Description                                                                                                                                                           |
| -------------------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `github_token`             | Required | The GitHub token used to authenticate the action.<br />You can use `${{ secrets.GITHUB_TOKEN }}` to access the default token provided by GitHub.                      |
| `max_patch_version`        | Required | The maximum number that a patch version can reach.<br />Once the patch limit is exceeded, the minor number increments and the patch number resets to 0.               |
| `max_minor_version`        | Required | The maximum number that a minor version can reach.<br />Once the minor limit is exceeded, the major number increments and the patch and the minor numbers reset to 0. |
| `increment_minor_version`  | Optional | When this is set to `true`, it increments the minor version and the patch number is reset to 0.<br />Default is `false`.                                              |
| `increment_major_version`  | Optional | When this is set to `true`, it increments the major version and the minor and patch numbers set to 0.<br />Default is `false`.                                        |
| `is_patch_version_limited` | Optional | When this is deactivated allows to increment the patch number over the limit.<br />This overwrites the patch and minor limits and increments.<br />Default is `true`. |

## Outputs

| Output         | Description                |
| -------------- | -------------------------- |
| `next_version` | The generated new version. |

---

For more information, you can check out the [GitHub Actions documentation](https://docs.github.com/en/actions).
