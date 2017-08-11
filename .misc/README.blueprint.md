Base Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

## Toolbox

| Name       | Version                                        | Source     |
|------------|------------------------------------------------|------------|
| Base image | `alpine:3.6`                                   | Docker Hub |
| OpenSSL    | `{{ .Values.Images.toolbox.openssl_version }}` | Alpine     |

## PHP-FPM
{{ range $version := .Values.Images.phpfpm.php_versions }}
| Name                       | Version                                             | Source                            |
|----------------------------|-----------------------------------------------------|-----------------------------------|
| Base image                 | `php:{{ $version }}-fpm-alpine`                     | Docker Hub                        |
| APCu                       | `{{ $.Values.Images.phpfpm.apcu_version }}`         | GitHub                            |
| PHP extension for Redis    | `{{ $.Values.Images.phpfpm.phpredis_version }}`     | GitHub                            |
| OpenSSL                    | `{{ $.Values.Images.phpfpm.openssl_version }}`      | Alpine                            |
| Composer                   | `{{ $.Values.Images.phpfpm.composer_version }}`     | https://getcomposer.org/installer |
| prestissimo                | `{{ $.Values.Images.phpfpm.prestissimo_version }}`  | Composer                          |
| PHP Coding Standards Fixer | `{{ $.Values.Images.phpfpm.php_cs_fixer_version }}` | GitHub                            |
| NodeJS                     | `{{ $.Values.Images.phpfpm.node_version }}`         | Alpine                            |
| yarn                       | `{{ $.Values.Images.phpfpm.yarn_version }}`         | Alpine                            |
{{ end }}