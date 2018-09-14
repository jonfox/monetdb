# Supported tags and respective `Dockerfile` links
* `latest` [(Dockerfile)](https://github.com/topaztechnology/monetdb/blob/master/Dockerfile) - the latest release
* `11.27.5` [(Dockerfile)](https://github.com/topaztechnology/monetdb/blob/master/Dockerfile) - release based on MonetDB 11.27.5 sources

# Overview

A MonetDB image built from sources on top of an Alpine base image, which allows creation of a dbfarm and a database on startup.

Joyent's [Containerpilot](https://www.joyent.com/containerpilot) is used to manage job scheduling.

# How to use this image

`docker run -e 'MONET_DATABASE=docker' -p 50000:50000 -d topaztechnology/monetdb:latest`

# Environment variables

* **MONET_DBFARM** : the path to the Monet dbfarm, see [here](https://www.monetdb.org/Documentation/monetdbd) for more details. Defaults to `/var/lib/monetdb/dbfarm`.
* **MONET_DATABASE** : the name of the Monet database to be created.