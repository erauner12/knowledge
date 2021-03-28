# Healthcheck 87586ef718ec4832930febf3d7a2c3f7

```bash
~/tmp/Container-Masterclass-Codes/CC_Docker/S2/cmc/demo-9
```

```bash
from flask import Flask

app = Flask(__name__)

@app.route('/')

def CMC():
    return 'Welcome to the Container Master Class by Cerulean Canvas'

if __name__ == '__main__':
    app.run(host='0.0.0.0')
```

* flask is an webserver gateway interface network \(PYTHON\)

```bash
Flask==0.12.2
```

```bash
FROM ubuntu:16.04

RUN apt-get update -y && \
    apt-get install -y python-pip python-dev curl

COPY . /app

WORKDIR /app

RUN pip install -r requirements.txt

HEALTHCHECK --interval=10s --timeout=30s CMD curl --fail http://localhost:5000/ || exit 1

CMD ["python", "app.py"]

STOPSIGNAL SIGKILL
```

`HEALTHCHECK` interval, timeout, and command

if the command encounters failure then exit

* `STOPSIGNAL` gives you the choice on how to handle

```bash
docker build -t flask_app .
```

```bash
docker run --rm -itd --name flask -p 5000:5000 flask_app
```

```bash
curl http://localhost:5000/
```

[http://localhost:5000/](http://localhost:5000/)

```bash
docker container stop flask
```

