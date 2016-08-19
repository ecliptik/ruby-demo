# ruby-demo
Simple demo ruby app for SDDevops Rancher presentation.

Uses [Sinatra](http://www.sinatrarb.com/) to define a single route.

* /
- display a random gif

# Deploy Locally

Deploy locally with [docker-compose](https://docs.docker.com/compose/) and listen on port 9292.

```
docker-compose up
```

# Deploy with Rancher

Deploy to [rancher](http://rancher.com/) and listen on port 20010.

```
rancher-compose --file docker-compose-rancher.yml \
                --rancher-file rancher-compose.yml \
                --project-name ruby-demo \
                up \
                --force-upgrade \
                --confirm-upgrade \
                --pull \
                -d
```
