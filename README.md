# grafana-awesome

> an awesome-style list of tools and resources for Grafana

## Contents

- [backing up and searching Grafana](#backing-up-and-searching-grafana)
- [grafana.db database migration](#migrating-grafanadb-database)
- [dashboard exporting and syncing](#dashboards-as-code-or-dashboard-syncing)
- [reporting](#reporting)
- [alerting](#alerting)
- [plugin development](#plugin-development)
- [data source specific](#data-source-specific)
    - [SQL databases (MySQL, MSSQL, Postgres, etc)](#sql-databases)
    - [Prometheus](#prometheus)

## backing up and searching Grafana

- [ysde/grafana-backup-tool](https://github.com/ysde/grafana-backup-tool)
    - A Python-based application to back up Grafana settings using the Grafana API

- [panodata/grafana-wtf](https://github.com/panodata/grafana-wtf)
    - Grep through all Grafana entities in the spirit of `git-wtf`.

- [Grafana extension for Raycast](https://github.com/raycast/extensions/tree/main/extensions/grafana)
    - Search your dashboard inside [Raycast](https://www.raycast.com/).

## migrating grafana.db database

- [grafana/database-migrator](https://github.com/grafana/database-migrator)
    - This script dumps data from a grafana sqlite database in a format that works with MySQL. It is intended to assist in migrating Grafana instances from the default sqlite database (grafana.db) to MySQL (or a MySQL-compatible DB like MariaDB).

## dashboards-as-code or dashboard syncing

### tools

- [Gist: how to use cURL to export all grafana dashboards to JSON](https://gist.github.com/crisidev/bd52bdcc7f029be2f295#gistcomment-3975489)
    - a years-long and still active gist thread for exporting dashboards

- [nicolastakashi/gitana](https://github.com/nicolastakashi/gitana)
    - Gitana is a lightweight dashboard sync (K8s + sidecar solution)

### resources

- CUE and the future of dashboards as code

## reporting

- [IzakMarais/reporter](https://github.com/IzakMarais/reporter)
    - Service that generates a PDF report from a Grafana dashboard

- [divinity666/ruby-grafana-reporter](https://github.com/divinity666/ruby-grafana-reporter)
    - Reporting Service for Grafana

## alerting

- [orojina/grafana-cli](https://github.com/orojina/grafana-cli)
    - grafana-cli is a command line tool which allows you to execute actions against Grafana api server such as:

## plugin development

### resources

- [grafana/grafana-plugin-repository](https://github.com/grafana/grafana-plugin-repository)
    - A good starting point for publishing a community plugin. Includes steps for submitting a plugin via the new workflow inside your Grafana Cloud account

- ["6 tips for improiving your Grafana plugin before you publish"](https://grafana.com/blog/2021/01/21/6-tips-for-improving-your-grafana-plugin-before-you-publish/)
    - read this blog post _before_ submitting your plugin.

### tools

- [grafana/plugin-validator](https://github.com/grafana/plugin-validator)
    - A tool for validating community plugins for publishing to Grafana.com.

- [marcusolsson/grafana-plugin-support](https://github.com/marcusolsson/grafana-plugin-support)
    - This repository contains various helper functions to assist in plugin development

- [grafana/plugin-workflows](https://github.com/grafana/plugin-workflows)
    - Contains a set of GitHub Action workflows for building, testing, and releasing Grafana plugins.

## time and time-picker solutions

- [WilliamVenner/grafana-timepicker-buttons](https://github.com/WilliamVenner/grafana-timepicker-buttons)
    - Datasource-configured buttons panel plugin that set the time range of your Grafana dashboard
    
## data source specific

### SQL databases

- Grafana 8 breaking changes
    - did you just upgrade to Grafana 8+? Did it break some of your panels that use a SQL-style DB like MySQL or Postgres? This is a thing:
        - [read this note in the changelog](https://grafana.com/docs/grafana/latest/installation/upgrading/#postgres-mysql-microsoft-sql-server-data-sources)
        - [read this issue comment for details and workarounds](https://github.com/grafana/grafana/issues/35534#issuecomment-861519658)
        - try using [the `prepare-time-series` transformation](https://grafana.com/docs/grafana/latest/panels/transformations/types-options/#prepare-time-series)

### Prometheus

- [roaldnefs/awesome-prometheus](https://github.com/roaldnefs/awesome-prometheus)
    - A curated list of awesome Prometheus resources, projects and tools.