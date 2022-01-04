# action-download-github-release-artifact
GitHub Action that downloads an artifact from a GitHub release (public or private)

### Usage

```
steps:
- uses: scoremedia/action-download-github-release-artifact@v1
with:
    owner: 'scoremedia'
    repo: 'release-artifact-test'
    tag: 'v1.0.0'
    artifact: 'test.txt'
    destination: './folder'
```

Note: This action depends on `jq` and `curl` being installed.

### Inputs

| Input | Description | Required |
|:-----:|:-----------:|:--------:|
| `owner` | The owner of the repository | Yes |
| `repo` | The name of the repository | Yes |
| `tag` | The tag of the release | Yes |
| `artifact` | The name of the artifact | Yes |
| `destination` | The destination folder | Yes |
| `token` | The Github token. If not provided it uses `GITHUB_TOKEN` | No |

### Outputs

| Input | Description |
|:-----:|:-----------:|
| `artifact_url` | The URL of the artifact saved to the `destination` folder with the name `artifact` |