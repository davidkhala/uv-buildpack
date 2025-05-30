# davidkhala/uv-buildpack

## Use

```yaml
steps:
- uses: actions/checkout@main
- uses: davidkhala/uv-buildpack@main
  with:
    working-directory: . # directory path (dirname) of file `pyproject.toml`. Default to current directory
    test-entry-point: echo 'test' # testing entry-point commands. such as `pytest`. If not specified, testing step will be skipped
    tests: tests # testing sources root directory.  Default `tests`
    version: 3.12 # python version. Default to runner's python version. Support 'latest' as value
    extras: extra1 extra2 # extras to be installed. It should be subset of extras defined in Default to install all extras
```
