# plausible-analytics

![Version: 0.3.3](https://img.shields.io/badge/Version-0.3.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.1.1](https://img.shields.io/badge/AppVersion-2.1.1-informational?style=flat-square)

A Helm Chart for Plausible Analytics - Simple, open-source, lightweight (< 1 KB) and privacy-friendly web analytics alternative to Google Analytics.

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| IMIO |  | <https://github.com/IMIO/> |

## Source Code

* <https://github.com/plausible/analytics>
* <https://github.com/imio/helm-charts>
* <https://github.com/imio/helm-plausible-analytics>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | clickhouse(clickhouse) | 3.6.7 |
| https://charts.bitnami.com/bitnami | postgresql(postgresql) | 12.8.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| baseURL | string | `"http://plausible-analytics.local"` |  |
| clickhouse | object | `{"auth":{"database":"plausible_events_db","password":"password","username":"clickhouse"},"enabled":true,"initContainers":[],"initdbScripts":{"db-init.sql":"CREATE DATABASE IF NOT EXISTS plausible_events_db\n"},"persistence":{"enabled":false},"replicaCount":1,"shards":1,"zookeeper":{"enabled":false}}` | ---------------------------------------------------------------------------- |
| clickhouseDatabaseURL | string | `"http://clickhouse:password@plausible-analytics-clickhouse:8123/plausible_events_db"` |  |
| clickhouseFlushIntervalMS | string | `""` |  |
| clickhouseMaxBufferSize | string | `""` |  |
| databaseCA | string | `nil` |  |
| databaseURL | string | `"postgres://postgres:postgres@plausible-analytics-postgresql:5432/plausible_db"` |  |
| disableRegistration | bool | `false` |  |
| extraEnv | list | `[]` |  |
| extra_geolocation.enabled | bool | `false` |  |
| extra_geolocation.geolite2CountryDB | string | `""` |  |
| extra_geolocation.geonamesSourceFile | string | `""` |  |
| extra_geolocation.maxmind.edition | string | `""` |  |
| extra_geolocation.maxmind.licenseKey | string | `""` |  |
| fullnameOverride | string | `""` |  |
| google.clientID | string | `nil` |  |
| google.clientSecret | string | `nil` |  |
| google.enabled | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| image.tag | string | `"v2.1.4"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts | list | `[]` |  |
| ingress.path | string | `"/"` |  |
| ingress.pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| labels | object | `{}` |  |
| listenIP | string | `"0.0.0.0"` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| logFailedLoginAttempts | bool | `false` |  |
| mailer.adapter | string | `""` |  |
| mailer.email | string | `""` |  |
| mailer.enabled | bool | `false` |  |
| mailer.mailgun.apiKey | string | `""` |  |
| mailer.mailgun.baseURI | string | `""` |  |
| mailer.mailgun.domain | string | `""` |  |
| mailer.mandrillApiKey | string | `""` |  |
| mailer.postmarkApiKey | string | `""` |  |
| mailer.sendgridApiKey | string | `""` |  |
| mailer.smtp.auth | bool | `false` |  |
| mailer.smtp.host | string | `""` |  |
| mailer.smtp.password | string | `""` |  |
| mailer.smtp.port | string | `""` |  |
| mailer.smtp.retries | string | `""` |  |
| mailer.smtp.ssl | bool | `false` |  |
| mailer.smtp.username | string | `""` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| plausibleInitContainers.clickhouse.image.repository | string | `"bitnami/clickhouse"` |  |
| plausibleInitContainers.clickhouse.image.tag | string | `"23.3.9"` |  |
| plausibleInitContainers.curl.enabled | bool | `false` |  |
| plausibleInitContainers.curl.image.repository | string | `"curlimages/curl"` |  |
| plausibleInitContainers.curl.image.tag | string | `"8.2.1"` |  |
| plausibleInitContainers.enabled | bool | `true` |  |
| plausibleInitContainers.postgresql.image.repository | string | `"postgres"` |  |
| plausibleInitContainers.postgresql.image.tag | string | `"13.3-alpine"` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresql | object | `{"auth":{"database":"plausible_db","password":"postgres","username":"postgres"},"enabled":true,"metrics":{"enabled":false},"port":5432,"primary":{"persistence":{"enabled":false}},"replication":{"enabled":false}}` | ---------------------------------------------------------------------------- |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| readinessProbe.initialDelaySeconds | int | `30` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| secret.create | bool | `true` |  |
| secret.existingSecret | string | `""` |  |
| secretKeyBase | string | `""` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| totpVaultKey | string | `"dsxvbn3jxDd16az2QpsX5B8O+llxjQ2SJE2i5Bzx38I="` |  |

