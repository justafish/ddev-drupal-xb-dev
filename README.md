# ddev-drupal-xb-dev

This is a DDEV addon for doing Drupal Experience Builder development.

- Follow [these instructions](https://github.com/justafish/ddev-drupal-core-dev?tab=readme-ov-file#installation) to install `justafish/ddev-drupal-core-dev`
- Run the installer
  ```
  ddev drupal install standard
  ```
- Install Experience Builder

  inside your Drupal core checkout:
  ```
  git clone git@git.drupal.org:project/experience_builder.git modules/contrib/experience_builder
  ddev add-on get justafish/ddev-drupal-xb-dev
  ```
- Enable the test module to develop Experience Builder on top of the Standard install profile
  ```
  ddev drupal test:extensions-enable
  ddev drupal module:install xb_dev_standard
  ```
- Run the Cypress tests
  ```
  ddev xb-npm run cy:run
  ```
