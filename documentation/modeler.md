# Running the Cafienne CMMN modeler

The Cafienne CMMN modeler is also available as a docker image and can be used to
create and deploy/export case models which can be run by the Cafienne engine.

> NOTE: This requires you to have a Docker Hub account and have access to the SpronQ docker
repositories. Contact SpronQ to get access.

To get the image from the repository, issue the following commands in a terminal:

1. `docker login`
2. `docker pull spronq/test:cmmn-modeler`

Next, to run the image use the following command:

`docker run --rm --name modeler -p3001:3001 -v <cafienne-demo>/workspace/definitions:/usr/src/app/repository -v <cafienne-demo>/deployments/definitions:/usr/src/app/repository_deploy spronq/test:cmmn-modeler`

> NOTE: Replace `<cafienne-demo>` with the path where you checked out this repository

> NOTE: you can access the modeler by going to [http://localhost:3001](http://localhost:3001)

When you deploy a model from the modeler and the Cafienne Demo environment is running, this model is directly available in de Cafienne Demo environment.
