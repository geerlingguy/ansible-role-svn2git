# Ansible Role: KDE's Svn2Git

Installs KDE's Svn2Git, a tool for quickly and easily converting SVN repositories to Git repositories, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    workspace: /root

Where certain files will be downloaded and built for git2svn installation.

## Dependencies

  - geerlingguy.svn
  - geerlingguy.git

## Example Playbook

    - hosts: servers
      roles:
        - { role: geerlingguy.git }

## License

MIT / BSD

## Author Information

This role was created in 2014 by Jeff Geerling (@geerlingguy), author of Ansible for DevOps. You can find out more about the book at http://ansiblefordevops.com/, and learn about the author at http://jeffgeerling.com/.
