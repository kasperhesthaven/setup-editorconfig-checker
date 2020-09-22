# setup-editorconfig-checker

This action downloads [editorconfig-checker](https://github.com/editorconfig-checker/editorconfig-checker) by version number and adds it to your path, enabling you to check if your files consider your .editorconfig-rules, regardless of filetype.

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
