# Docker Py + SQL

![Docker Image CI](https://github.com/tiagogoliveira/docker/actions/workflows/docker-image.yml/badge.svg)

An image with pyodbc for Microsoft SQL Server.

```sh
docker pull tiagogoliveira/docker:latest
```

### Testing

Small application for testing the image configuration:

```sh
cd ./test
cp config.dev.ini config.ini

docker-compose build
docker-compose up
```

### Docker Hub

Commands for manually publishing the image to Docker Hub:

```sh
export dockerHubImage='tiagogoliveira/docker:latest'

docker image build -t docker:latest ./image
docker login --username='<username>'
docker tag '<image_id>' $dockerHubImage
docker push $dockerHubImage
```