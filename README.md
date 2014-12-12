# DevDB RethinkDB

RethinkDB v1.15.2 - single node for development.

## Quickstart

```
docker pull devdb/rethinkdb:latest
docker run -d --name rethinkdb -p 8080:8080 devdb/rethinkdb:latest
```

then point your browser to `http://localhost:8080` and the RethinkDB Web UI will come up.

**Warning**: The data in RethinkDB is lost when the container is destroyed. If you want the data to persist, then start RethinkDB using:

```
docker pull devdb/rethinkdb:latest
docker run -d --name rethinkdb -p 8080:8080 -v /tmp/rethinkdb:/data devdb/rethinkdb:latest
```

and RethinkDB in the container will dump the data into `/tmp/rethinkdb` on your host machine.
