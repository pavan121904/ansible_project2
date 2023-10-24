# Ansible Role: Prometheus

This Ansible role automates the installation and configuration of Prometheus on your servers. Prometheus is an open-source monitoring and alerting toolkit.

## Table of Contents

- [Role Features](#role-features)
- [Requirements](#requirements)
- [Role Variables](#role-variables)
- [Dependencies](#dependencies)
- [Example Playbook](#example-playbook)

## Role Features

This role provides the following features:

- Installs Prometheus on the target server.
- Configures Prometheus with custom arguments.
- Manages Prometheus configuration files.
- Ensures the Prometheus service is enabled and started.

## Requirements

Before using this role, ensure that:

- You have a target server where you want to install Prometheus.
- You have Ansible installed on your local machine.

## Role Variables

The role uses the following variables, which you can customize in your playbook:

- `prometheus_dir_configuration`: Directory where Prometheus configuration files are stored.

## Dependencies

This role doesn't have any specific role dependencies.

## Example Playbook

Here's an example playbook that uses this role:

```yaml
- hosts: your_target_hosts
  become: yes
  vars:
    prometheus_dir_configuration: /etc/prometheus  # Specify the directory where Prometheus configuration files will be stored
  roles:
    - prometheus
