# Introduction

Docker-compose file for running the Blazemeter Taurus tool

## Running the container

To execute this docker-compose file use `docker-compose up`
Container will stop when tests are finished.

Example config.yml file for running *jmeter, nunit and selenium* tests in Taurus can be found in /examples/ folder.
Before running anything, you should put name of your YAML file in the .env file (placed alongside docker-compose.yml) as *TAURUS_CONFIG* in order for it to be saved as an environment variable and run by Taurus

## Volumes

* /bzt-configs - default working dir of blazemeter. You should put your yaml file and test sources in this folder.
* /tmp/artifacts - folder where test run artifacts will be saved.

## Running your tests

Place your scripts and config in /bzt-configs mounted folder
Replace 'scenarios' elements in example config.yml file with your own (with paths to mounted script files) and add them in *execution* section as a scenario.
Your test results will be in /tmp/artifacts mounted dir after the execution
