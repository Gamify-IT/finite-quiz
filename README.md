# finitequiz

A simple single-choice question game.

## Development

### Getting started

Clone the repository  
```sh
git clone https://github.com/Gamify-IT/finitequiz.git
```

Install the dependencies  
```sh
npm install
```

#### Run with Docker-compose

Start all dependencies with our docker-compose files.
Check the [manual for docker-compose](https://github.com/Gamify-IT/docs/blob/main/dev-manuals/languages/docker/docker-compose.md).

### Compile and Hot-Reload for Development

```sh
npm run serve
```

### Test

Run the tests:
```sh
npm run test:unit
```

To also get the test coverage:
```sh
npm run test:unit -- --coverage
```

### Build

Build the Docker-Container
```sh
docker build -t finitequiz-dev .
```
And run it at port 8000 with
```sh
docker run -d -p 8000:80 --name finitequiz-dev finitequiz-dev
```

To monitor, stop and remove the container you can use the following commands:
```sh
docker ps -a -f name=finitequiz-dev
```
```sh
docker stop finitequiz-dev
```
```sh
docker rm finitequiz-dev
```

## User manual

Run the docker container with the following command at port 8000:
```sh
docker run -d -p 8000:80 --name finitequiz ghcr.io/gamify-it/finitequiz:latest
```
Now you can access it at [http://localhost:8000](http://localhost:8000).  
To access it externally replace localhost with your IP.  

To monitor the container you can use the following command:
```sh
docker ps -a -f name=finitequiz
```
To stop the container you can use the following command:
```sh
docker stop finitequiz
```
To remove the container you can use the following command:
```sh
docker rm finitequiz
```
