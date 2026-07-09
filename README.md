# davidkhala/uv-buildpack

## Use

```yaml
steps:
- uses: actions/checkout@main
- uses: davidkhala/uv-buildpack@main
  with:
    version: 3.12 # python version. Default to runner's python version. Support 'latest' as value
    working-directory: . # directory path (dirname) of file `pyproject.toml`. Default to current directory
    extras: extra1 extra2 # extras to be installed. They are subset of [project.optional-dependencies]. Default to install all extras
    groups: group1 group2 # groups to be installed. They are subset of [dependency-groups]. Default to install all groups
    post-install: echo 'post install' # script to run with `uv run` after `uv sync`. If not specified, this step will be skipped
    tests: tests # testing sources root directory.  Default `tests`
    test-entry-point: echo 'test' # testing entry-point commands. such as `pytest`. If not specified, testing step will be skipped
```
