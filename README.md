# setup-editorconfig-checker

This GitHub action downloads [editorconfig-checker](https://github.com/editorconfig-checker/editorconfig-checker) by version and adds it to your path, enabling you to lint your files according to your .editorconfig-rules, across multiple file types.

## Inputs

### `version`

**Optional** The desired version of editorconfig-checker. This will be set to the latest GitHub release version if not set.

### `command-name`

**Optional** The name by which editorconfig-checker should be available. This defaults to 'editorconfig-checker'.

# Usage

See [action.yml](action.yml)

Basic:

```yaml
steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Install editorconfig-checker
    - uses: kasperhesthaven/editorconfig-checker@v1
      with:
          version: "2.1.0" # Defaults to latest if not set

    - name: Lint
    - run: editorconfig-checker
```
