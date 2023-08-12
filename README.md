DevOps Exercises
================

Working with Nexus repositories.

### Scenarios

- As a developer, I want to publish my npm package so that other users within my organization can use it.
- As an admin, I want to expose both, private and public repositories as a single registry for my users.
- As a developer, I want to include organization code into my projects.


## Setup

1. Create a local storage for nexus, `mkdir nexus-data`
2. Change the ownership of the _nexus-data_ folder `chown -R 200:200 nexus-data`

## Run the services

1. Use Compose to execute the service `docker-compose up`
2. Grab the password from `/nexus-data/admin.password `
3. Navigate to [local nexus dashboard](http://localhost:8081/)
4. Login as _admin_ (using the password you got from point `2`)


# Configure NPM Repositories

By following the [official guide](https://help.sonatype.com/repomanager2/node-packaged-modules-and-npm-registries) you should create the following structure:

1. A proxy NPM repository.
2. A private repository to host your private packages (see in the example folder the `npm-publish`).
3. A group repository to expose both, private and proxy repositories to your users.

