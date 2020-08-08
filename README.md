# wp-composer
Examples for installing plugins and themes with, composer on WordPress.

`plugin.json` Needs to be added to the private plugin directory
`theme.json` Needs to be added to the private theme directory

The below needs to be added to the WordPress main `composer.json` file.

For each new plugin or theme added, you will need to add a new `vsc` repository.
```
    {
      "type": "vcs",
      "url": "https://github.com/WP-Funnel-Hackers/new-private-wordpress-plugin.git"
    },
```

```
  "repositories": [
    {
      "type": "composer",
      "url": "https://wpackagist.org",
      "only": ["wpackagist-plugin/*", "wpackagist-theme/*"]
    },
    {
      "type": "vcs",
      "url": "https://github.com/WP-Funnel-Hackers/private-wordpress-plugin-1.git"
    },
    {
      "type": "vcs",
      "url": "https://github.com/WP-Funnel-Hackers/private-wordpress-plugin-2.git"
    }
```
Then to install run

```
composer require WP-Funnel-Hackers/private-wordress-plugin
```
