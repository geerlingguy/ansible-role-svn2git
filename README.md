# Ansible Role: KDE's Svn2Git

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-svn2git.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-svn2git)

Installs [KDE's Svn2Git](https://techbase.kde.org/Projects/MoveToGit/UsingSvn2Git), a tool for quickly and easily converting SVN repositories to Git repositories, on any RHEL/CentOS or Debian/Ubuntu Linux system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    workspace: /root

Where certain files will be downloaded and built for git2svn installation.

    svn2git_source_repo: https://github.com/svn-all-fast-export/svn2git.git
    svn2git_source_version: master

The source repository and version (git branch, tag, or commit hash) from which svn2git's code will be cloned.

    svn2git_install_path: /usr/local/share

The location where svn2git will be installed.

    svn2git_qmake_bin_path: /usr/lib64/qt4/bin/qmake

The path to the `qmake` binary executable. This could differ slightly based on where QT is installed on your system.

## Dependencies

  - `geerlingguy.svn`
  - `geerlingguy.git`

## Example Playbook

    - hosts: servers
      roles:
        - geerlingguy.svn
        - geerlingguy.git
        - geerlingguy.svn2git

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](https://www.jeffgeerling.com/), author of [Ansible for DevOps](http://www.ansiblefordevops.com/).
