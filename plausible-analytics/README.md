# plausible-analytics

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.1.1](https://img.shields.io/badge/AppVersion-2.1.1-informational?style=flat-square)

Plausible-analytics Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://imio.github.io/helm-charts | plausible-analytics | 0.3.3 |
| https://ujstor.github.io/helm-charts-system | secret-store | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| baseURL | string | `"http://plausible-analytics.local"` |  |
| customIngress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/proxy-connect-timeout" | string | `"3600"` |  |
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
| disableRegistration | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| image.tag | string | `"v2.1.4"` |  |
| logFailedLoginAttempts | bool | `true` |  |
| replicaCount | int | `1` |  |
| resources.limits.cpu | string | `"200m"` |  |
| resources.limits.memory | string | `"256Mi"` |  |
| resources.requests.cpu | string | `"100m"` |  |
| resources.requests.memory | string | `"128Mi"` |  |
| secret-store.secretStore.clusterWide | bool | `false` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.create | bool | `true` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.name | string | `"analytics-secret-store-sa"` |  |
| secret-store.secretStore.provider.type | string | `"kubernetes"` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |

