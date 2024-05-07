# maven build
````
mvn clean install
````
# Running in Docker Containers
## Individual containers
### First build the image
(Starting from the root/parent project.)
#### Facade
````
cd composer-v1-facade

docker build -t lreynolds/composer-v1-facade:latest .
````
#### Composition
````
cd composer-v1-composition-service

docker build -t lreynolds/composer-v1-composition:latest .
````
#### Generator
````
cd composer-v1-generator-service

docker build -t lreynolds/composer-v1-generator:latest .
````

### Run the container from the image
````
docker run lreynolds/composer-v1-facade:latest
docker run lreynolds/composer-v1-composition:latest
docker run lreynolds/composer-v1-generator:latest
````

## All Containers
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