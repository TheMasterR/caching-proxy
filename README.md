# Caching proxy docker image

[![Docker Pulls](https://img.shields.io/docker/pulls/themasterr/caching-proxy.svg)](https://hub.docker.com/r/themasterr/caching-proxy)

Front your webserver containers with a transparent cache.

## What does it do?

Runs an nginx server as a caching reverse proxy for a given URL.

## Usage

Environment variables:

- `UPSTREAM`: URL of the upstream service which should be cached (Required)
- `MAX_SIZE`: Size of the cache to use (on-disk) (Required)
- `ALLOWED_ORIGIN`: origin URL which is allowed to load the files from this server (header `Access-Control-Allowed-Origins`) (default `*`)
- `GZIP`: Set to `off` in order to disable gzip compression (enabled by default)

The server will be listening on port 80.

Use [docker-compose.yml](docker-compose.yml) for an example.
