# Running Cafienne within Docker

This is a short "manual" to run a cafienne dev environment in docker.

### Required versions

To run the cafienne demo you need at least these versions:

* Docker Engine 1.12.0+
* Docker Compose 1.9.0+

### Running for the first time:

To run the environment (with docker-compose) use the following steps:

1. Open a terminal and change into the docker folder: `cd docker`
2. Run `docker-compose -f cafienne-demo.yml pull` to pull the latest docker images
3. Run the environment by running: `docker-compose -f cafienne-demo.yml up`

This will pull the required images from docker hub, create the required containers and start them.
It therefore may take a while ...

### Stopping and/or removing the environment

There are 2 methods to stop and/or remove the environment.

The first one stops a running environment and removes all created containers.
So everything is completely removed. Only use this method if you want to rebuild all
containers and start with a clean environment.

1. In a new terminal window, change to the docker folder and run: `docker-compose -f cafienne-demo.yml down`
2. Next clean all the elasticsearch data: `rm -rf elasticsearch/ cafienne/`

The second method only stops the running containers and all data is preserved. Use this method if you want
to preserve all your running cases.

1. In a new terminal window, change to the docker folder and run: `docker-compose -f cafienne-demo.yml stop`

### Running the environment normally

After creating/running the environment the first time, you can use the following
 command to start all the containers again.

1. Change into the docker folder and run: `docker-compose -f cafienne-demo.yml start`

## Exposed URLs

This composition exposes a set of URLs

- Cafienne UI: [http://localhost:8081](http://localhost:8081)
- Cafienne API: [http://localhost:18082](http://localhost:18082)
- ElasticSearch Head: [http://localhost:9200/_plugin/head](http://localhost:9200/_plugin/head)
