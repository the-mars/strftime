[![GitHub license](https://img.shields.io/github/license/alphp/strftime)](https://github.com/alphp/strftime/blob/master/LICENSE)
[![GitHub release](https://img.shields.io/github/release/alphp/strftime)](https://github.com/alphp/strftime/releases)
[![Packagist](https://img.shields.io/packagist/v/php81_bc/strftime)](https://packagist.org/packages/php81_bc/strftime)
[![Packagist Downloads](https://img.shields.io/packagist/dt/php81_bc/strftime)](https://packagist.org/packages/php81_bc/strftime/stats)
[![GitHub issues](https://img.shields.io/github/issues/alphp/strftime)](https://github.com/alphp/strftime/issues)
[![GitHub forks](https://img.shields.io/github/forks/alphp/strftime)](https://github.com/alphp/strftime/network)
[![GitHub stars](https://img.shields.io/github/stars/alphp/strftime)](https://github.com/alphp/strftime/stargazers)

# strftime
Locale-formatted strftime using IntlDateFormatter (PHP 8.1 compatible)

This provides a cross-platform alternative to strftime() for when it will be removed from PHP.

Note that output can be slightly different between libc sprintf and this function as it is using ICU.

Original code: https://gist.github.com/bohwaz/42fc223031e2b2dd2585aab159a20f30

Original autor: [BohwaZ](https://bohwaz.net/)

# Requirements
- PHP >= 5.6
- ext-intl ([Internationalization extension ICU](https://www.php.net/manual/en/book.intl.php))

# Installation

## Composer install
You can install this plugin into your application using [composer](https://getcomposer.org):

- Add php81_bc/strftime package to your project:
  ```bash
    composer require php81_bc/strftime
  ```

- Load the function PHP81_BC\strftime in your project
  ```php
  <?php
    require 'vendor/autoload.php';
    use function PHP81_BC\strftime;
  ```

## Manual install
- Download [php-8.1-strftime.php](https://github.com/alphp/strftime/raw/master/src/php-8.1-strftime.php) and save it to an accessible path of your project.
- Load the function PHP81_BC\strftime in your project
  ```php
  <?php
    require 'php-8.1-strftime.php';
    use function PHP81_BC\strftime;
  ```

# Usage
```php
  use function PHP81_BC\strftime;
  echo strftime('%A %e %B %Y %X', new \DateTime('2021-09-28 00:00:00'), 'fr_FR');
```

## Original use
```php
  \setlocale('fr_FR.UTF-8', LC_TIME);
  echo \strftime('%A %e %B %Y %X', strtotime('2021-09-28 00:00:00'));
```
