# rgl-action

A GitHub Action for rgl Bedrock Addon compiler pipeline.

## Usage

### Pre-requisites

Create a workflow `.yml` file in your `.github/workflows` directory.

### Inputs

| Input          | Description                         | Default   | Values |
| -------------- | ----------------------------------- | --------- | - |
| `profile`      | Regolith profile to run             | `default` | |
| `github_token` | GitHub token to get private filters | None      | |
| `nodejs_runtime` | JS Runtime to run | `node`      | `node`, `bun` |
| `resolvers` | Resolver to use | `github.com/Bedrock-OSS/regolith-filter-resolver/resolver.json` | |

### Example workflow

```yml
name: Example workflow
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: respectZ/rgl-action@v1.0.0
        with:
          profile: default
```