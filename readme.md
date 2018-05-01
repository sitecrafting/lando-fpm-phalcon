# Lando FPM Phalcon

This a Lando image built for use with PHP-FPM, Nginx, and Phalcon.

## Usage with Lando

This image was designed to work as an override for the `php` service within Lando's `lemp` recipe:

```yaml
name: my-phalcon-app
recipe: lemp
config:
  webroot: www

services:
  appserver:
    type: php:custom
    overrides:
      services:
        image: sitecrafting/lando-fpm-phalcon
```

Lando-FPM-Phalcon _should_ be generic enough to work as a drop-in replacement for any PHP-FPM-based PHP service. 

## Usage with vanilla Docker

Run a barebones image without Lando:

```bash
docker run -it -p 8080:80 -v /path/to/your/app/root:/var/www sitecrafting/lando-fpm-phalcon
```

## Issues/Contributions

Reach out with a GH issue or PR, and I'll get my people to work on it.

## License

MIT
