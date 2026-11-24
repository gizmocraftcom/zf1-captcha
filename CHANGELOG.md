# Changelog
## 2.0.0
Fork of `diablomedia/zendframework1-captcha`, published as `gizmocraft/zendframework1-captcha`.
### Breaking changes
- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-captcha` to `gizmocraft/zendframework1-captcha`. It now requires the `gizmocraft/zendframework1-*` forks (exception, loader, crypt, text, form, validate, view at `^2.0.0`; config and session at `^3.0.0`).
- Removed `Zend_Captcha_ReCaptcha` and `Zend_Form_Decorator_Captcha_ReCaptcha`, together with their tests, and dropped the requirement on `diablomedia/zendframework1-service-recaptcha`. The classes depend on the reCAPTCHA v1 service, which Google shut down in 2018, so they cannot work any more. Code that uses `'captcha' => 'ReCaptcha'` or the `Captcha_ReCaptcha` decorator must switch to another captcha (Dumb, Figlet, Image or Word) or to a maintained reCAPTCHA integration outside this package.
- The remaining captchas (Dumb, Figlet, Image, Word), `Zend_Captcha_Adapter`, `Zend_Captcha_Base`, `Zend_Form_Element_Captcha` and the Captcha and Word decorators are unchanged.
### Other changes
- No other public signatures changed. `Zend_Captcha_Image` (GD, FreeType) produces no deprecations on PHP 8.5 and 8.6; it never called `imagedestroy()`.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes (`#[Group]`, `#[DoesNotPerformAssertions]` instead of annotations, which PHPUnit 12+ ignores).
- CI runs PHP 8.5 and 8.6.
