# Ansible Role: Drupal Console

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-drupal-console.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-drupal-console)

Installs [Drupal Console](http://drupalconsole.com/) on any Linux or UNIX system.

## Requirements

`curl` and `php` (version 5.4+) should be installed and working.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    drupal_console_path: /usr/local/bin/composer

The path where Drupal Console will be installed and available to your system. Should be in your user's `$PATH` so you can use Drupal Console by entering `drupal` instead of the full path.

    drupal_console_keep_updated: true

By default, this role will always update Drupal Console to the latest version whenever it's run. If you'd like to change this behavior, switch this variable to `false`.

    drupal_console_config: ~/.console

The path to the Drupal Console configuration file.

## Dependencies

  - geerlingguy.php (Installs PHP).

## Example Playbook

    - hosts: servers
      roles:
        - { role: geerlingguy.drupal-console }

After the playbook runs, `drupal` will be placed in `/usr/local/bin/drupal` (this location is configurable), and will be accessible via normal system accounts.

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
