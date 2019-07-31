# Nginx proxy for Elasticsearch
- Load balanced cluster
- HTTP connections keep alive for better performance

`docker-compose up`

Validate open connections:

`curl localhost:8080/_nodes/stats/http?pretty | grep total_opened`

Validate load balancing:

`curl localhost:8080 | grep es0` 