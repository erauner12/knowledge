# Docker file example 3 429dd375fe00480281d0a01f3df2dcb3

```bash
FROM ubuntu:16.04

RUN apt-get update && apt-get install nginx -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

* `expose` what port the container is listening

```bash
docker build -t img_expose .
```

```bash
docker run -itd --rm --name cont_expose -p 8080:80 img_expose
```

navigate to;

