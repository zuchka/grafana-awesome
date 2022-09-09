# grafana-awesome

> an awesome-style list of tools and resources for Grafana

note: this is a work in progress--PRs are encouraged!

## CONTENTS

- [quickstarting Grafana](#quickstarting-grafana)
    - [examples](#examples)
    - [templates](#templates)
    - [cheat sheets](#cheat-sheets)
    - [videos](#videos)
- [admin tasks](#admin-tasks)
    - [backing up Grafana settings](#backing-up-grafana)
    - [searching Grafana](#searching-grafana)
    - [migrating the grafana.db database](#migrating-the-grafanadb-database)
    - [exporting and syncing dashboards (as-code)](#dashboard-exporting--syncing)
    - [reporting](#reporting)
    - [auth](#auth)
- [alerting](#alerting)
    - [unified alerting](#unified-alerting)
    - [legacy alerting](#legacy-alerting)
- [plugin development](#plugin-development)
    - building
    - signing
    - publishing
- [datasources](#data-sources)
    - [SQL data sources (MySQL, MSSQL, Postgres, etc)](#sql-driven-data-sources)
    - [Prometheus data source](#prometheus-data-source)
    - Loki
    - InfluxDB
    - ElasticSearch
    - Cloudwatch
    - Azure Monitor
    - Zabbix
- [visualizations](#visualizations)
    - [table panel](#table-panel)
        - [how to fix the gauges inside the table panel](https://github.com/grafana/grafana/issues/40926#issuecomment-957202015)
- [networking](#networking)
    - [reverse proxies](#reverse-proxies)
- [other](#other-resources)

## <u>quickstarting Grafana</u>

> resources to sandbox, bootstrap, and quickstart Grafana


### examples   

- #### [play.grafana.org](TK)
    - grafana's public sandbox. a great place to try out features or mock up a problem.

- #### [grafana/tutorial-environment](https://github.com/grafana/tutorial-environment)
    - a batteries-inluded sample web application + grafana + loki + prometheus. Deploy everything with a single `docker-compose up`. And don't forget to try [the companion "Fundamentals" tutorial](https://grafana.com/tutorials/grafana-fundamentals/).


### templates

- #### [title](TK)
    - description

- #### [title](TK)
    - description

### cheat sheets

- #### [Grafana Cheatsheet, by Ruan Bekker](https://github.com/ruanbekker/cheatsheets/tree/master/grafana)
    - description

### videos

- #### [How to add a Prometheus data source in Grafana 8.3](https://www.youtube.com/watch?v=PwGtkD0xRzk)
    - a one-minute quickstart video

- #### [How to build a Prometheus query in Grafana 8.3](https://www.youtube.com/watch?v=5VrjOzIOJPw)
    - a one-minute quickstart video

## <u>admin tasks</u>

> resources for common admin tasks like migrating the Grafana db, syncing dashboards, and generating reports

### backing up Grafana

- #### [ysde/grafana-backup-tool](https://github.com/ysde/grafana-backup-tool)
    
    - A Python-based application to back up Grafana settings using the Grafana API

### searching Grafana

- #### [panodata/grafana-wtf](https://github.com/panodata/grafana-wtf)

    - Grep through all Grafana entities in the spirit of `git-wtf`.

- #### [Grafana extension for Raycast](https://github.com/raycast/extensions/tree/main/extensions/grafana)

    - Search your dashboard inside [Raycast](https://www.raycast.com/).

### migrating the grafana.db database

- #### [grafana/database-migrator](https://github.com/grafana/database-migrator)
    - This script dumps data from a grafana sqlite database in a format that works with MySQL. It is intended to assist in migrating Grafana instances from the default sqlite database (grafana.db) to MySQL (or a MySQL-compatible DB like MariaDB).

### dashboard exporting & syncing

- #### [how to use cURL to export all grafana dashboards to JSON](https://gist.github.com/crisidev/bd52bdcc7f029be2f295#gistcomment-3975489)
    - a years-long and still active gist thread for exporting dashboards

- #### [nicolastakashi/gitana](https://github.com/nicolastakashi/gitana)
    - Gitana is a lightweight dashboard sync (K8s + sidecar solution)

- #### [netsage-project/gdg](https://github.com/netsage-project/gdg)
    - Grafana Dash-n-Grab (GDG) -- a CLI to backup and restore dashboards and datasources.

### reporting

- #### [IzakMarais/reporter](https://github.com/IzakMarais/reporter)  
    - Service that generates a PDF report from a Grafana dashboard

- #### [divinity666/ruby-grafana-reporter](https://github.com/divinity666/ruby-grafana-reporter)   
    - Reporting Service for Grafana

<<<<<<< HEAD
### auth

- [How to configure Auth0 and Grafana](https://cyral.com/blog/how-to-grafana-auth0/), by Kaizen Towfiq 

## ALERTING
=======
- #### [panodata/grafanimate](https://github.com/panodata/grafanimate)  
    - Tool for creating animations of your time-series by capturing screenshots while stepping through time.
>>>>>>> f8cf9ea9878e779c789a0a29346f3eeb94dd32a3

## <u>alerting</u>
> resources for legacy alerting and the new unified alerting (Grafana 8+)

### unified alerting

- #### [title](TK)
    - description

- #### [title](TK)
    - description

- [orojina/grafana-cli](https://github.com/orojina/grafana-cli)
    - a command line tool that allows you to execute actions against Grafana api server (e.g. start/stop alerts)

### legacy alerting

## <u>plugin development</u>
> resources for building, signing, and publishing Grafana Plugins

### building

- #### [marcusolsson/grafana-plugin-support](https://github.com/marcusolsson/grafana-plugin-support)
    - This repository contains various helper functions to assist in plugin development

- #### [title](TK)
    - description

### signing

- #### [title](TK)
    - description

### publishing

- #### ["6 tips for improving your Grafana plugin before you publish"](https://grafana.com/blog/2021/01/21/6-tips-for-improving-your-grafana-plugin-before-you-publish/)
    - read this blog post _before_ submitting your plugin.

- #### [grafana/plugin-validator](https://github.com/grafana/plugin-validator)
    - A tool for validating community plugins for publishing to Grafana.com.

- #### [grafana/plugin-workflows](https://github.com/grafana/plugin-workflows)
    - Contains a set of GitHub Action workflows for building, testing, and releasing Grafana plugins.

- #### [grafana/grafana-plugin-repository](https://github.com/grafana/grafana-plugin-repository)
    - A good starting point for publishing a community plugin. Includes steps for submitting a plugin via the new workflow inside your Grafana Cloud account

## <u>data sources</u>

> data source plugins, exporters, REST APIs, and other get-my-data-into-Grafana solutions

### SQL-driven data source plugins

- #### [grafana/sqlds](https://github.com/grafana/sqlds)
    - Most SQL-driven datasources, like `Postgres`, `MySQL`, and `MSSQL` share extremely similar codebases. The `sqlds` package is intended to remove the repetition of these datasources and centralize the datasource logic.

- #### [just upgraded to Grafana 8+?](https://grafana.com/docs/grafana/latest/installation/upgrading/#postgres-mysql-microsoft-sql-server-data-sources) 
    - Did it break some panels that use a SQL-driven DB like MySQL or Postgres? This is a known breaking change:

    - [read this note in the changelog](https://grafana.com/docs/grafana/latest/installation/upgrading/#postgres-mysql-microsoft-sql-server-data-sources)
    - [read this issue comment for details and workarounds](https://github.com/grafana/grafana/issues/35534#issuecomment-861519658)
    - try using [the `prepare-time-series` transformation](https://grafana.com/docs/grafana/latest/panels/transformations/types-options/#prepare-time-series)

### Prometheus data source plugin

- #### [roaldnefs/awesome-prometheus](https://github.com/roaldnefs/awesome-prometheus)

    - A curated list of awesome Prometheus resources, projects and tools.

- #### [grafana/dashboard-linter](https://github.com/grafana/dashboard-linter)

    - Lint your dashboards for common mistakes (Prometheus data source only)

### Python, Pandas, & Data Analysis

- #### [panodata/grafana-pandas-datasource](https://github.com/panodata/grafana-pandas-datasource)

    - connect Python's greatest data analysis library to Grafana. `grafana-pandas-datasource` is a REST API based on Flask for serving Pandas Dataframes to Grafana. This way, a native Python application can supply data to Grafana both easily and powerfully. 

    - [Originally based on this gist by @linar-jether](https://gist.github.com/linar-jether/95ff412f9d19fdf5e51293eb0c09b850)

## <u>visualizations</u>

### table panel

- #### [[how to fix the gauges inside the table panel](https://github.com/grafana/grafana/issues/40926#issuecomment-957202015)]

### timeseries panel

## <u>networking</u>

### reverse proxies

- #### [Reverse Proxy change in 8.3.5](https://github.com/grafana/grafana/issues/45117#issuecomment-1033842787)
    - the new header setting for reverse proxies for 8.3.5+. Did upgrading to 8.3.5+ break your grafana? Is your grafana behind a reverse proxy? Check out this issue.

## <u>other resources</u>

### IoT, home lab, & maker solutions

- #### [grafana/prometheus-arduino](https://github.com/grafana/prometheus-arduino)
    - An Arduino library for sending prometheus metrics directly to a Prometheus remote write endpoint.

### time and time-picker solutions

- #### [WilliamVenner/grafana-timepicker-buttons](https://github.com/WilliamVenner/grafana-timepicker-buttons)

    - Datasource-configured buttons panel plugin that set the time range of your Grafana dashboard
