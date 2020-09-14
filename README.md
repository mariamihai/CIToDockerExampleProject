[![CircleCI](https://circleci.com/gh/mariamihai/CIToDockerExampleProject.svg?style=svg)](https://circleci.com/gh/mariamihai/CIToDockerExampleProject)
[![Docker](https://img.shields.io/docker/v/mariamihai/sbm-beer-service?sort=date)](https://hub.docker.com/r/mariamihai/sbm-beer-service)

# Simple CI to Docker Image project
This is a simple application I used to learn the processes used by CircleCI and to help me build and push a simple Docker image.

## Using the application
Pull the image from the Docker Hub:
```
docker pull mariamihai/ci-to-docker-example-project
```

Run a container:
```
docker run -d -p 8080:8080 mariamihai/ci-to-docker-example-project
```

Go to [http://localhost:8080/hello](http://localhost:8080/hello). You will receive an "Hello" from the application.

## Status
**[COMPLETED]** - I am setting a personal status of "Completed" and will probably not update this repository in the near future as this was a learning project.