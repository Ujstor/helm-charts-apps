# plausible-analytics

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.0.0](https://img.shields.io/badge/AppVersion-2.0.0-informational?style=flat-square)

Plausible-analytics Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://imio.github.io/helm-charts | plausible-analytics | 0.3.3 |
| https://ujstor.github.io/helm-charts-system | secret-store | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| customIngress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/proxy-read-timeout" | string | `"3600"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/proxy-send-timeout" | string | `"3600"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/server-snippets" | string | `"location / {\n  proxy_set_header Upgrade $http_upgrade;\n  proxy_http_version 1.1;\n  proxy_set_header X-Forwarded-Host $http_host;\n  proxy_set_header X-Forwarded-Proto $scheme;\n  proxy_set_header X-Forwarded-For $remote_addr;\n  proxy_set_header Host $host;\n  proxy_set_header Connection \"upgrade\";\n  proxy_set_header X-Real-IP $remote_addr;\n  proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;\n  proxy_set_header   Upgrade $http_upgrade;\n  proxy_cache_bypass $http_upgrade;\n}\n"` |  |
| customIngress.className | string | `"nginx"` |  |
| customIngress.enabled | bool | `false` |  |
| customIngress.hosts[0].host | string | `"plausible-analytics.local"` |  |
| customIngress.hosts[0].paths[0].path | string | `"/"` |  |
| customIngress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| customIngress.tls[0].hosts[0] | string | `"plausible-analytics.local"` |  |
| customIngress.tls[0].secretName | string | `"plausible-analytics-tls"` |  |
| plausible-analytics.baseURL | string | `"http://plausible-analytics.local"` |  |
| plausible-analytics.disableRegistration | bool | `true` |  |
| plausible-analytics.image.repository | string | `"docker.io/plausible/analytics"` |  |
| plausible-analytics.image.tag | string | `"v2.0.0"` |  |
| plausible-analytics.logFailedLoginAttempts | bool | `true` |  |
| plausible-analytics.postgresql.enabled | bool | `true` |  |
| plausible-analytics.postgresql.primary.persistence.enabled | bool | `true` |  |
| plausible-analytics.replicaCount | int | `1` |  |
| plausible-analytics.resources.limits.cpu | string | `"500m"` |  |
| plausible-analytics.resources.limits.memory | string | `"512Mi"` |  |
| plausible-analytics.resources.requests.cpu | string | `"100m"` |  |
| plausible-analytics.resources.requests.memory | string | `"128Mi"` |  |
| plausible-analytics.service.port | int | `80` |  |
| plausible-analytics.service.type | string | `"ClusterIP"` |  |
| plausible-analytics.totpVaultKey | string | `""` |  |
| secret-store.secretStore.clusterWide | bool | `false` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.create | bool | `true` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.name | string | `"analytics-secret-store-sa"` |  |
| secret-store.secretStore.provider.type | string | `"kubernetes"` |  |

