# harbor

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.12.0](https://img.shields.io/badge/AppVersion-2.12.0-informational?style=flat-square)

Harbor Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://helm.goharbor.io | harbor | 1.16.0 |
| oci://harbor.k3s0.ujstor.com/helm | minio-tenant | 1.1.0 |

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
| harbor.persistence.imageChartStorage.s3.encrypt | bool | `false` |  |
| harbor.persistence.imageChartStorage.s3.existingSecret | string | `"harbor-s3-secret"` |  |
| harbor.persistence.imageChartStorage.s3.multipartcopychunksize | string | `"33554432"` |  |
| harbor.persistence.imageChartStorage.s3.multipartcopymaxconcurrency | int | `50` |  |
| harbor.persistence.imageChartStorage.s3.region | string | `"us-east-1"` |  |
| harbor.persistence.imageChartStorage.s3.regionendpoint | string | `"https://minio-harbor-hl.harbor.svc.cluster.local:9000"` |  |
| harbor.persistence.imageChartStorage.s3.rootdirectory | string | `"/registry"` |  |
| harbor.persistence.imageChartStorage.s3.secure | bool | `true` |  |
| harbor.persistence.imageChartStorage.s3.skipverify | bool | `true` |  |
| harbor.persistence.imageChartStorage.s3.storageclass | string | `"STANDARD"` |  |
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
| minio-tenant.minio-tenant.tenant.pools[0].size | string | `"50Gi"` |  |
| minio-tenant.minio-tenant.tenant.pools[0].volumesPerServer | int | `1` |  |

