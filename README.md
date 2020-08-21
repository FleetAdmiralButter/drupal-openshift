# Drupal 8.9.2 on OpenShift QuickStart

Drupal 8.9.2 LTS project ready to be deployed on OpenShift.\
S2I deploys the application with PHP 7.3 using the following image: https://github.com/sclorg/s2i-php-container/tree/master/7.3
Forks, issues, pull requests, and any other feedback welcome.


### Deploying
Deploy with:
```
oc new-project <your_project_name>
docker pull centos/php-73-centos7
oc new-app centos/php-73-centos7:latest~https://github.com/FleetAdmiralButter/drupal-openshift.git#master
```

This application will need a MySQL service to connect to.\
A standard MySQL service deployed via the built-in OpenShift template will suffice. Externally hosted databases will work too.

### Configuration
This project includes a php.ini which will get loaded by PHP automatically. You can add any required PHP configuration in there.\
This project's php.ini has already been set up to allow Drupal to work OOTB with the S2I builder.

### Included Modules:
- drupal/gin
- drupal/admin_toolbar
- drupal/gin_login
- drupal/field_group
- drupal/libraries
- drush

### Installing New Modules/Themes Before Deploying:
```
composer require 'drupal/somemodule:^3.0'
```

### Check out my Drupal.org profile:
https://www.drupal.org/u/fleetadmiralbutter

### TODO
- Remove the core/ folder so Composer takes care of scaffolding.

### ABOUT DRUPAL

Drupal is an open source content management platform supporting a variety of
websites ranging from personal weblogs to large community-driven websites. For
more information, see the Drupal website at https://www.drupal.org, and join
the Drupal community at https://www.drupal.org/community.
