---
layout: layout.pug
navigationTitle: Release Notes
title: Release Notes
menuWeight: 40
excerpt: New features, updates, and known limitations
render: mustache
model: ../data.yml
---

# Version v1.0.0

## New features

* Add Marathon LB integration.
* Enable gzip compression for Grafana's HTTP server.
* Add a link to the Grafana UI on the Services page.
* Set the Home dashboard in Grafana to the DC/OS Overview dashboard.
* Add a configuration option for the Grafana dashboard theme style (defaults to Light).
* Default DC/OS Grafana dashboards are loaded to a folder called DC/OS Defaults.

## Updates

* Grafana dashboard titles are no longer overwritten by the file path of the dashboard json.
* Push Gateway is no longer supported.
* Decrease the number of resources in the default package configuration.
* Read in DC/OS CA certs for verification in the Prometheus agent discovery task (Enterprise only).
* Update Prometheus to v2.9.2.
* Update Alertmanager to v0.16.2.
* Update Grafana to v6.1.4.
* Update SDK to v0.56.0.

## Known limitations

* Upgrading from v0.4.3 is not possible due to the removal of Push Gateway.
* Service name cannot contain characters that are not allowed in a DNS name (e.g., /) if using Marathon LB integration.

# Version v0.4.3

## Updates

* Fix issues that occur when the service is installed in a folder.
* Fix a regression related to deploy key support.

# Version v0.4.2

## Updates

* Workaround the UI bug for package install.

# Version v0.4.1

## Updates

* Bug fixes (DSS profile support is missing).

# Version v0.4.0

## New features

* Allow accessing Alertmanager UI through Admin Router.
* Allow accessing Prometheus UI through Admin Router.
* Support loading Prometheus alert rules from a Git repository.
* Support reloading Alertmanager configurations after install.
* Support DC/OS Storage Service (DSS) volume profiles.

## Updates

* Support for configuring Prometheus storage retention.
* Support for configuring Alertmanager resource footprint (i.e., CPU and memory).
* Installable from the Universe.
* Update SDK to 0.55.2.
* New logo.

## Known limitations

* Upgrading from v0.3.0 is not supported at this time.
* Does not support loading Prometheus alert rules recursively from a directory.

# Version v0.3.0

## New features

* Allow accessing Grafana UI through Admin Router.
* Support configuring Grafana admin user credentials.
* Support Open DC/OS.
* Support [Package Registry](https://docs.mesosphere.com/latest/administering-clusters/repo/package-registry/).

## Updates

* Remove support for Prometheus Mesos Exporter, which is no longer used to collect Mesos metrics.

# Version v0.2.1

## Updates

* Correct permissions required to run the package.

# Version v0.2.0

## New features

* Support `SSH auth` when fetching from Git repository.
* Add default Grafana dashboards which can be automatically loaded.
* Support Grafana server placement constraints.
* Support fetching from a branch in a Git repository.

## Updates

* Grafana v5.3.4.
* Use local persistent volume for Grafana server.
* Use Docker image for Grafana server.
* Recursively clone Git sub-modules from a Git repository.

# Version v0.1.1

Bug fix release.

## Updates

* Add missing release notes.

# Version v0.1.0

Initial release.

## New features

* Prometheus v2.2.1.
* Grafana v5.0.1.
* Alertmanager v0.15.2.
* Push Gateway v0.5.2.
* Automatically scrape dcos-metrics service endpoints in Prometheus.
* Automatically load Grafana dashboard configurations from a Git repository.
* Automatically load Alertmanager configurations from a Git repository.
* Support strict mode DC/OS cluster.
* Support launching Grafana server on public agents.

## Known limitations

* No persistent storage for Grafana dashboard configurations.
* No external storage for Prometheus data.
* No backup for Prometheus data.
