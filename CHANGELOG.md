# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-log-writer-mail`, published as `gizmocraft/zendframework1-log-writer-mail`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-log-writer-mail` to `gizmocraft/zendframework1-log-writer-mail`. It now requires `gizmocraft/zendframework1-layout`, `gizmocraft/zendframework1-log` and `gizmocraft/zendframework1-mail`, each `^2.0.0`.

### Other changes

- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Dropped the dev dependency on the `view-helper-layout` package. The test layout script reads the `events` value through the `placeholder('Zend_Layout')` view helper instead of `layout()`.
- Tests migrated to PHPUnit 13 attributes. The removed `getMockForAbstractClass()` and the deprecated `any()` mock expectations were replaced by small test doubles (a transport and a layout subclass).
- CI runs PHP 8.5 and 8.6.
- No library code changes and no public signature changes.
