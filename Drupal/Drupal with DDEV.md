## Configure your local development environment to serve your application

Replace `my-site` with a machine-friendly (no spaces or special punctuation) name for your new application and run the following command (assumes DDEV):

```php
mkdir my-site
cd my-site
ddev config --docroot web --project-name my-site --project-type drupal10 --create-docroot
```

This will create a new DDEV project configured to host a Drupal application. DDEV will store the generated configuration in a new `.ddev` subdirectory.

Next, start the DDEV container

```php
ddev start
```

You now have a web server and database server configured and running. Configuring DDEV first allows us to run Composer from within DDEV instead of installing it locally.

## Create a new Drupal application

Next, use [Composer](https://getcomposer.org/download/) to install Drupal, which enables you to install and update dependencies (modules, themes, profiles, libraries, etc.) also with Composer. It is best practice to [ensure that your entire Drupal application is managed with Composer](https://www.drupal.org/docs/develop/using-composer/using-composer-to-manage-drupal-site-dependencies) in order to facilitate manageable upgrades.

Now create a new Drupal application with Composer. Note: `ddev composer create` will unpack and download the files into the current folder, unlike `composer create-project` which downloads Drupal into a separate folder.

```php
ddev composer create drupal/recommended-project
```

Next install the latest version of Drush, a command-line utility for Drupal.

```php
ddev composer require drush/drush
```

It is possible to install Drupal with Composer without using the DDEV environment, but not recommended, since PHP versions in DDEV and your local environment may differ.

```php
composer create-project drupal/recommended-project
```

You now have a web server and database server configured and running.

## Install Drupal

Next, you must install Drupal using Drush, which populates your Drupal application’s new database.

Using DDEV and Drush, execute the command below. Replace `my-password` with the password that you would like to use for the [admin (user 1) account](https://www.drupal.org/docs/user_guide/en/user-admin-account.html).

```php
ddev drush site:install --account-name=admin --account-pass=my-password
```

Drupal is now installed.

## Log In

Finally, launch your new Drupal site and log in.

```php
ddev launch
```

You can also generate a one-time login link.

```php
ddev drush user:login
```

If necessary, execute `ddev describe` to view the URL of your site. Copy and paste that URL into your web browser to visit it.

Log in to the site using the `--account-name` and `--account-pass` you specified in the previous section ([the section called “Install Drupal”](https://www.drupal.org/docs/official_docs/en/_local_development_guide.html#install_drupal "Install Drupal")).

## Next steps

What now?

Learn how you can begin to extend and customize your new Drupal application. Visit the [Drupal User Guide](https://www.drupal.org/docs/user_guide/en/index.html) and read the following chapters:

- [Chapter 4. Basic Site Configuration](https://www.drupal.org/docs/user_guide/en/config-chapter.html)
- [Chapter 5. Basic Page Management](https://www.drupal.org/docs/user_guide/en/content-chapter.html)
- [Chapter 6. Setting Up Content Structure](https://www.drupal.org/docs/user_guide/en/content-structure-chapter.html)

## Appendix

We chose to use DDEV for this local development guide because it met the following criteria:

1. Must be free and open source, without tying users into a proprietary product or service.
2. Must be well maintained, with long term support.
3. Must follow Drupal best practices.
4. Must be compatible with MacOS, Windows, and Linux.
5. Must be as simple as possible
    
    1. Fewest pre-requisites
    2. Fewest manual steps
    

To suggest a different local development solution, please create an issue in the [Official Docs issue queue](https://www.drupal.org/project/issues/official_docs?categories=All).

## Related Content

## [Development tools](https://www.drupal.org/docs/develop/development-tools)

Commonly used tools to aid in Drupal development