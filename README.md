# Drupal distribution project

This project template should be used to start a new drupal project with the Ribote profile. 

## Usage

```
composer create-project daille-daille/ribote-project MY_PROJECT --stability dev --no-interaction
```
The `composer create-project` command passes ownership of all files to the 
project that is created. You should create a new git repository, and commit 
all files.

## Installing Drupal

You should update the `.env` file with your values.
Then install drupal using drush:
```shell
vendor/bin/drush si ribote \
  install_configure_form.enable_update_status_emails=NULL \
  install_configure_form.enable_update_status_module=false \
  install_configure_form.date_default_timezone=Europe/Paris \
  install_configure_form.site_default_country=FR
```

## Features & design choices

### robots.txt

Your project will have a robots-append.txt where you will be able to add custom indexation rules.
The robots.txt will be updated with drupal core and your rules during the composer-scaffolding step of a composer command.

### core-composer-scaffold dependency in the require-dev section

This choice has been made to avoid surprises during deployments.
You should commit the scaffolded files you want in production.
Of course, during production/pre-production deployments, you use the `composer install --no-dev` option.
