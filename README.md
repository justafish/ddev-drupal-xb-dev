# ddev-drupal-xb-dev

This is a DDEV addon for doing Drupal Experience Builder development.

1. Follow these instructions to install `justafish/ddev-drupal-core-dev` https://github.com/justafish/ddev-drupal-core-dev?tab=readme-ov-file#ddev-core-dev
2. Launch your site
  ```
  ddev launch
  ```
3. Install Experience Builder
  inside your Drupal core checkout:
  ```
  git clone git@git.drupal.org:project/experience_builder.git modules/contrib/experience_builder
  ddev add-on get justafish/ddev-drupal-xb-dev
  ```
4. Enable the test module to develop Experience Builder on top of the Standard install profile
  ```
  ddev drupal test:extensions-enable
  ddev drupal module:install xb_dev_standard
  ```
5. Run the Cypress tests
  ```
  ddev xb-npm run cy:run
  ```
