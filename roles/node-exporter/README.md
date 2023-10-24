# Ansible Role: Node Exporter

This Ansible role automates the installation and configuration of Node Exporter on your servers. Node Exporter is a Prometheus exporter that exposes system-level metrics.

## Table of Contents

- [Role Features](#role-features)
- [Requirements](#requirements)
- [Role Variables](#role-variables)
- [Dependencies](#dependencies)
- [Example Playbook](#example-playbook)

## Role Features

This role provides the following features:

- Checks if Node Exporter is already installed.
- Creates a system user for Node Exporter.
- Downloads and installs Node Exporter if it's not already present or if the version is different.
- Creates a systemd service for Node Exporter.
- Ensures that the Node Exporter service is enabled and started.

## Requirements

Before using this role, ensure that:

- You have a target server where you want to install Node Exporter.
- You have Ansible installed on your local machine.

## Role Variables

The role uses the following variables, which you can customize in your playbook:

- `node_exporter_bin`: Path to the Node Exporter binary.
- `node_exporter_user`: User for running Node Exporter.
- `node_exporter_dir_conf`: Directory for Node Exporter configuration.
- `node_exporter_group`: Group for Node Exporter.
- `node_exporter_version`: Version of Node Exporter to install.

## Dependencies

This role doesn't have any specific role dependencies.

## Example Playbook

Here's an example playbook that uses this role:

```yaml
- hosts: your_target_hosts
  become: yes
  vars:
    node_exporter_bin: /usr/local/bin/node_exporter
    node_exporter_user: node_exporter
    node_exporter_dir_conf: /etc/node_exporter
    node_exporter_group: node_exporter
    node_exporter_version: 1.2.3  # Specify the desired version
  roles:
    - node-exporter
