# ReelGoofy: CI/CD & Telemetry

ReelGoofy is a movie recommendation service.

## Assignment

ReelGoofy's API was implemented in the third homework. We followed up on it in the fourth assignment, where we containerized it and made it persist its data. We will finish this application by setting up a simple CI/CD pipeline and instrumenting it with metrics.

### Specification

#### CI/CD

The CI/CD pipeline will be created using GitHub Actions. The requirements are simple:

- Regarding integration, the pipeline must lint, format, build, and test the code.
- Regarding delivery, the pipeline will build the container image and push it to a public registry of your choice.
  - E.g. GitHub Container Registry, Docker Hub, etc.

Do not forget to use the predefined GitHub actions as they will simplify the work for you. The ones you might consider using:

- [setup-go](https://github.com/actions/setup-go)
- [golangci-lint-action](https://github.com/golangci/golangci-lint-action)
- [build-push-action](https://github.com/docker/build-push-action)

#### Metrics

Extend your compose file with [Prometheus](https://hub.docker.com/r/prom/prometheus) and [Grafana](https://hub.docker.com/r/grafana/grafana). We will use Prometheus as our metrics backend and Grafana for visualizing the metrics.

Create configurations for both Prometheus and Grafana (the `scrape_configs` and `datasources` are what interests us, respectively).

Instrument the ReelGoofy application with custom metrics. The application must expose metrics for the number of HTTP requests on specific endpoints, their response times, and response codes. For additional metrics, the choice is up to you.

Lastly, create a dashboard for the ReelGoofy service and create at least six visualizations (graphs). Do not forget to persist the newly created graphs, either by exporting them or by mounting a volume with the Grafana configuration files to the repository. Either way, they should be stored in a `data` directory.

## Requirements

The application has a functioning CI/CD pipeline that lints, formats, builds, tests, and containerizes it. The application is also properly instrumented and monitoring is set up using Grafana and the created dashboard.

## Motivation

The main goal is to finish the ReelGoofy application by instrumenting it with telemetry and by creating a functioning pipeline. Having both of these implemented is a necessity for real-life applications.
