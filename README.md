# Drupal 8.9.2 on OpenShift QuickStart

Drupal 8.9.2 LTS project ready to be deployed on OpenShift.
Forks, issues, pull requests welcome.

Deploy with:
```
oc new-project <your_project_name>
oc new-app php~https://github.com/FleetAdmiralButter/drupal-openshift.git#master
```

### Included Modules:
- drupal/gin
- drupal/admin_toolbar
- drupal/gin_login
- drupal/field_group
- drupal/libraries
- drush


### ABOUT DRUPAL

Drupal is an open source content management platform supporting a variety of
websites ranging from personal weblogs to large community-driven websites. For
more information, see the Drupal website at https://www.drupal.org, and join
the Drupal community at https://www.drupal.org/community.

Legal information about Drupal:
 * Know your rights when using Drupal:
   See LICENSE.txt in the "core" directory.
 * Learn about the Drupal trademark and logo policy:
   https://www.drupal.com/trademark
