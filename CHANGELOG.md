## [1.0.5](https://github.com/catalystsquad/action-release-action/compare/v1.0.4...v1.0.5) (2023-01-10)


### Bug Fixes

* adjust semantic version action version ([#8](https://github.com/catalystsquad/action-release-action/issues/8)) ([c759794](https://github.com/catalystsquad/action-release-action/commit/c759794328f1ec60d91ffb4d698de3ee8ab61435))

## [1.0.4](https://github.com/catalystsquad/action-release-action/compare/v1.0.3...v1.0.4) (2022-04-01)


### Bug Fixes

* Checkout main, not the commit that triggered the workflow. That commit is already out of date. ([#6](https://github.com/catalystsquad/action-release-action/issues/6)) ([ff5e96b](https://github.com/catalystsquad/action-release-action/commit/ff5e96b15a62b4c85a3fb7bdde96d1b4de78c842))

## [1.0.3](https://github.com/catalystsquad/action-release-action/compare/v1.0.2...v1.0.3) (2022-04-01)


### Bug Fixes

* Specify which branch to commit readme back to. "main" is already checked out when this workflow runs, but the auto commit action defaults to head_ref so for PR triggers you must specify the branch name. ([#5](https://github.com/catalystsquad/action-release-action/issues/5)) ([95b75df](https://github.com/catalystsquad/action-release-action/commit/95b75df808baa0fcb545cffc6d18129705cf8e54))

## [1.0.2](https://github.com/catalystsquad/action-release-action/compare/v1.0.1...v1.0.2) (2022-04-01)


### Bug Fixes

* Checkout main before updating readme ([#4](https://github.com/catalystsquad/action-release-action/issues/4)) ([de43ca4](https://github.com/catalystsquad/action-release-action/commit/de43ca48535ca5284fdc96741cb9a1f59b2179ce))

## [1.0.1](https://github.com/catalystsquad/action-release-action/compare/v1.0.0...v1.0.1) (2022-04-01)


### Bug Fixes

* Update order of operations for a release ([#3](https://github.com/catalystsquad/action-release-action/issues/3)) ([d7b9fa8](https://github.com/catalystsquad/action-release-action/commit/d7b9fa847be050123bfdfb95e49d98a345ebfbfe))

# 1.0.0 (2022-02-28)


### Bug Fixes

* Initial commit ([#1](https://github.com/catalystsquad/action-release-action/issues/1)) ([a553dd0](https://github.com/catalystsquad/action-release-action/commit/a553dd00c07e8f2c215af663695a3db033e96e73))
* Update readme format and add example usage ([#2](https://github.com/catalystsquad/action-release-action/issues/2)) ([b743506](https://github.com/catalystsquad/action-release-action/commit/b743506b0e7267f5c59f3ee4438d17015345c4f5))
