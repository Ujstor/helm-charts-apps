# docker-mailserver

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 4.0.7](https://img.shields.io/badge/AppVersion-4.0.7-informational?style=flat-square)

Mailserver chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://docker-mailserver.github.io/docker-mailserver-helm | dockermailserver(docker-mailserver) | 4.0.7 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| certificates.duration | string | `"2160h"` |  |
| certificates.issuerRef.kind | string | `"Issuer"` |  |
| certificates.issuerRef.name | string | `"letsencrypt-issuer"` |  |
| certificates.organization | string | `"Organization"` |  |
| certificates.renewBefore | string | `"360h"` |  |
| dockermailserver.certificate | string | `"mailserver-tls"` |  |
| dockermailserver.deployment.env.OVERRIDE_HOSTNAME | string | `"mail.domain.com"` |  |

