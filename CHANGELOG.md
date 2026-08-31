# Changelog

## [3.3.0](https://github.com/rolehippie/logstash/compare/v3.2.0...v3.3.0) (2026-08-31)

### Features

* use facts, better repo definition and restructuring ([aa0ada7](https://github.com/rolehippie/logstash/commit/aa0ada7aa0128d8c073a7e8f5c39a6ad0ca06f95))

### Dependencies

* **minor:** update dependency pipx:ansible-doctor to v8.4.0 ([16eebab](https://github.com/rolehippie/logstash/commit/16eebab770805b2c8ea41d1f57ed9f5c1d6dc182))
* **minor:** update dependency pipx:ansible-lint to v26.8.0 ([#59](https://github.com/rolehippie/logstash/issues/59)) ([c99894e](https://github.com/rolehippie/logstash/commit/c99894e5375cb7796b65df870591c1cff4b09feb))
* **minor:** update dependency pipx:molecule to v26.8.0 ([c67fd2a](https://github.com/rolehippie/logstash/commit/c67fd2aff05676765ab7bd2ec915bb3b16564579))
* **patch:** update dependency pipx:ansible-core to v2.21.3 ([9134f1f](https://github.com/rolehippie/logstash/commit/9134f1f3c0d2c57cc995b38314358aa0e32b5b74))
* **patch:** update dependency pipx:ansible-doctor to v8.4.1 ([#61](https://github.com/rolehippie/logstash/issues/61)) ([e1c77c2](https://github.com/rolehippie/logstash/commit/e1c77c2d44cbe2373ea08ec873ead918dbaf3449))
* **patch:** update dependency pre-commit to v4.6.2 ([#58](https://github.com/rolehippie/logstash/issues/58)) ([9c60f04](https://github.com/rolehippie/logstash/commit/9c60f0484d1a6d1ebf683ced606ded8d742a7dfa))
* **patch:** update dependency python to v3.14.7 ([e9085e2](https://github.com/rolehippie/logstash/commit/e9085e26bfd2bf34a1f8a98a56a25c458ee8e1e4))

## [3.2.0](https://github.com/rolehippie/logstash/compare/v3.1.0...v3.2.0) (2026-07-27)

## [3.1.0](https://github.com/rolehippie/logstash/compare/v3.0.0...v3.1.0) (2025-11-17)


### Features

* apply new repo structure and update linting ([138c636](https://github.com/rolehippie/logstash/commit/138c6360381488ea3b79664d04bab09c791040aa))

## [3.0.0](https://github.com/rolehippie/logstash/compare/v2.1.0...v3.0.0) (2024-02-12)


### Features

* drop support for ubuntu 18.04 ([1959f01](https://github.com/rolehippie/logstash/commit/1959f015c85f3b3192152ebfda99942831970dcc))
* used full qualified collection names ([20ff905](https://github.com/rolehippie/logstash/commit/20ff9050ce6ba124ce3d09e61dd559179b0a2d19))


### Bugfixes

* use right attribute for user shell ([83b5c1c](https://github.com/rolehippie/logstash/commit/83b5c1c4d9babcea0ef90323422207be4671dde6))

## [2.1.0](https://github.com/rolehippie/logstash/compare/v2.0.0...v2.1.0) (2023-05-29)


### Features

* use unified path for repo key and drop legacy key ([b3a638a](https://github.com/rolehippie/logstash/commit/b3a638a99f40daedd620f57eee6127d39ba75a37))

## [2.0.0](https://github.com/rolehippie/logstash/compare/v1.0.0...v2.0.0) (2023-01-05)


### Features

* upgrade logstash exporter to 0.7.0 ([3abbe89](https://github.com/rolehippie/logstash/commit/3abbe89770eea58708e2b735da6dce65a60d8f2b))
* upgrade logstash to 8.5 and simplify apt repo definition ([2d97083](https://github.com/rolehippie/logstash/commit/2d970833006030e7e083f96832c0957e477cdad8))

## 1.0.0 (2023-01-05)


### Features

* restructure workflows and enable automated releases ([8b3999b](https://github.com/rolehippie/logstash/commit/8b3999b42083d40c4ea1a06ec042ff2be2962f31))


### Bugfixes

* stdout and stderr for exporter version check ([d2e352f](https://github.com/rolehippie/logstash/commit/d2e352fb030b47bed5a66ba1b813309e0fe93150))
* use include_tasks instead of include ([eacb62b](https://github.com/rolehippie/logstash/commit/eacb62b85a8f110f7fba39aa032e7d31b1e43200))
