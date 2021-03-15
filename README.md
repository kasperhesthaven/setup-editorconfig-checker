# Setup Editorconfig Checker

[![GitHub release](https://img.shields.io/github/release/kasperhesthaven/setup-editorconfig-checker.svg)](https://gitHub.com/kasperhesthaven/setup-editorconfig-checker/releases/)
[![GitHub license](https://img.shields.io/github/license/kasperhesthaven/setup-editorconfig-checker.svg)](https://github.com/kasperhesthaven/setup-editorconfig-checker/blob/master/LICENSE)

This GitHub action downloads [editorconfig-checker](https://github.com/editorconfig-checker/editorconfig-checker) by version and adds it to your path, enabling you to lint your files according to your .editorconfig-rules, across multiple file types.

## Inputs

### `version`

**Optional** The desired version of editorconfig-checker. This will be set to the latest GitHub release version if not set.

### `command-name`

**Optional** The name by which editorconfig-checker should be available. This defaults to 'editorconfig-checker'.

## Usage

See [action.yml](action.yml)

Basic:

```yaml
steps:
    - name: Checkout repository
      uses: actions/checkout@v2.3.4

    - name: Install editorconfig-checker
      uses: kasperhesthaven/setup-editorconfig-checker@v1.2.0
      with:
          version: "2.1.0" # (Optional) Defaults to latest if not set

    - name: Lint
      run: editorconfig-checker
```

## License

This project is licensed under the Unlicense license - see the [LICENSE.txt](LICENSE.txt) file for details.
