---
title: How to Build
nextjs:
  metadata:
    title: How to build plugin
    description: Learn how to build a plugin in Aikeedo.
---

In this guide, you will learn how to build a plugin in Aikeedo. Plugins are essential tools that enhance the functionality of your Aikeedo platform. By building a plugin, you can customize your platform to meet your specific requirements and provide a seamless user experience. {% .lead %}

We're going to build a simple plugin that adds an integration with [CurrencyBeacon](https://currencybeacon.com) to your Aikeedo platform. This plugin will add the Currency Beacon as an alternative currency rate provider to your platform.

## Prerequisites

This tutorial assumes that you have a basic understanding of PHP and Composer. You should also have a local development environment set up for Aikeedo.

## Step 1: Create a new plugin

To create a new plugin, you need to create a new directory in the `/public/content/plugins` directory of your Aikeedo platform with the following structure: `yourorganization/plugin-name`. We will name our plugin `heyaikeedo/currency-beacon`.

```bash
mkdir -p public/content/plugins/heyaikeedo/currency-beacon
```

## Step 2: Create the composer.json file for the plugin

{% callout type="note" %}
Each plugin in Aikeedo is a Composer package thus it requires a `composer.json` file. The `composer.json` file contains metadata about the plugin, such as its name, description, and dependencies.
{% /callout %}

Next, create a `composer.json` file in the `public/content/plugins/heyaikeedo/currency-beacon` directory with the following content:

```json
{
  "name": "heyaikeedo/currency-beacon",
  "type": "aikeedo-plugin",
  "require": {
    "heyaikeedo/composer": "^1.0.0"
  },
  "extra": {
    "entry-class": "Aikeedo\\CurrencyBeacon\\Plugin"
  }
}
```

This is minimal `composer.json` file required for an Aikeedo plugin. It specifies the name of the plugin, its type, and the required `heyaikeedo/composer` package. The `heyaikeedo/composer` package is a special Composer package that provides additional functionality for Aikeedo plugins and it must be required by all Aikeedo plugins.

Pay attention to the `type` field in the `composer.json` file. The `type` field must be set to `aikeedo-plugin` for Aikeedo plugins.

Name of the plugin in the `composer.json` file must match the path to the plugin directory in the `/public/content/plugins` directory. Its format is `yourorganization/plugin-name`. Its required to uniquely identify the plugin. In our case, the name of the plugin is `heyaikeedo/currency-beacon` and the path to the plugin directory is `public/content/plugins/heyaikeedo/currency-beacon`.

## Step 3: Define version constraints

Only stable packages are allowed to be installed in Aikeedo by default. So we need to define the version constraints for our plugin in the `composer.json` file. We can do this by adding the `version` field to the `composer.json` file.

```json
{
  "name": "heyaikeedo/currency-beacon",
  "type": "aikeedo-plugin",
  "version": "1.0.0",
  "require": {
    "heyaikeedo/composer": "^1.0.0"
  },
  "extra": {
    "entry-class": "Aikeedo\\CurrencyBeacon\\Plugin"
  }
}
```

Our plugin can now be installed as a Composer package using the `composer require` command. However, it won't do anything yet because we haven't created the plugin class yet. Also, the app will throw an error as it won't be able to find the plugin class.

## Step 3: Create the plugin class

Next, create the plugin class in the `src/Plugin.php` file of the plugin directory. The plugin class must implement the `Plugin\Domain\PluginInterface` interface. Currently the `PluginInterface` interface defines only one method `boot` which is called when the plugin is loaded by the Aikeedo platform.

```php
<?php

declare(strict_types=1);

namespace Aikeedo\CurrencyBeacon;

use Override;
use Plugin\Domain\Context;
use Plugin\Domain\PluginInterface;

class Plugin implements PluginInterface
{
    #[Override]
    public function boot(Context $context): void
    {
        // Implementation details are omitted
        // You can find the full implementation in folllowing git repository:
        // https://github.com/heyaikeedo/plugins-currency-beacon
    }
}
```

## Step 4: Setup autoloading

One final step is to setup autoloading for the plugin. You can do this by adding autoloading configuration to the `composer.json` file of the plugin.

```json
{
  "name": "heyaikeedo/currency-beacon",
  "type": "aikeedo-plugin",
  "version": "1.0.0",
  "require": {
    "heyaikeedo/composer": "^1.0.0"
  },
  "extra": {
    "entry-class": "Aikeedo\\CurrencyBeacon\\Plugin"
  },
  "autoload": {
    "psr-4": {
      "Aikeedo\\CurrencyBeacon\\": "src/"
    }
  }
}
```

## Step 5: Install the plugin

Now that you have created the plugin, you can install it using the `composer require` command. Run the following command in the root directory of your Aikeedo platform:

```bash
composer require heyaikeedo/currency-beacon
```

This will install the plugin and its dependencies. Once the plugin is installed, you can enable it in the Aikeedo dashboard.

`composer.json` file may include additional fields and configurations depending on the requirements of the plugin. You can find more information about the `composer.json` file in the [Composer documentation](https://getcomposer.org/doc/04-schema.md). Also can also add several extra fields such as title, description etc. to the `composer.json` file to provide additional information about the plugin. This additional information may be used by the Aikeedo dashboard to display information about the plugin.

You can find the full implementation of the `CurrencyBeacon` plugin in the following git repository: [https://github.com/heyaikeedo/plugins-currency-beacon](https://github.com/heyaikeedo/plugins-currency-beacon)

If you have any questions or need assistance, feel free to [reach out to our support team](mailto:support@aikeedo.com).
