# docker-ttrss

This repo is based on the work of [fischerman/docker-ttrss](https://github.com/fischerman/docker-ttrss), I only needed to add the [Feedly theme](https://github.com/levito/tt-rss-feedly-theme)  

## About Tiny Tiny RSS

> *From [the official readme](http://tt-rss.org/redmine/projects/tt-rss/wiki):*

Tiny Tiny RSS is an open source web-based news feed (RSS/Atom) reader and aggregator,
designed to allow you to read news from any location,
while feeling as close to a real desktop application as possible.

![](http://tt-rss.org/images/1.9/1.jpg)

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
