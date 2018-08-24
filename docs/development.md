# Development

## Folder structure
### Code folder structure
* **api**: definition of the RedisFailover CRD.
* **client**: autogenerated client to interact with redis-failovers.
* **cmd**: contains the starting point of the application.
* **log**: wrapper of logrus, created to be able to mock it.
* **metrics**: exposer of status of the failovers created.
* **mocks**: contains the mocked interfaces for testing the application.
* **operator**: the main logic. Manages the requests from k8s and creates/updates/deletes the pieces as needed.
* **service**: services/clients to interact with k8s and redises.
* **vendor**: vendored packages used by the application.

### Non-code folder structure
* **charts**: helm chart to deploy the operator.
* **docker**: Dockerfiles to generate redis-failover docker images.
* **example**: yaml files with spec of redis-failover.
* **hack**: scripts to generate the redis-failover api-client.
* **scripts**: scripts used to build and run the app.

## Make development commands
You can do the following commands with make:
* Build the development container.
`make docker-build`
* Generate mocks.
`make go-generate`
* Generate client
`make update-codegen`
* Run tests.
`make test`
* Build the executable file.
`make build`
* Run the app.
`make run`
* Access the docker instance with a shell.
`make shell`
* Install dependencies
`make get-deps`
* Update dependencies
`make update-deps`
* Build the app image.
`make image`