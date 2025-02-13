# gitea

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.22.3](https://img.shields.io/badge/AppVersion-1.22.3-informational?style=flat-square)

Gitea Helm chart configured by Ujstor

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://dl.gitea.com/charts/ | gitea | 10.6.0 |
| oci://harbor.k3s0.ujstor.com/helm | secret-store | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| gitea.gitea.admin.existingSecret | string | `"gitea-admin-secret"` |  |
| gitea.gitea.config.service.DISABLE_REGISTRATION | bool | `true` |  |
| gitea.gitea.config.service.REGISTER_MANUAL_CONFIRM | bool | `false` |  |
| gitea.gitea.config.service.REQUIRE_SIGNIN_VIEW | bool | `true` |  |
| gitea.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/force-ssl-redirect" | string | `"true"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/proxy-body-size" | string | `"2048m"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/proxy-read-timeout" | string | `"1200"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/proxy-send-timeout" | string | `"1200"` |  |
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

