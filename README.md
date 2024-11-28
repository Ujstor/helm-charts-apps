# K8s Apps Helm Charts

Helm chart collection that simplifies Kubernetes configuration to be production-ready.

# gitea

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.22.3](https://img.shields.io/badge/AppVersion-1.22.3-informational?style=flat-square)

Gitea Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://dl.gitea.com/charts/ | gitea | 10.6.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| gitea.persistence.size | string | `"5Gi"` |  |


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
| baseURL | string | `"http://plausible-analytics.local"` |  |
| customIngress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| customIngress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
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


