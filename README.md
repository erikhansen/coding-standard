# ECG Magento Code Sniffer Coding Standard

[![SensioLabsInsight Medal](https://insight.sensiolabs.com/projects/a06c37c6-0d79-4476-aff5-12d8ce1d8c53/big.png "SensioLabsInsight Medal")](https://insight.sensiolabs.com/projects/a06c37c6-0d79-4476-aff5-12d8ce1d8c53)

ECG Magento Code Sniffer Coding Standard is a set of rules and sniffs for [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) tool.

It allows automatically check your code against some of the common Magento and PHP coding issues, like:
- raw SQL queries;
- SQL queries inside a loop;
- direct instantiation of Mage and Enterprise classes;
- unnecessary collection loading;
- excessive code complexity;
- use of dangerous functions;
- use of PHP Superglobals;

and many others.

#### Update: Magento 2 standard just released. Try it out:

```sh
$ phpcs --config-set installed_paths ./vendor/magento-ecg/coding-standard
$ phpcs --standard=EcgM2 /path/to/code
```

# Installation & Usage

Before starting using our coding standard install [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer).

Clone or download this repo somewhere on your computer or install it with [Composer](http://getcomposer.org/).
To do so, add the dependency to your `composer.json` file by running `composer require magento-ecg/coding-standard`.

Add the standards directory to PHP_CodeSniffer installed paths:
```sh
$ phpcs --config-set installed_paths ./vendor/magento-ecg/coding-standard
```

Select a standard to run with CodeSniffer:

* Ecg for Magento
* EcgM2 for Magento 2

Run CodeSniffer:

```sh
$ phpcs --standard=Ecg /path/to/code
```
```sh
$ phpcs --standard=EcgM2 /path/to/code
```

PHP CodeSniffer will automatically scan Magento PHP files. To check design templates, you can specify `phtml` in the `--extensions` argument: `--extensions=php,phtml`.

# Requirements

PHP 5.4 and up.

Checkout the `php-5.3-compatible` branch to get the PHP 5.3 version.

# Contribution

Please feel free to contribute new sniffs or any fixes or improvements for the existing ones.
