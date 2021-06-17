## KrakenD serving GraphQL data from REST endpoint

To try this demo execute the docker-compose included in this repo from its root folder:

```shell
$ docker-compose up
```

This repo contains 3 simple example use cases from KrakenD:
1. An example JSON response from a fake REST api (http://localhost:8080/user/1.json)
2. An example response that aggregates data from 2 requests to GitHub -users & repos- from one single endpoint (http://localhost:8080/github/github-username-here)
3. An example response that returns the response of a GrahQL backend from a simple REST endpoint (http://localhost:8080/graphql/hello-world)

Relevant files:
- `krakend/krakend.json`: the KrakenD config file, including the API Gateway behaviour
- `data/user/1.json`: the mocked answer that will be returned by the fake REST Api
- `graphql-server/server.js` the fake GraphQL server definition (using Express)
