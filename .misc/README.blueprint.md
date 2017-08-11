Base Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

## Toolbox
{{ range $image := .Values.Images.toolbox }}
### {{ $image.tag }}

| Name       | Version                                    | Source     |
|------------|--------------------------------------------|------------|
| Base image | `alpine:{{ $image.stack.alpine_version }}` | Docker Hub |
| OpenSSL    | `{{ $image.stack.openssl_version }}`       | Alpine     |
{{ end }}
## PHP-FPM
{{ range $image := .Values.Images.phpfpm }}
### {{ $image.tag }}

| Name                       | Version                                         | Source                            |
|----------------------------|-------------------------------------------------|-----------------------------------|
| Base image                 | `php:{{ $image.stack.php_version }}-fpm-alpine` | Docker Hub                        |
| APCu                       | `{{ $image.stack.apcu_version }}`               | GitHub                            |
| PHP extension for Redis    | `{{ $image.stack.phpredis_version }}`           | GitHub                            |
| OpenSSL                    | `{{ $image.stack.openssl_version }}`            | Alpine                            |
| Composer                   | `{{ $image.stack.composer_version }}`           | https://getcomposer.org/installer |
| prestissimo                | `{{ $image.stack.prestissimo_version }}`        | Composer                          |
| PHP Coding Standards Fixer | `{{ $image.stack.php_cs_fixer_version }}`       | GitHub                            |
| NodeJS                     | `{{ $image.stack.node_version }}`               | Alpine                            |
| yarn                       | `{{ $image.stack.yarn_version }}`               | Alpine                            |
{{ end }}