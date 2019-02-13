# Microserve Contribution Day

A Docksal based local environment for our Drupal contribution days at [Microserve](https://microserve.io).

It includes commonly used Docksal addons, and automates common tasks like cloning Drupal core, copying and changing settings files and setting up SimpleTest for running automated tests.
This should simplify and speed up the setup process, allowing more time for people to focus on contribution tasks.

## Prerequisites

- [Docksal](https://docksal.io)
- [Git](https://git-scm.com)

## Local setup

1. Clone the repository into a local directory, specifying the directory name and the Drupal version.

    ```
    git clone https://github.com/microserve-io/contribution-day.git --branch 7.x drupal7
    ```

1. Go into the `drupal7` directory.

1. Run the `fin init` command. This will start the Docksal containers, clone the specified version of core, copy in the static files, and run `drush site-install`.

   Drupal itself will be cloned into a `drupal` directory. Ensure that you are within this directory when creating patch files.

1. Visit http://drupal7.docksal in your browser.

1. To run automated tests, use the `fin simpletest` command.

## License

MIT
