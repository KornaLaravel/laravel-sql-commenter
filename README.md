
[<img src="https://github-ads.s3.eu-central-1.amazonaws.com/support-ukraine.svg?t=1" />](https://supportukrainenow.org)

# SqlCommenter

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/laravel-sqlcommenter.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-sqlcommenter)
[![GitHub Tests Action Status](https://img.shields.io/github/workflow/status/spatie/laravel-sqlcommenter/run-tests?label=tests)](https://github.com/spatie/laravel-sqlcommenter/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/workflow/status/spatie/laravel-sqlcommenter/Check%20&%20fix%20styling?label=code%20style)](https://github.com/spatie/laravel-sqlcommenter/actions?query=workflow%3A"Check+%26+fix+styling"+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/spatie/laravel-sqlcommenter.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-sqlcommenter)

Augment your Laravel queries with comments in [SqlCommenter](https://google.github.io/sqlcommenter/) format.

SqlCommenter is compatible with [PlanetScale's Query Insights](https://docs.planetscale.com/concepts/query-insights).

**Before**

```mysql
select * from users
```

**After**

```mysql
select * from "users"/*controller='UsersController',action='index'*/;
```

## Support us

[<img src="https://github-ads.s3.eu-central-1.amazonaws.com/laravel-sqlcommenter.jpg?t=1" width="419px" />](https://spatie.be/github-ad-click/laravel-sqlcommenter)

We invest a lot of resources into creating [best in class open source packages](https://spatie.be/open-source). You can support us by [buying one of our paid products](https://spatie.be/open-source/support-us).

We highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address on [our contact page](https://spatie.be/about-us). We publish all received postcards on [our virtual postcard wall](https://spatie.be/open-source/postcards).

## Installation

You can install the package via composer:

```bash
composer require spatie/laravel-sqlcommenter
```

You can publish the config file with:

```bash
php artisan vendor:publish --tag="laravel-sqlcommenter-config"
```

This is the contents of the published config file:

```php
<?php

return [
    /**
     * Log the Laravel framework's version
     */
    'framework' => true,

    /**
     * Log which controller & action the query originated in
     * you can also enable logging of the full namespace
     * of the controller
     */
    'controller' => true,
    'controller_namespace' => false,

    /**
     * Log which route the query originated in
     */
    'route' => true,

    /**
     * Log which job the query originated in
     */
    'job' => true,
    'job_namespace' => false,

    /**
     * Log the db driver
     */
    'driver' => true,
];
```

## Usage

Configure which things you want to add to the SqlComments in the config file. After that, everything should work as expected.

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](https://github.com/riasvdv/.github/blob/main/CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [Rias](https://github.com/riasvdv)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
