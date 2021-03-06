# Contributing

The project follows the [Open Knowledge International coding standards](https://github.com/okfn/coding-standards).

All PHP Code MUST conform to [PHP-FIG](http://www.php-fig.org/psr/) accepted PSRs.

Flow Framework has a nice guide regarding coding standards:
* [Printable summary of most important coding guidelines on one page **(.pdf)**](http://flowframework.readthedocs.io/en/stable/_downloads/Flow_Coding_Guidelines_on_one_page.pdf)
* [The full guide **(.html)**](http://flowframework.readthedocs.io/en/stable/TheDefinitiveGuide/PartV/CodingGuideLines/PHP.html)


## Getting Started

1. Clone the repo
2. Run the tests
```
$ composer install
$ composer test
```


## Phpunit - for unit tests

[![Travis](https://travis-ci.org/frictionlessdata/datapackage-php.svg?branch=master)](https://travis-ci.org/frictionlessdata/datapackage-php)

Phpunit is used for unit tests, you can find the tests under tests directory

Running Phpunit directly: `vendor/bin/phpunit --bootstrap tests/autoload.php tests/`


## Coveralls - for coverage

[![Coveralls](http://img.shields.io/coveralls/frictionlessdata/datapackage-php.svg?branch=master)](https://coveralls.io/r/frictionlessdata/datapackage-php?branch=master)

when running `composer test` phpunit generates coverage report in coverage-clover.xml - this is then sent to Coveralls via Travis.


## Scrutinizer-ci - for code analysis

[![Scrutinizer-ci](https://scrutinizer-ci.com/g/OriHoch/datapackage-php/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/OriHoch/datapackage-php/)

Scrutinizer-ci integrates with GitHub and runs on commits.

It does static code analysis and ensure confirmation to the coding stnadards.

At the moment, the integration with frictionlessdata repo is not working, you can setup a Scrutinizer-ci account for your fork and run against that.

## php-cs-fixer - code style check & autofix

[php-cs-fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) can be used to check and fix code style

you need to manually install it, then you can run : `composer style-check` or `composer style-fix`

## Publishing a release and updating Packagist

[![Packagist](https://img.shields.io/packagist/dm/frictionlessdata/datapackage.svg)](https://packagist.org/packages/frictionlessdata/datapackage)
[![SemVer](https://img.shields.io/badge/versions-SemVer-brightgreen.svg)](http://semver.org/)

* Publish a release (using SemVer) on GitHub
* go to https://packagist.org/packages/frictionlessdata/datapackage
* Login with GitHub which has permissions
* click "Update"
* all releases from GitHub appear as releases on Packagist

## updating frictionlessdata schemas

The json schemas for the frictionlessdata specs are stored locally as part of the package.

They might change from time to time, to donwnload the latest specs run `composer update_registry`
