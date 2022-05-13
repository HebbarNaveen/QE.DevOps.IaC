# Introduction

Docker-compose files for spinning up the `OWASP ZAP` in different modes for security analysis.

## How-To

There are 2 docker-compose files each serving the purpose to launch `OWASP ZAP` tool in specific mode.
Each docker-compose file has a corresponding [.env](https://docs.docker.com/compose/env-file/) file containing the required parameters.
Follow the description/instructions in .env file before executing the docker-compose file.

1. `Proxy` folder contains the files to start-up the `OWASP ZAP` tool in headless proxying mode where it would proxy all the HTTP calls made by tests.

2. `Scan` folder contains the files to start-up the `OWASP ZAP` tool in headless scan mode depending on the choice made in parameters.

To execute the docker-compose file use `docker-compose up`

Add the `-d` flag at the end for detached execution

To stop the execution, hit Ctrl+C, and then `docker-compose down`
