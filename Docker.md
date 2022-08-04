**Docker** is a software suite that uses [OS-level
virtualization](wikipedia:OS-level_virtualization "wikilink") to deliver
software in packages called containers. Containers are isolated from one
another and bundle their own software, libraries and configuration
files; they can communicate with each other through well-defined
channels. Because all of the containers share the services of a single
operating system kernel, they use fewer resources than [virtual
machines](wikipedia:Virtual_machine "wikilink").

## Dockerfile

### Example alpine linux MySQL Dockerfile {#example_alpine_linux_mysql_dockerfile}

``` {.dockerfile .numberLines}
FROM alpine:3.14
RUN apk add --no-cache mysql-client
ENTRYPOINT ["mysql"]
```

  INSTRUCTION   Example                                                 
  ------------- ------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------
  FROM          FROM alpine:3.14                                        FROM instruction gets an image from dockerhub to use as a base.
  RUN           RUN \[\"executable\", \"param1\", \"param2\"\]          RUN instruction runs an executable with parameters during the building of the image.
  ENTRYPOINT    ENTRYPOINT \[\"executable\", \"param1\", \"param2\"\]   ENTRYPOINT instruction runs a shell command or executable when the container starts. There can only be one ENTRYPOINT or CMD in a Dockerfile.
  CMD           CMD \[\"executable\",\"param1\",\"param2\"\]            It\'s like ENTRYPOINT but can be configured from CLI.
  COPY          COPY `<src>`{=html} `<dest>`{=html}                     COPY instruction copies new files or directories from `<src>`{=html} and adds them to the filesystem of the container at the path `<dest>`{=html}
  ADD           ADD `<src>`{=html} `<dest>`{=html}                      Similar to COPY but has additional features like adding files from external sites or extracting compressed files.
  LABEL         LABEL version=\"1.0\"                                   LABEL instruction adds metadata to an image.
  EXPOSE        EXPOSE 8080                                             EXPOSE instruction informs Docker that the container listens on the specified ports while running.
  VOLUME        VOLUME \[\"/app\"\]                                     VOLUME instruction informs Docker that a volume will be mounted at specified path.

  : Dockerfile instructions refrence sheet

### How to build an image from a Dockerfile {#how_to_build_an_image_from_a_dockerfile}

Note that the last argument is expecting a folder that contains your
Dockerfile and NOT the file itself.

    docker build --tag myimage:latest .

## Docker run {#docker_run}

### Basic docker run command {#basic_docker_run_command}

    docker run myimage:latest

### \--publish

Commonly you need to access ports from container on your host machine,
this [Command-Line flag](Command-Line_flag "wikilink") helps you change
and access them.

#### Example command that expose port 8080 to port 80 on the host. {#example_command_that_expose_port_8080_to_port_80_on_the_host.}

    docker run --publish 80:8080 myimage:latest

## Docker compose {#docker_compose}

### Example docker-compose.yml {#example_docker_compose.yml}

``` {.yaml .numberLines}
version: "3.7"

services:
  mycontainer:
    container_name: mycontainer
    image: myimage
    environment:
      - PUID=1000
      - PGID=1000
      - UMASK=002
      - TZ=Europe/Tallinn
    ports:
        - 80:8080
    restart: unless-stopped
```

### How to start a docker compose config? {#how_to_start_a_docker_compose_config}

    docker compose up --file docker-compose.yml
