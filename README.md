# Cafienne Demo environment

This repository allows you to setup a Cafienne demo environment based on docker images
of Cafienne, Cafienne-UI and the underlying ElasticSearch storage engine.

Please read the following documents:

-
- [Running the Cafienne CMMN modeler](documentation/modeler.md)

## Prerequisites

To be able to run this environment, you need to have access to some repositories on Github
and Docker Hub. Please contact SpronQ to arrange the proper access. But before contacting SpronQ,
you need to create a [Github](https://github.com) and [Docker Hub](https://hub.docker.com) account for yourself.

Next clone this repository from Github by running the following command in a terminal:

`git clone https://github.com/SpronQ/cafienne-demo.git`

## Running the environment

See [Running a Cafienne Demo environment with docker](documentation/docker.md)

## Deploying CMMN models to the demo environment

First you need to setup and configure the Cafienne CMMN modeler to create new models and deploy them to
this environment. See [Running the Cafienne CMMN modeler](documentation/modeler.md) on how to set this up
properly.

### Deploy existing models to the demo enviroment

When you already have existing models build by the Cafienne CMMN modeler, you can simply deploy them to this
environment by copying the build CMMN model XML file to the `deployments/definitions` folder in this repository.
The Cafienne Demo environment picks up any valid model that is stored in this folder.

## Exposed URLs of the Cafienne Demo environment

After starting up de Cafienne Demo environment, the following URL allow you to access the various parts of the
environment:

- Cafienne UI: [http://localhost:8081](http://localhost:8081)
- Cafienne API: [http://localhost:18082](http://localhost:18082)
- ElasticSearch Head: [http://localhost:9200/_plugin/head](http://localhost:9200/_plugin/head)

You can logon to the Cafienne UI by using `admin` for the username and password
