# How to use

## First use

For fisrt usage, you need to build image docker.

``` bash
docker-compose build
```

## Quick start
```
docker network create nw_twint
docker-compose up -d elasticsearch
sleep 10
docker-compose up -d searchapp
docker-compose run twint -u noneprivacy -es elasticsearch:9200 --json -o /opt/twint/noneprivacy.json
open http://localhost:3000
```

## Twint, Elasticsearch & Searchapp

Start to up elaticsearch and searchapp

``` bash
docker network create nw_twint
docker-compose up -d elasticsearch searchapp twint

```

## Execute Twint command

``` bash
docker network create nw_twint
docker-compose run -v $PWD/output:/srv/twint twint {{CMD TWINT}}
```

## Examples of command

A few simple examples to help you understand the basics:

``` bash
docker-compose run twint -u username -es elasticsearch:9200
docker-compose run twint -u username -es elasticsearch:9200 --json -o /opt/twint/username.json
```

if local install of twint
``` bash
twint -u username -es localhost:9200
twint -u username -es localhost:9200 --json -o /opt/twint/username.json
```

## Screenshots
![alt text](https://github.com/lucmski/twint-search/raw/master/docs/screenshot1.png "Screenshot #1")

![alt text](https://github.com/lucmski/twint-search/raw/master/docs/screenshot2.png "Screenshot #2")
