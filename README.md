# ament_link pre-commit hooks

Work in progress pacakge

## Supported hooks

- [x] ament_black
- [x] ament_flake8
- [x] ament_lint_cmake
- [x] ament_pep257
- [x] ament_uncrustify
- [x] ament_xmllint

## Unsupported hooks

- [ ] ament_mypy
- [ ] ament_pclint
- [ ] ament_pycodestyle
- [ ] ament_pyflakes
- [ ] ament_clang_format
- [ ] ament_clang_tidy
- [ ] ament_copyright
- [ ] ament_cppcheck
- [ ] ament_cpplint
- [ ] ament_lint

## Python Packages published by this repository

- [x] ament-black

## Deprecated Python Packages published by this repository

Basing your pre-commit github actions on top of ros:$ROS_DISTRO-ros-base give
you most of the ament linters, and therefore there is no need to mantain python
packages. In the long run it might be a better idea to publish the packages on
pypi and pythonize everything. But for now we rely on `system` hooks with the
`ament-black` exception.

- [x] ament-clang-tidy
- [x] ament-lint
- [x] ament-lint-cmake-py
- [x] ament-lint-flake8
- [x] ament-lint-pep257
- [x] ament-mypy
- [x] ament-pycodestyle
- [x] ament-style-uncrustify
- [x] ament-xmllint
