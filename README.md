# zeppelin-dockers
Dockerfile for each apache zeppelin release

**Zeppelin**, a web-based notebook that enables interactive data analytics. You can make beautiful data-driven, interactive and collaborative documents with SQL, Scala and more.

## Usage

To start Zeppelin pull the `latest` image of zeppelin-base:
```
docker pull mahmoudelgamal/zeppelin-base
```
And you can pull the zeppelin release image:
```
docker pull mahmoudelgamal/zeppelin-release:0.5.0
docker run --rm -it -p 8080:8080 -p 8081:8081 mahmoudelgamal/zeppelin-release:0.5.0 -c bash
```
Zeppelin located on `/usr/local/zeppelin/` path

Run zeppelin inside docker:
```
/usr/local/zeppelin/bin/zeppelin-daemon start
```

Zeppelin will be running at `http://${DOCKER_HOST}:8080`.
