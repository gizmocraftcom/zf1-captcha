# Zend Framework 1 - Captcha

[![Build](https://github.com/gizmocraftcom/zf1-captcha/workflows/Build/badge.svg?event=push)](https://github.com/gizmocraftcom/zf1-captcha/actions?query=workflow%3ABuild+event%3Apush)
[![codecov](https://codecov.io/gh/gizmocraftcom/zf1-captcha/branch/master/graph/badge.svg)](https://codecov.io/gh/gizmocraftcom/zf1-captcha)
[![Latest Stable Version](https://poser.pugx.org/gizmocraft/zendframework1-captcha/v/stable)](https://packagist.org/packages/gizmocraft/zendframework1-captcha)
[![Total Downloads](https://poser.pugx.org/gizmocraft/zendframework1-captcha/downloads)](https://packagist.org/packages/gizmocraft/zendframework1-captcha)
[![License](https://poser.pugx.org/gizmocraft/zendframework1-captcha/license)](https://packagist.org/packages/gizmocraft/zendframework1-captcha)


This is just the Zend_Captcha, Zend_Form_Element_Captcha and Zend_Form_Decorator_Captcha components extracted from our fork of the Zend Framework 1 repo (https://github.com/gizmocraftcom/zf1).

## Dropped functionality

`Zend_Captcha_ReCaptcha` and `Zend_Form_Decorator_Captcha_ReCaptcha` have been removed, together with their tests and the requirement on `diablomedia/zendframework1-service-recaptcha`. They depend on the reCAPTCHA v1 service, which Google shut down in 2018. The Dumb, Figlet, Image and Word captchas, the `Zend_Captcha_Adapter` interface, `Zend_Captcha_Base`, `Zend_Form_Element_Captcha` and the Captcha and Word decorators are unchanged. This is a breaking change; see `CHANGELOG.md`.

Originally forked from the upstream repository https://github.com/diablomedia/zf1-captcha. Copyright and license of the original authors are kept in LICENSE.txt.
