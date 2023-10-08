# ament_link pre-commit hooks

## How to use the github action in a workflow

```yaml
jobs:
  style:
    runs-on: ubuntu-latest
    container:
      image: ros:iron-ros-base
      options: --user 1001:127 # TODO: Fix this crap
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with: { python-version: "3.10" }
      - uses: nachovizzo/ament_lint_pre_commit@v0.0.5
```

## Supported hooks

For the time being, all the hooks, with the exception of `ament-black`, and
`ament-clang-format` must be system-wide available. This means that pre-commit
will not attempt to install it, but rather use a binary that is visible in the
`$PATH`. I tried an alternative solution, like publishing the python packages
to the [pypi.org registry](https://pypi.org/search/?q=%22ament_%22&o=), but
this comes with the additional burden of having to manually release new
packages every time there is an update on the ROS mainstream repositories. For
now, we keep it simple by just using the available ament linters. In the
future, it would be ideal to just rely on pure python packages so the
`pre-commit` hook can be run on any non-ros environment.

- [x] ament_black (\*)
- [x] ament_clang_format (\*)
- [x] ament_cpplint
- [x] ament_flake8
- [x] ament_lint_cmake
- [x] ament_pep257
- [x] ament_uncrustify
- [x] ament_xmllint

(\*): [ament-black](https://github.com/nachovizzo/ament_black) managed by
@nachovizzo, automatic pypi.org releases on tag pushes
(\*): ament-clang-format: is not available yet on pypi but it's available
inside a ament_ friendly environment such as ROS 2

## Unsupported hooks

The fact that are unspotted does not mean that they don't work, it only means I
haven't tested it so far and therefore are not part of the
[.pre-commit-hooks.yaml](./.pre-commit-hooks.yaml) config.

- [ ] ament_mypy
- [ ] ament_pclint
- [ ] ament_pycodestyle
- [ ] ament_pyflakes
- [ ] ament_clang_format
- [ ] ament_clang_tidy
- [ ] ament_copyright
- [ ] ament_cppcheck
- [ ] ament_lint
