# Pragmatic PHP Coding Standards
__A project by [Pragmatic](https://pragmatic.agency).__

<p>
	<img alt="Version 0.0.1" src="https://img.shields.io/badge/version-0.0.1-blue.svg?cacheSeconds=86400" />
	<img alt="License: GPL 3.0 only" src="https://img.shields.io/badge/License-GPL--3.0--only-yellow.svg" />
</p>


> Style guide for writing consistent PHP code for WordPress projects.

## Installation

Our PHP coding standards are enforced via [php_codesniffer](https://packagist.org/packages/squizlabs/php_codesniffer) and can be installed using the PHP package manager [composer](https://getcomposer.org/).

```bash
$ composer require pragmaticweb/php-coding-standards --dev
```

## Usage

### Basic usage

When installed using composer, our coding standards are ready to be used by running:

```bash
$ vendor/bin/phpcs --standard="Pragmatic" ./my-plugin ./my-file.php
```

### Configuration file

In order to make it easier to modify our standards to better fit your project, you can create a `phpcs.xml.dist` file which could contain something like this:

```xml
	<?xml version="1.0"?>
	<ruleset name="MyProjectCodingStandard">

		<description>My Project coding standard.</description>

		<file>./my-plugin</file>
		<file>./my-file.php</file>

		<config name="text_domain" value="my-project"/>

		<rule ref="Pragmatic" />

	</ruleset>
```

Using a config file, allows you to only run `vendor/bin/phpcs` to check the code style.

For more advanced usage, please refer to the [PHP Codesniffer docs](https://github.com/squizlabs/PHP_CodeSniffer/wiki).

## Included rules

### WordPress Coding Standard

We're pretty much using WordPress coding standards at this point with some exclusions (see `ruleset.xml`).

See https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards.

### PHPcompatibilityWP

It allows to analyse code for compatibility with higher and lower versions of PHP. The default target version is PHP 7.0+.

Target version can be changed via custom `phpcs.xml`.

See https://github.com/PHPCompatibility/PHPCompatibilityWP

### PSR2

See https://github.com/php-fig-rectified/psr2r-sniffer

## Contributing

The Pragmatic coding standards is what enables our engineers to work together and write consistent PHP code.

Pull requests are welcome but will need to be reviewed by the members of our team.

Please open an issue first to discuss what you would like to change and, if our team agrees with it, then we could look into merging them.
