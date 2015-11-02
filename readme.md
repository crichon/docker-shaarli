# Shaarli Docker

## Presentation

[Shaarli](http://sebsauvage.net/wiki/doku.php?id=php:shaarli)

> a minimalist delicious clone you can install on your own website. It is designed to be personal (single-user), fast and handy.

In this directory you will find the dockerfile providing crichon/shaarli.
Based on [php:apache](https://registry.hub.docker.com/_/php/)

## Usage

Just run:

    docker run --name shaarli crichon/shaarli:latest

Shaarli be available on http://localhost:80

If you prefer you can use the compose file in order to start an automatic reverse proxy.
It should then be available on http://shaarli.localdomain.


Build and run:

    docker build --name shaarli shaarli/
    docker run --name shaarli shaarli

## Details

**php:apache** use port 80 by default, refer to [its](https://registry.hub.docker.com/_/php/) documentation for details.

All data are contained inside the volume:

    /var/www/html/data

If you are using the compose file, data would be kept thanks to a data container.
