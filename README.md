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
| gitea.ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTPS"` |  |
| gitea.ingress.annotations."nginx.ingress.kubernetes.io/force-ssl-redirect" | string | `"true"` |  |
| gitea.ingress.className | string | `"nginx"` |  |
| gitea.ingress.enabled | bool | `true` |  |
| gitea.ingress.hosts[0].host | string | `nil` |  |
| gitea.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| gitea.ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| gitea.ingress.tls[0].secretName | string | `"gitea-tls"` |  |

