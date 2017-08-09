<p align="center">
    <img src="https://user-images.githubusercontent.com/8983173/28176182-c45b1196-67f6-11e7-8d96-fd1aefd3fcab.png" alt="kickoff-docker-php's logo" width="200" height="200" />
</p>
<h3 align="center">kickoff-docker-php-images</h3>
<p align="center">Base images of kickoff-docker-php</p>

---

This is the Git repository of the Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

# Menu

* [Toolbox](#toolbox)
* [PHP-FPM](#php-fpm)

## Toolbox

| Name                       | Version                                              |
|----------------------------|------------------------------------------------------|
| Base image                 | `php:7.1.8-alpine`                          |
| APCu                       | `5.1.8`         |
| PHP extension for Redis    | `3.1.3`     |
| Composer                   | `1.5.0`     |
| prestissimo                | `0.3.7`  |
| PHP Coding Standards Fixer | `2.4.0` |
| NodeJS                     | `6.10.3-r1`         |
| yarn                       | `0.23.3-r0`         |

## PHP-FPM

| Name                    | Version                                         |
|-------------------------|-------------------------------------------------|
| Base image              | `php:7.1.8-fpm-alpine`                 |
| APCu                    | `5.1.8`     |
| PHP extension for Redis | `3.1.3` |