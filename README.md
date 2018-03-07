# docker-ttrss

Tiny Tiny RSS docker container with Feedly theme

This repo is based on the work of [fischerman/docker-ttrss](https://github.com/fischerman/docker-ttrss), I only needed to add the [Feedly theme](https://github.com/levito/tt-rss-feedly-theme)

## Quickstart

### Install database

```
docker run -d --name ttrssdb nornagon/postgres
```

### Install ttrss

```
docker run -d  -e SELF_URL_PATH="http://YOURDOMAIN.COM" --link ttrssdb:db -p 80:80 kamasoutra/docker-ttrss
```

### More infos

See [fischerman/docker-ttrss repo](https://github.com/fischerman/docker-ttrss)
