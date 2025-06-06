<!--
SPDX-FileCopyrightText: 2023 Slavi Pantaleev

SPDX-License-Identifier: AGPL-3.0-or-later
-->

# prometheus_postgres_exporter

This is an [Ansible](https://www.ansible.com/) role which installs [Prometheus Postgres Exporter](https://github.com/prometheus-community/postgres_exporter) to run as a [Docker](https://www.docker.com/) container wrapped in a systemd service.

This role *implicitly* depends on:

- [`com.devture.ansible.role.playbook_help`](https://github.com/devture/com.devture.ansible.role.playbook_help)
- [`com.devture.ansible.role.systemd_docker_base`](https://github.com/devture/com.devture.ansible.role.systemd_docker_base)

> **NOTE**: check [defaults/main.yml](./defaults/main.yml) to see full list of config options

## Integrate with Grafana

You can use the dashboard [9628](https://grafana.com/grafana/dashboards/9628-postgresql-database/) to visualize the data in Grafana. The variable `prometheus_postgres_exporter_dashboard_urls` might help you.

![A grafana dashboard showing connection data, commits to the database and more](assets/grafana_screenshot.jpeg)

## Development

You can optionally install [pre-commit](https://pre-commit.com/) so that simple mistakes are checked and noticed before changes are pushed to a remote branch. See [`.pre-commit-config.yaml`](./.pre-commit-config.yaml) for which hooks are to be executed.

See [this section](https://pre-commit.com/#usage) on the official documentation for usage.
