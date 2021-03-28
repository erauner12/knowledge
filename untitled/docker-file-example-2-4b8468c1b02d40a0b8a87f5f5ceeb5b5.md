# Docker file example 2 4b8468c1b02d40a0b8a87f5f5ceeb5b5

```bash
FROM ubuntu:trusty

LABEL Creator: "Cerulean Canvas" \
      Version: "1.0"

RUN apt-get update -y

ENTRYPOINT ["/bin/ping","-c","5"]

CMD ["localhost"]
```

* entrypoint will bring container back to a starting point upon restart
* CMD is the argument for `ENTRYPOINT`

```bash
docker build -t img_entry-cmd .
```

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Docker/S2/D-5  docker images
REPOSITORY                                                               TAG                  IMAGE ID       CREATED          SIZE
img_entry-cmd                                                            latest               ad02bbd1fb44   49 seconds ago   210MB
img_run-env                                                              latest               404c67dc1614   9 minutes ago    147MB
img_from                                                                 latest               360ae1486b91   13 minutes ago   161MB
docker.cernerrepos.net/alva/alva-config                                  latest               4c8f9dc1d3f0   26 hours ago     474MB
cerngoussmash100.cernerasp.com:5000/aw062641_support_automation_search   latest               a294948f87b9   3 weeks ago      263MB
python                                                                   3.9-alpine           d4d4f50f871a   3 weeks ago      44.2MB
nginx                                                                    latest               ae2feff98a0c   3 weeks ago      133MB
flowalex/linux_package_installer                                         dev-20201206091745   2cb969f53495   4 weeks ago      486MB
ubuntu                                                                   16.04                9499db781771   6 weeks ago      131MB
mysql/mysql-server                                                       latest               c8552d79a138   2 months ago     405MB
ubuntu                                                                   trusty               df043b4f0cf1   3 months ago     197MB
nvuillam/npm-groovy-lint                                                 latest               7c492ff18101   4 months ago     340MB
```

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Docker/S2/D-5  docker run --name cont_entry-cmd img_entry-cmd
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.034 ms
64 bytes from localhost (127.0.0.1): icmp_seq=2 ttl=64 time=0.066 ms
64 bytes from localhost (127.0.0.1): icmp_seq=3 ttl=64 time=0.049 ms
64 bytes from localhost (127.0.0.1): icmp_seq=4 ttl=64 time=0.192 ms
64 bytes from localhost (127.0.0.1): icmp_seq=5 ttl=64 time=0.112 ms

--- localhost ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4102ms
rtt min/avg/max/mdev = 0.034/0.090/0.192/0.058 ms
```

```bash
er046256@w1738944  ~/tmp/Container-Masterclass-Codes/CC_Docker/S2/D-5  docker ps -a
CONTAINER ID   IMAGE           COMMAND                  CREATED              STATUS                          PORTS     NAMES
7b5df9fd81bd   img_entry-cmd   "/bin/ping -c 5 loca…"   About a minute ago   Exited (0) About a minute ago             cont_entry-cmd
590f5fa7efc7   img_run-env     "bash"                   11 minutes ago       Up 11 minutes                             cont_run-env
```

