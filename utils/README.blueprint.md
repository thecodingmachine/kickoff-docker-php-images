Base Docker images for the [kickoff-docker-php](https://github.com/thecodingmachine/kickoff-docker-php/) project.

## Toolbox
{{ range $image := .Values.Images.toolbox }}
### {{ $image.tag }}

| Name       | Version                                    |
|------------|--------------------------------------------|
| Base image | `alpine:{{ $image.stack.alpine_version }}` |
| OpenSSL    | `{{ $image.stack.openssl_version }}`       |
{{ end }}
## PHP-FPM
{{ range $image := .Values.Images.phpfpm }}
### {{ $image.tag }}

| Name                       | Version                                         |
|----------------------------|-------------------------------------------------|
| Base image                 | `php:{{ $image.stack.php_version }}-fpm-alpine` |
| APCu                       | `{{ $image.stack.apcu_version }}`               |
| PHP extension for Redis    | `{{ $image.stack.phpredis_version }}`           |
{{- if $image.stack.yaml_version }}
| YAML                       | `{{ $image.stack.yaml_version }}`               |
{{- end }}
{{- if $image.stack.xdebug_version }}
| Xdebug                     | `{{ $image.stack.xdebug_version }}`             |
{{- end }}
| OpenSSL                    | `{{ $image.stack.openssl_version }}`            |
| Composer                   | `{{ $image.stack.composer_version }}`           |
| prestissimo                | `{{ $image.stack.prestissimo_version }}`        |
| PHP Coding Standards Fixer | `{{ $image.stack.php_cs_fixer_version }}`       |
| NodeJS                     | `{{ $image.stack.node_version }}`               |
| yarn                       | `{{ $image.stack.yarn_version }}`               |
{{ end }}