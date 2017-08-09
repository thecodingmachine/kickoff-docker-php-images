Base Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

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