# Drupal: Export config

## Roles

* Web developer: This requires command-line access and the ability to issue a pull request against the git repository.

## Steps

We have made changes to Drupal's configuration in our local environment, and now we need to capture those in our VCS. In Drupal 8, we do this using the config management system. There are a couple of ways to export our configuration to code, but the method we prefer on developers.redhat.com is using `drush`.

* Execute `./vendor/bin/drush config-export`
* This will export the changes we've made to YAML files that we can commit to Git and include in a pull request that will now include all of the changes required to create this assembly type

## Deliverables

* We have created a pull request that includes all of the FE changes and export YAML config required to create this assembly type

[Previous page](./3-adding-assembly-reference-fields.md)
[Next page](./5-creating-assembly-content.md)
