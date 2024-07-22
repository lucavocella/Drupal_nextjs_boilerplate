# Nextjs boilerplate with docker-compose

This example contains everything needed to get a Drupal development environment up and running with DDEV.
The drupal installation is super clean, no modifications has been applied.

## Benefits of Docker

- You don't need to run/install Drupal and all services needed in your local environment ✨
- The environment will be the same accross any OS
- You can run multiple environments with different configuration

## Prerequisites

Install [Docker Desktop](https://docs.docker.com/get-docker) for Mac, Windows, or Linux. Docker Desktop includes Docker Compose as part of the installation.
Install [DDEV](https://ddev.com/get-started/)

## How to use

```bash
cd backend
ddev start
ddev composer create drupal/recommended-project:^10
ddev config --update
ddev composer require drush/drush
ddev drush site:install --account-name=admin --account-pass=admin -y
# use the one-time link (CTRL/CMD + Click) from the command below to edit your admin account details.
ddev drush uli
ddev launch
```

## Useful commands

Enter php container
```bash
ddev sh
```

Using Drush
```bash
ddev drush [command name]
```

## Read more about ddev
[DDEV website](https://ddev.com/get-started/)

Pay attention: for better performance on windows when you install docker with wsl remember to locate the project folder in the wsl container and not under windows folders.