# ddev-drupal-xb-dev

This is a DDEV addon for doing Drupal Experience Builder development.

- Follow [these instructions](https://github.com/justafish/ddev-drupal-core-dev?tab=readme-ov-file#installation) to install `justafish/ddev-drupal-core-dev`
- Clone Experience Builder inside your Drupal core checkout:
  ```
  git clone git@git.drupal.org:project/experience_builder.git modules/contrib/experience_builder
  ```
- Install this add-on
  ```
  ddev add-on get justafish/ddev-drupal-xb-dev
  ```
- Run the installer
  ```
  ddev drupal install standard
  ddev launch
  ```
- Enable Experience Builder
  ```
  ddev drupal module:install experience_builder
  ```
- Enable the test module to develop Experience Builder on top of the Standard install profile
  ```
  ddev drupal test:extensions-enable
  ddev drupal module:install xb_dev_standard
  ```
- Visit [`https://drupal.ddev.site/node/add/article`](https://drupal.ddev.site/node/add/article) and save an article (just filling out the title is enough)
- In the toolbar, click "Experience Builder" 🥳
- Run the Cypress tests
  ```
  ddev xb-npm run cy:run
  ```
