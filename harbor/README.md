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
| harbor.expose.ingress.annotations."ingress.kubernetes.io/proxy-body-size" | string | `"0"` |  |
| harbor.expose.ingress.annotations."ingress.kubernetes.io/ssl-redirect" | string | `"true"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/proxy-body-size" | string | `"0"` |  |
| harbor.expose.ingress.annotations."nginx.ingress.kubernetes.io/ssl-redirect" | string | `"true"` |  |
| harbor.expose.ingress.className | string | `"nginx"` |  |
| harbor.expose.ingress.hosts.core | string | `"harbor.domain.com"` |  |
| harbor.expose.tls.certSource | string | `"auto"` |  |
| harbor.expose.tls.enabled | bool | `true` |  |
| harbor.expose.type | string | `"ingress"` |  |
| harbor.externalURL | string | `"https://harbor.domain.com"` |  |
| harbor.persistence.enabled | bool | `true` |  |
| harbor.persistence.imageChartStorage.disableredirect | bool | `true` |  |
| harbor.persistence.imageChartStorage.s3.bucket | string | `"harbor-bucket"` |  |
| harbor.persistence.imageChartStorage.s3.existingSecret | string | `"harbor-s3-secret"` |  |
| harbor.persistence.imageChartStorage.s3.region | string | `"us-west-1"` |  |
| harbor.persistence.imageChartStorage.s3.regionendpoint | string | `"http://minio.harbor.svc.cluster.local"` |  |
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
| harbor.trivy.enabled | bool | `true` |  |
| harbor.trivy.gitHubToken | string | `""` |  |
| minio-harbor.minio-tenant.tenant.buckets[0].name | string | `"harbor-bucket"` |  |
| minio-harbor.minio-tenant.tenant.buckets[0].objectLock | bool | `false` |  |
| minio-harbor.minio-tenant.tenant.buckets[0].region | string | `"us-east-1"` |  |
| minio-harbor.minio-tenant.tenant.name | string | `"harbor-minio"` |  |
| minio-harbor.minio-tenant.tenant.pools.size | string | `"10Gi"` |  |

