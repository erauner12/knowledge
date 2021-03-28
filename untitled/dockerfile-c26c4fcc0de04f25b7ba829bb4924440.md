# Dockerfile c26c4fcc0de04f25b7ba829bb4924440

* a sequential set of instruction for Docker Engine
* primary way of interacting with Docker
* Each instruction creates a layer on the image that will be built

Layers can be cached and reused by Docker

```bash
FROM
ARG

RUN
ADD | COPY
ENV

CMD
ENTRYPOINT
EXPOSE
```

```bash
FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN mkdir /home/Codes

ENV USER Cerulean-Canvas
ENV SHELL /bin/bash
ENV LOGNAME Cerulean-Canvas

CMD ["bash"]
```

```bash
docker build -t img_run-env .
```

* -t `tag`

```bash
docker run -itd --name cont_run-env img_run-env
```

```bash
docker ps -a
```

```bash
docker exec -it cont_run-env bash
```

