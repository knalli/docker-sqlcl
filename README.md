# docker-sqlcl

Oracle SQLcl docker container

<!-- TOC depthFrom:2 -->

- [Install](#install)
- [Run](#run)
- [Volumes](#volumes)

<!-- /TOC -->

## Install

First [download Oracle SQLcl](http://www.oracle.com/technetwork/developer-tools/sqlcl/downloads/index.html)

```bash
git clone https://github.com/martindsouza/docker-sqlcl

cd docker-sqlcl
# *** Copy the downloaded sqlcl.zip file into this directory ***

docker build -t martindsouza/docker-sqlcl .
```

## Run

The following is focused on MacOS / Linux users.

- Create alias

```bash
alias sqlcl="docker run -it --rm \
  -v `pwd`:/sqlcl \
  martindsouza/docker-sqlcl"
```

- Then to run execute: `sqlcl <connection string>`

## Volumes

Parameter | Description
---------|----------
`/sqlcl` | This is the folder that SQLcl will 