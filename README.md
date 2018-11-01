# Locust example

https://github.com/algas/locust-example

## Tutorial

1. Run your web server with a terminal
`./web`
2. Execute locust with another terminal
`./locust -f locustfile.py --host  http://host.docker.internal:8888`
3. Open web with your web browser
http://localhost:8089

## Run local with web

```
docker run --rm -p 8089:8089 -w /work -v $(pwd):/work algas/locust -f your-locustfile.py --host http://example.com
```

## Run local without web

```
docker run --rm -w /work -v $(pwd):/work algas/locust -f your-locustfile.py --no-web -c 100 -r 10 --host http://example.com
```
