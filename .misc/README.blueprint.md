<p align="center">
    <img src="https://user-images.githubusercontent.com/8983173/28176182-c45b1196-67f6-11e7-8d96-fd1aefd3fcab.png" alt="kickoff-docker-php's logo" width="200" height="200" />
</p>
<h3 align="center">kickoff-docker-php-images</h3>
<p align="center">Base images of the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project</p>
<p align="center">
    <a href="https://github.com/thecodingmachine/kickoff-docker-php/tree/master"><img src="https://img.shields.io/badge/beta-2.0-yellow.svg" alt="Beta release: 2.0"></a>
    <a href="https://github.com/thecodingmachine/kickoff-docker-php/tree/v1.0.3"><img src="https://img.shields.io/badge/stable-1.0.3-green.svg" alt="Stable release: 1.0.3"></a>
</p>

---

This is the Git repository of the Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

# Menu

* [Toolbox](#toolbox)
* [PHP-FPM](#php-fpm)
* [NGINX](#nginx)

## Toolbox
{{ range $version := .Values.Images.toolbox.php_versions }}
| Name                       | Version                                              |
|----------------------------|------------------------------------------------------|
| Base image                 | `php:{{ $version }}-alpine`                          |
| APCu                       | `{{ $.Values.Images.toolbox.apcu_version }}`         |
| PHP extension for Redis    | `{{ $.Values.Images.toolbox.phpredis_version }}`     |
| Composer                   | `{{ $.Values.Images.toolbox.composer_version }}`     |
| prestissimo                | `{{ $.Values.Images.toolbox.prestissimo_version }}`  |
| PHP Coding Standards Fixer | `{{ $.Values.Images.toolbox.php_cs_fixer_version }}` |
| NodeJS                     | `{{ $.Values.Images.toolbox.node_version }}`         |
{{ end }}
## PHP-FPM

TODO

## NGINX

TODO