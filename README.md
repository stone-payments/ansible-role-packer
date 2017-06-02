# Ansible Role: packer

[![Build Status](https://travis-ci.org/bramford/ansible-role-packer.svg?branch=master)](https://travis-ci.org/bramford/ansible-role-packer)

Ansible role that installs packer from releases.hashicorp.com

## Supported Operating Systems

*Any GNU/Linux operating system* with `unzip`

## Requirements

- Ansible 2.1+
- Make sure that the "packer_install_directory" are in your environment path.

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { packer }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with optional vars set
      hosts: all
      roles:
        - { packer,
            packer_version: 1.0.0,
            packer_install_directory: "/opt/packer"
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/{{username}}/{{repository}}.git roles/packer
