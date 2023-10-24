# Ansible Role: Grafana

This Ansible role automates the installation and configuration of Grafana on your servers. Grafana is an open-source platform for monitoring and observability, allowing you to create customizable dashboards and visualize data from various data sources.

## Table of Contents

- [Role Features](#role-features)
- [Requirements](#requirements)
- [Role Variables](#role-variables)
- [Dependencies](#dependencies)


## Role Features

This role provides the following features:

- Installation of Grafana on the target server.
- Configuration of Grafana's systemd service.
- Waiting for Grafana to be up and running.
- Changing the admin password for the Grafana GUI.

## Requirements

Before using this role, ensure that:

- You have a target server where you want to install Grafana.
- You have Ansible installed on your local machine.

## Role Variables

The role uses the following variables, which you can customize in your playbook:

- `grafana_admin_password`: Set the admin password for Grafana.

## Dependencies

This role doesn't have any specific role dependencies.

## Example Playbook

Here's an example playbook that uses this role:

```yaml
- hosts: your_target_hosts
  become: yes
  vars:
    grafana_admin_password: YourSecurePassword
  roles:
    - grafana
