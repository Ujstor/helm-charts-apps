# K8s Apps Helm Charts

Helm chart collection that simplifies Kubernetes configuration to be production-ready.

# gitea

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.22.3](https://img.shields.io/badge/AppVersion-1.22.3-informational?style=flat-square)

Gitea Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://dl.gitea.com/charts/ | gitea | 10.6.0 |
| https://ujstor.github.io/helm-charts-system | secret-store | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| gitea.gitea.admin.existingSecret | string | `"gitea-admin-secret"` |  |
| gitea.persistence.size | string | `"5Gi"` |  |
| secret-store.secretStore.clusterWide | bool | `false` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.create | bool | `true` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.name | string | `"gitea-secret-store-sa"` |  |
| secret-store.secretStore.provider.type | string | `"kubernetes"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

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
| plausible-analytics.disableRegistration | bool | `false` |  |
| plausible-analytics.image.pullPolicy | string | `"IfNotPresent"` |  |
| plausible-analytics.image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| plausible-analytics.image.tag | string | `"v2.1.4"` |  |
| plausible-analytics.logFailedLoginAttempts | bool | `true` |  |
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


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# uptime-kuma

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.23.13](https://img.shields.io/badge/AppVersion-1.23.13-informational?style=flat-square)

Uptime Kuma Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.irsigler.cloud | uptime-kuma | 2.20.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| uptime-kuma.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| uptime-kuma.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| uptime-kuma.ingress.annotations."nginx.ingress.kubernetes.io/proxy-read-timeout" | string | `"3600"` |  |
| uptime-kuma.ingress.annotations."nginx.ingress.kubernetes.io/proxy-send-timeout" | string | `"3600"` |  |
| uptime-kuma.ingress.annotations."nginx.ingress.kubernetes.io/server-snippets" | string | `"location / {\n  proxy_set_header Upgrade $http_upgrade;\n  proxy_http_version 1.1;\n  proxy_set_header X-Forwarded-Host $http_host;\n  proxy_set_header X-Forwarded-Proto $scheme;\n  proxy_set_header X-Forwarded-For $remote_addr;\n  proxy_set_header Host $host;\n  proxy_set_header Connection \"upgrade\";\n  proxy_set_header X-Real-IP $remote_addr;\n  proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;\n  proxy_set_header   Upgrade $http_upgrade;\n  proxy_cache_bypass $http_upgrade;\n}\n"` |  |
| uptime-kuma.ingress.className | string | `"nginx"` |  |
| uptime-kuma.ingress.enabled | bool | `false` |  |
| uptime-kuma.ingress.hosts[0].host | string | `"uptime.domain.com"` |  |
| uptime-kuma.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| uptime-kuma.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| uptime-kuma.ingress.tls[0].hosts[0] | string | `"uptime.domain.com"` |  |
| uptime-kuma.ingress.tls[0].secretName | string | `"uptime-kuma-tls"` |  |
| uptime-kuma.resources.limits.cpu | string | `"500m"` |  |
| uptime-kuma.resources.limits.memory | string | `"512Mi"` |  |
| uptime-kuma.resources.requests.cpu | string | `"100m"` |  |
| uptime-kuma.resources.requests.memory | string | `"128Mi"` |  |
| uptime-kuma.volume.accessMode | string | `"ReadWriteOnce"` |  |
| uptime-kuma.volume.enabled | bool | `true` |  |
| uptime-kuma.volume.size | string | `"2Gi"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# wordpress

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 6.7.1](https://img.shields.io/badge/AppVersion-6.7.1-informational?style=flat-square)

Wordpress Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | wordpress | 24.0.7 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| wordpress.autoscaling.enabled | bool | `false` |  |
| wordpress.autoscaling.maxReplicas | int | `11` |  |
| wordpress.autoscaling.minReplicas | int | `1` |  |
| wordpress.autoscaling.targetCPU | int | `50` |  |
| wordpress.autoscaling.targetMemory | int | `50` |  |
| wordpress.containerPorts.http | int | `8080` |  |
| wordpress.containerPorts.https | int | `8443` |  |
| wordpress.existingSecret | string | `""` |  |
| wordpress.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| wordpress.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| wordpress.ingress.enabled | bool | `false` |  |
| wordpress.ingress.hostname | string | `"wordpress.test.com"` |  |
| wordpress.ingress.ingressClassName | string | `"nginx"` |  |
| wordpress.ingress.path | string | `"/"` |  |
| wordpress.ingress.pathType | string | `"Prefix"` |  |
| wordpress.ingress.tls | bool | `true` |  |
| wordpress.mariadb.architecture | string | `"standalone"` |  |
| wordpress.mariadb.auth.database | string | `"bitnami_wordpress"` |  |
| wordpress.mariadb.auth.password | string | `""` |  |
| wordpress.mariadb.auth.rootPassword | string | `""` |  |
| wordpress.mariadb.auth.username | string | `"bn_wordpress"` |  |
| wordpress.mariadb.enabled | bool | `true` |  |
| wordpress.mariadb.primary.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| wordpress.mariadb.primary.persistence.enabled | bool | `true` |  |
| wordpress.mariadb.primary.persistence.size | string | `"2Gi"` |  |
| wordpress.mariadb.primary.persistence.storageClass | string | `""` |  |
| wordpress.mariadb.primary.resources | object | `{}` |  |
| wordpress.mariadb.primary.resourcesPreset | string | `"micro"` |  |
| wordpress.persistence.accessMode | string | `"ReadWriteOnce"` |  |
| wordpress.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| wordpress.persistence.dataSource | object | `{}` |  |
| wordpress.persistence.enabled | bool | `true` |  |
| wordpress.persistence.existingClaim | string | `""` |  |
| wordpress.persistence.selector | object | `{}` |  |
| wordpress.persistence.size | string | `"2Gi"` |  |
| wordpress.persistence.storageClass | string | `""` |  |
| wordpress.replicaCount | int | `1` |  |
| wordpress.resourcesPreset | string | `"micro"` |  |
| wordpress.service.httpsTargetPort | string | `"https"` |  |
| wordpress.service.ports.http | int | `80` |  |
| wordpress.service.ports.https | int | `443` |  |
| wordpress.service.type | string | `"ClusterIP"` |  |
| wordpress.wordpressBlogName | string | `"User's Blog!"` |  |
| wordpress.wordpressEmail | string | `"user@example.com"` |  |
| wordpress.wordpressFirstName | string | `"FirstName"` |  |
| wordpress.wordpressLastName | string | `"LastName"` |  |
| wordpress.wordpressPassword | string | `""` |  |
| wordpress.wordpressScheme | string | `"http"` |  |
| wordpress.wordpressTablePrefix | string | `"wp_"` |  |
| wordpress.wordpressUsername | string | `"user"` |  |


