# Drupal Skeleton documentation

Overview off all Skeleton Documentation:

## Quick Start
- [Quick start](quick-start.md) : Short guide to get you started within minutes.

## Requirements
- [Requirements](requirements.md) : Minimal requirments to use the
  drupal-skeleton.

## Commands
- [bin/install](command-install.md) : Install the project.
- [bin/reset](command-reset.md) : Reset an existing project back to the
  fresh-installed state.
- [bin/upgrade](command-upgrade.md) : Upgrade an existing project by downloading
  core & contributed as defined in the make files, and update drupal by running
  `drush updb` command afterwards.
- [bin/build](command-build.md) : Create a package of the project ready to be
  deployed on production.
- [bin/backup](command-backup.md) : Create a backup of the installed project.
- [bin/restore](command-restore.md) : Restore one of the backups.


## Configuration
- [config](config.md) : The structure of the `config` directory.
- [config.sh](config-config.md) : The global configuration file.
- [make files](config-make.md) : How to add contrib modules, themes and
  libraries using the make file configuration.
- [modules](config-modules.md) : Enable and Disable modules during install and
  reset.
- [cleanup](config-cleanup.md) : Delete directories and files when the `web`
  directory is (re)build.


## Hooks
- [hook system](hooks.md) : More information about the hook system: add
  your own script steps before and/or after the existing command steps.
- [hook helpers](hooks-helpers.md) : Overview of all helper functions that can
  be used when writing hooks.
- [predefined variables](hooks-variables.md) : Overview of all variables that
  can be accessed and used when writing hooks.


## Project
- [project](project.md) : Add custom install profiles, modules, themes and
  libraries to the project.


## Editor (IDE)
- [Editor setup](editor.md) : Info how to setup your editor (IDE).
