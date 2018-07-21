# Cafienne Demo environment

This repository allows you to setup a Cafienne demo environment based on docker images
of Cafienne, Cafienne-UI and the underlying ElasticSearch storage engine.

## Prerequisites

To be able to run this environment, you need to have access to the cafienne-demo repository in Github. Please contact SpronQ to arrange the proper access.
Before contacting SpronQ you need to create a [Github](https://github.com) account for yourself.

Next clone this repository from Github by running the following command in a terminal:

`git clone https://github.com/cafienne/cafienne-demo.git`

## Running the environment

See [Running a Cafienne Demo environment with docker](documentation/docker.md)

## Exposed URLs of the Cafienne Demo environment

After starting up de Cafienne Demo environment, the following URL allow you to access the various parts of the
environment:

- Cafienne task user interface: http://localhost:8081
- Cafienne modeler environment: http://localhost:3001
- Cafienne API (exposed through Swagger): http://localhost:18082
- MailCatcher web UI: http://localhost:1080

You can logon to the Cafienne UI by using `admin` for the username and `cafienne` for the password

## Building and deploying a CMMN model

### Creating a model
The Cafienne modeler can be accessed via http://localhost:3001.
In this environment, you can create new CMMN models and deploy them to the engine.

### Deploy existing models to the demo enviroment

When you already have existing models built by the Cafienne CMMN modeler, you can simply deploy them to this
environment by copying the build CMMN model XML file to the `deployments/definitions` folder in this repository.
The Cafienne Demo environment picks up any valid model that is stored in this folder.

## Help

If you need help or encounter issues, you can search the [existing repository issues](https://github.com/cafienne/cafienne-demo/issues) or directly [create a new issue](https://github.com/cafienne/cafienne-demo/issues/new).
