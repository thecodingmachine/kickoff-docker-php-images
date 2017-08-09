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
| yarn                       | `{{ $.Values.Images.toolbox.yarn_version }}`         |
{{ end }}
## PHP-FPM
{{ range $version := .Values.Images.phpfpm.php_versions }}
| Name                    | Version                                         |
|-------------------------|-------------------------------------------------|
| Base image              | `php:{{ $version }}-fpm-alpine`                 |
| APCu                    | `{{ $.Values.Images.phpfpm.apcu_version }}`     |
| PHP extension for Redis | `{{ $.Values.Images.phpfpm.phpredis_version }}` |
{{ end }}