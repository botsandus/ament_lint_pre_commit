Transition repo until I found out what to do with the public upstream

# ament_link pre-commit hooks

Work in progress pacakge

## Supported hooks

- [x] ament_black
- [ ] ament_clang_format
- [ ] ament_clang_tidy
- [ ] ament_copyright
- [ ] ament_cppcheck
- [ ] ament_cpplint
- [x] ament_flake8
- [ ] ament_lint
- [x] ament_lint_cmake
- [ ] ament_mypy
- [ ] ament_pclint
- [x] ament_pep257
- [ ] ament_pycodestyle
- [ ] ament_pyflakes
- [x] ament_uncrustify
- [x] ament_xmllint

## Python Packages publsihed by this repository

- [x] ament-black
- [x] ament-clang-tidy
- [x] ament-lint
- [x] ament-lint-cmake-py
- [x] ament-lint-flake8
- [x] ament-lint-pep257
- [x] ament-mypy
- [x] ament-pycodestyle
- [x] ament-style-uncrustify
- [x] ament-xmllint

## TODO

- [ ] Fix release version madness at pypi! (flake8 linter already in 0.14.4 instead of 0.14.2, because of packaging errors)
- [ ] Automate release of ament\_\* python packages
- [ ] Automate tags of repository
  - [ ] The tag in the pyproject.toml should be the one from the upstream (iron) for example
  - [ ] This tag should be the same for all the dependencies
  - [ ] Upon new changes, first all the python packages should be publsihed and then this repo hook should be tagged
