# Docker Architecture b2e964bf084c4e49a06855f3842ef97b

Docker Engine

* Docker Client
  * Docker CLI

    ```bash
    docker pull
    docker run
    ```

  * Docker API
  * Docker client sends API calls to docker host and displays results
* Docker Host
  * Docker host actually runs the apps
  * Docker Daeomon runs the apps by turning into docker images
    * docker images can be run as containers
  * Docker host talks to docker registry to pull/push images
* Docker Registry
  * Serves as a place to server docker images

