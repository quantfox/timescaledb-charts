# PostgreSQL with TimescaleDB Helm Chart

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/timescaledb)](https://artifacthub.io/packages/search?repo=timescaledb)

This Helm chart provides an easy way to deploy a PostgreSQL database with TimescaleDB, a popular PostgreSQL plugin for time-series data. The existing options for TimescaleDB Helm charts are either deprecated or incompatible with the latest requirements, so this chart addresses those limitations.

## About

- Unmaintained Official TimescaleDB Chart: The official TimescaleDB Helm chart is no longer actively maintained, making it challenging to deploy a reliable and up-to-date TimescaleDB database.
- Incompatibility with Bitnami PostgreSQL Chart: Bitnami’s PostgreSQL chart is a widely used and actively maintained option for PostgreSQL, but it lacks compatibility with the TimescaleDB extension, which requires specific PostgreSQL configurations and dependencies.

This chart bridges these gaps by providing a maintained, ready-to-use PostgreSQL with TimescaleDB integration.

## Features

- PostgreSQL Setup: Deploys a PostgreSQL database pre-configured to work with TimescaleDB.
- TimescaleDB Extension: Automatically sets up TimescaleDB to support efficient time-series data storage and querying.
- Helm Customization: Allows for customization of PostgreSQL parameters to better suit time-series workloads.

## Installation

### 1.	Add the Helm repository (if not already added):

```bash
helm repo add timescaledb https://quantfox.github.io/timescaledb-charts/
helm repo update
```


### 2.	Install the chart:

```bash
helm install my-timescaledb timescaledb/timescaledb
```

## Configuration

This chart provides configuration options for:

- Database parameters like the authentication method and password
- Resource requests and limits for PostgreSQL and TimescaleDB
- Persistence and storage class configuration
- Additional TimescaleDB-specific configurations

## License

This chart is licensed under the Apache 2.0 License. See the LICENSE file for more details.

For any issues or feature requests, please open a GitHub issue on this repository.