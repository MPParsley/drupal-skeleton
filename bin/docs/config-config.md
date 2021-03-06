# config.sh
The `config.sh` file contains the global configuration for the project. It is
specific for the environment where the scripts are run (eg. local development,
test, acceptance, production, ...).

> **Warning** : Don't include this file in the versioning system as it is
> environment specific!

Use the `config_example.sh` script to give an example of the expected
configuration variables.

**This is the only required file within the `config` directory.**

The config file contains by default a minimal set of configuration variables.
Feel free to add your own extra variables as required by the implemented
[command hooks][link-hooks].



## Default configuration variables
The default config file contains following variables:


#### Site information
Information about the platform:

- **SITE_NAME** : The name of the site that will be installed. This name will be
  used in the output of the commands as well as settings the drupal site name
  when the platform is installed (`$SITE_NAME`).
- **SITE_URL** : The URL where the platform can be accessed after installation.
  This is used by the login step in the commands to open a browser and login to
  the platform (`$SITE_URL`).
- **SITE_PROFILE** : The drupal install profile to use when installing the
  platform. This is by default the *standard* profile (`$SITE_PROFILE`).


#### Database specific variables
A drupal installation requires a database, set the database connection
parameters in the `config.sh` file.

> **Noot** : the script will not create the database for you, add it manually
> to the database server.

- **DB_HOST** : The database hostname or IP address (`$DB_HOST`).
- **DB_USER** : The database username (`$DB_USER`).
- **DB_PASS** : The database password (`$DB_PASS`).
- **DB_NAME** : The database name (`$DB_NAME`).


#### The administration account
When a new installation is run, an administration account is created using the
credentials from the config file:

- **ACCOUNT_NAME** : The administration account (login) name (`$ACCOUNT_NAME`).
- **ACCOUNT_PASS** : Tha administration account password (`$ACCOUNT_PASS`).
- **ACCOUNT_MAIL** : The email address of the administration account
  (`$ACCOUNT_MAIL`). This is by default created using the account name and the
  site url (`$ACCOUNT_NAME@$SITE_URL`).



## Example config file

```
# The name of the site.
SITE_NAME="Drupal Skeleton"

# URL where the site is hosted.
SITE_URL="drupal-skeleton.sg"

# The install profile that shouls be installed.
SITE_PROFILE="standard"

# Database connection parameters.
DB_USER="localuser"
DB_PASS="localpass"
DB_NAME="drupal_skeleton"
DB_HOST="localhost"

# Administrator account (user 1).
ACCOUNT_NAME="admin"
ACCOUNT_PASS="drupal"
ACCOUNT_MAIL="$ACCOUNT_NAME@$SITE_URL"
```



[Back to overview][link-overview]



[link-hooks]: hooks.md

[link-overview]: README.md
