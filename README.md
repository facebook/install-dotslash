# GitHub Action to install DotSlash

[<img alt="build status" src="https://img.shields.io/github/actions/workflow/status/facebook/install-dotslash/ci.yml?branch=latest&style=for-the-badge" height="20">](https://github.com/facebook/install-dotslash/actions?query=branch%3Alatest)

This GitHub Action installs a precompiled `dotslash` binary from
<https://github.com/facebook/dotslash/releases>.

```yaml
name: test suite
on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: facebook/install-dotslash@latest
      - run: ./some_dotslash_file
```

By default, the action installs the latest DotSlash release. To pin a release,
pass the release tag:

```yaml
      - uses: facebook/install-dotslash@latest
        with:
          version: v0.5.9
```

## License

`install-dotslash` is MIT licensed, as found in the LICENSE file.
