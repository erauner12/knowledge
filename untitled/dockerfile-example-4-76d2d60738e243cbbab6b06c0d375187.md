# Dockerfile example 4 76d2d60738e243cbbab6b06c0d375187

```bash
cd demo-8
total 16
-rw-r--r--@ 1 er046256  1745752250  234 Dec 11  2018 child-Dockerfile
-rw-r--r--@ 1 er046256  1745752250  302 Dec 11  2018 parent-Dockerfile
```

```bash
------------------------------------ parent-dockerfile ---------------------------------------

FROM ubuntu:16.04

ONBUILD RUN echo "Greetings from your parent image!" > /tmp/hello.txt

CMD ["bash"]

----------------------------------- End of parent-dockrefile ---------------------------------
```

```bash
------------------------------------ child-dockerfile ---------------------------------------

FROM papa-ubuntu:latest

CMD ["bash"]

----------------------------------- End of child-dockrefile ---------------------------------
```

* papa-ubuntu is name the name of the image we will soon build

```bash
docker build -f parent-Dockerfile -t papa-ubuntu .
```

```bash
docker build -f child-Dockerfile -t baby-ubuntu .
```

```bash
docker run -itd --name baby-container baby-ubuntu
```

```bash
docker exec -it baby-container bash
```

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Docker/S2/cmc/demo-8  docker exec -it baby-container bash
root@b2921e63e3d2:/# cd tmp/
root@b2921e63e3d2:/tmp# ll
total 12
drwxrwxrwt 1 root root 4096 Jan  9 20:33 ./
drwxr-xr-x 1 root root 4096 Jan  9 20:33 ../
-rw-r--r-- 1 root root   34 Jan  9 20:33 hello.txt
root@b2921e63e3d2:/tmp# cat hello.txt
Greetings from your parent image!
```

