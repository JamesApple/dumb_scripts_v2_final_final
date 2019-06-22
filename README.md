# Dumb Scripts V2 Final Final

A collection of scripts I use infrequently but desperately don't want to write
again anytime soon.

## examine_pg_dump

### Requirements

* Docker
* .sql dump from an existing PostgreSQL database

### Why?

Downloading and installing postgres on my local machine just to poke at
someones data seems a bit much.

This takes the dump and loads it into a docker container which can then be
interacted with through external GUI tooling or the container directly.

It does unfortunately leave the volume behind in ~/docker/volumes/postgres but
postgres needs a mounted volume to not chuck on startup.

### Usage

```
./examine_pg_dump ~/Desktop/dump.sql
```
