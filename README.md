# OpenTelemetryDemo

## Overview

This project is designed to run using Docker Compose. Follow the steps below to build and run the project.

## Getting Started

### Prerequisites

- Docker/ Docker Desktop
- Docker Compose

### Building the Project

Before running the project, build it and then run docker-compose (Docker Compose) in default project run.


### Accessing Metrics

You can access the metrics at the following URL:
  ```
      http://localhost:18888/StructuredLogs
  ```
### Login to Aspire Dashboard

To login to the Aspire dashboard, you need to obtain the login token from the logs of the running container. Look for the following log entry:

```
dashboard | info: Aspire.Dashboard.DashboardWebApplication[0]
dashboard |       Login to the dashboard at http://0.0.0.0:18888/login?t=a74bc513a1b64e1d525dba23019e0b24
```

In the above log entry, the token is { a74bc513a1b64e1d525dba23019e0b24 }. Use this token to login to the dashboard at:
  ```
      http://localhost:18888/StructuredLogs
  ```
### API Usage

The postApi endpoint accepts an integer value corresponding to the following options:

    0 - Decaf
    1 - Espresso
    2 - DoubleEspresso
    3 - Cappuccino

Make sure to use one of these values when making requests to the postApi endpoint.
