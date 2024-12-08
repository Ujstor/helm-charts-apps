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
| gitea.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/force-ssl-redirect" | string | `"true"` |  |
| gitea.ingress.className | string | `"nginx"` |  |
| gitea.ingress.enabled | bool | `false` |  |
| gitea.ingress.hosts[0].host | string | `"gitea.domain.com"` |  |
| gitea.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| gitea.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| gitea.ingress.tls[0].hosts[0] | string | `"gitea.domain.com"` |  |
| gitea.ingress.tls[0].secretName | string | `"gitea-tls"` |  |
| gitea.persistence.size | string | `"5Gi"` |  |
| secret-store.secretStore.clusterWide | bool | `false` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.create | bool | `true` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.name | string | `"gitea-secret-store-sa"` |  |
| secret-store.secretStore.provider.type | string | `"kubernetes"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# gitlab

![Version: 8.6.1](https://img.shields.io/badge/Version-8.6.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 17.6.1](https://img.shields.io/badge/AppVersion-17.6.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.gitlab.io | gitlab-runner | 0.71.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| gitlab-runner.concurrent | int | `10` |  |
| gitlab-runner.gitlabUrl | string | `"http://gitlab-webservice-default.gitlab.svc.cluster.local:8181"` |  |
| gitlab-runner.rbac.create | bool | `true` |  |
| gitlab-runner.rbac.rules[0].apiGroups[0] | string | `""` |  |
| gitlab-runner.rbac.rules[0].resources[0] | string | `"pods"` |  |
| gitlab-runner.rbac.rules[0].verbs[0] | string | `"get"` |  |
| gitlab-runner.rbac.rules[0].verbs[1] | string | `"list"` |  |
| gitlab-runner.rbac.rules[0].verbs[2] | string | `"watch"` |  |
| gitlab-runner.rbac.rules[0].verbs[3] | string | `"create"` |  |
| gitlab-runner.rbac.rules[0].verbs[4] | string | `"delete"` |  |
| gitlab-runner.rbac.rules[1].apiGroups[0] | string | `""` |  |
| gitlab-runner.rbac.rules[1].resources[0] | string | `"pods/exec"` |  |
| gitlab-runner.rbac.rules[1].verbs[0] | string | `"create"` |  |
| gitlab-runner.rbac.rules[1].verbs[1] | string | `"patch"` |  |
| gitlab-runner.rbac.rules[1].verbs[2] | string | `"delete"` |  |
| gitlab-runner.rbac.rules[2].apiGroups[0] | string | `""` |  |
| gitlab-runner.rbac.rules[2].resources[0] | string | `"pods/attach"` |  |
| gitlab-runner.rbac.rules[2].verbs[0] | string | `"list"` |  |
| gitlab-runner.rbac.rules[2].verbs[1] | string | `"get"` |  |
| gitlab-runner.rbac.rules[2].verbs[2] | string | `"create"` |  |
| gitlab-runner.rbac.rules[2].verbs[3] | string | `"delete"` |  |
| gitlab-runner.rbac.rules[2].verbs[4] | string | `"update"` |  |
| gitlab-runner.rbac.rules[3].apiGroups[0] | string | `""` |  |
| gitlab-runner.rbac.rules[3].resources[0] | string | `"secrets"` |  |
| gitlab-runner.rbac.rules[3].verbs[0] | string | `"list"` |  |
| gitlab-runner.rbac.rules[3].verbs[1] | string | `"get"` |  |
| gitlab-runner.rbac.rules[4].apiGroups[0] | string | `""` |  |
| gitlab-runner.rbac.rules[4].resources[0] | string | `"configmaps"` |  |
| gitlab-runner.rbac.rules[4].verbs[0] | string | `"list"` |  |
| gitlab-runner.rbac.rules[4].verbs[1] | string | `"get"` |  |
| gitlab-runner.rbac.rules[4].verbs[2] | string | `"create"` |  |
| gitlab-runner.rbac.rules[4].verbs[3] | string | `"delete"` |  |
| gitlab-runner.runners.config | string | `"[[runners]]\n  [runners.kubernetes]\n    namespace = \"{{.Release.Namespace}}\"\n    image = \"alpine\"\n    privileged = false\n"` |  |
| gitlab-runner.secrets[0].items[0].key | string | `"runner-registration-token"` |  |
| gitlab-runner.secrets[0].items[0].path | string | `"runner-registration-token"` |  |
| gitlab-runner.secrets[0].name | string | `"gitlab-gitlab-runner-secret"` |  |
| gitlab.certIssuerEmail | string | `"mail@mail.com"` |  |
| gitlab.domain | string | `"domain.com"` |  |
| gitlab.ingressClassName | string | `nil` |  |
| gitlab.version | string | `nil` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# harbor

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.12.0](https://img.shields.io/badge/AppVersion-2.12.0-informational?style=flat-square)

Harbor Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.goharbor.io | harbor | 1.16.0 |
| https://ujstor.github.io/helm-charts-system | minio-tenant | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| harbor.cache.enabled | bool | `false` |  |
| harbor.cache.expireHours | int | `24` |  |
| harbor.existingSecretAdminPassword | string | `"harbor-admin-secret"` |  |
| harbor.existingSecretSecretKey | string | `"harbor-secretkey-secret"` |  |
| harbor.expose.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-body-size" | string | `"0"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-buffering" | string | `"off"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-connect-timeout" | string | `"300"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-read-timeout" | string | `"300"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-send-timeout" | string | `"300"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/ssl-redirect" | string | `"true"` |  |
| harbor.expose.ingress.className | string | `"nginx"` |  |
| harbor.expose.ingress.hosts.core | string | `"harbor.domain.com"` |  |
| harbor.expose.tls.certSource | string | `"secret"` |  |
| harbor.expose.tls.enabled | bool | `true` |  |
| harbor.expose.tls.secret.secretName | string | `"harbor-ingress"` |  |
| harbor.expose.type | string | `"ingress"` |  |
| harbor.externalURL | string | `"https://harbor.domain.com"` |  |
| harbor.internalTLS.enabled | bool | `false` |  |
| harbor.ipFamily.ipv4.enabled | bool | `true` |  |
| harbor.ipFamily.ipv6.enabled | bool | `false` |  |
| harbor.persistence.enabled | bool | `true` |  |
| harbor.persistence.imageChartStorage.disableredirect | bool | `true` |  |
| harbor.persistence.imageChartStorage.s3.bucket | string | `"harbor-bucket"` |  |
| harbor.persistence.imageChartStorage.s3.chunksize | string | `"5242880"` |  |
| harbor.persistence.imageChartStorage.s3.existingSecret | string | `"harbor-s3-secret"` |  |
| harbor.persistence.imageChartStorage.s3.multipartcopychunksize | string | `"33554432"` |  |
| harbor.persistence.imageChartStorage.s3.multipartcopymaxconcurrency | int | `100` |  |
| harbor.persistence.imageChartStorage.s3.region | string | `"us-east-1"` |  |
| harbor.persistence.imageChartStorage.s3.regionendpoint | string | `"http://minio-harbor-hl.harbor.svc.cluster.local:9000"` |  |
| harbor.persistence.imageChartStorage.s3.rootdirectory | string | `"/registry"` |  |
| harbor.persistence.imageChartStorage.s3.secure | bool | `false` |  |
| harbor.persistence.imageChartStorage.s3.skipverify | bool | `true` |  |
| harbor.persistence.imageChartStorage.s3.v4auth | bool | `true` |  |
| harbor.persistence.imageChartStorage.type | string | `"s3"` |  |
| harbor.persistence.persistentVolumeClaim.database.accessMode | string | `"ReadWriteOnce"` |  |
| harbor.persistence.persistentVolumeClaim.database.size | string | `"1Gi"` |  |
| harbor.persistence.persistentVolumeClaim.jobservice.accessMode | string | `"ReadWriteOnce"` |  |
| harbor.persistence.persistentVolumeClaim.jobservice.size | string | `"1Gi"` |  |
| harbor.persistence.persistentVolumeClaim.redis.accessMode | string | `"ReadWriteOnce"` |  |
| harbor.persistence.persistentVolumeClaim.redis.size | string | `"1Gi"` |  |
| harbor.persistence.persistentVolumeClaim.registry.accessMode | string | `"ReadWriteOnce"` |  |
| harbor.persistence.persistentVolumeClaim.registry.size | string | `"5Gi"` |  |
| harbor.persistence.persistentVolumeClaim.trivy.accessMode | string | `"ReadWriteOnce"` |  |
| harbor.persistence.persistentVolumeClaim.trivy.size | string | `"5Gi"` |  |
| harbor.persistence.resourcePolicy | string | `"keep"` |  |
| harbor.registry.relativeurls | bool | `true` |  |
| harbor.trivy.enabled | bool | `true` |  |
| harbor.trivy.gitHubToken | string | `""` |  |
| minio-tenant.minio-tenant.tenant.buckets[0].name | string | `"harbor-bucket"` |  |
| minio-tenant.minio-tenant.tenant.buckets[0].objectLock | bool | `false` |  |
| minio-tenant.minio-tenant.tenant.buckets[0].region | string | `"us-east-1"` |  |
| minio-tenant.minio-tenant.tenant.configuration.name | string | `"minio-admin-secret"` |  |
| minio-tenant.minio-tenant.tenant.name | string | `"minio-harbor"` |  |
| minio-tenant.minio-tenant.tenant.pools[0].name | string | `"pool-0"` |  |
| minio-tenant.minio-tenant.tenant.pools[0].servers | int | `1` |  |
| minio-tenant.minio-tenant.tenant.pools[0].size | string | `"20Gi"` |  |
| minio-tenant.minio-tenant.tenant.pools[0].volumesPerServer | int | `1` |  |


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
| plausible-analytics.image.repository | string | `"docker.io/plausible/analytics"` |  |
| plausible-analytics.image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| plausible-analytics.image.tag | string | `"v2.1.4"` |  |
| plausible-analytics.image.tag | string | `"v2.0.0"` |  |
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


