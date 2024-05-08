# Running locally with testcontainers
Use the **ComposerLocal** run configuration. Data will be lost after a restart.

# Run each service in a docker container
Data is persisted after a restart.

To clear existing data.
````
rmdir .\DbData
````
## maven build
````
mvn clean install -DskipTests
````
## Build the docker containers
### Start all containers
````
docker-compose up -d
````

### Stop all containers
````
docker-compose down
````

### Monitor logs
````
docker-compose logs -f
````