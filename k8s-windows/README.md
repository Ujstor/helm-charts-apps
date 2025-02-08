# k8s-windows

![Version: 1.0.1](https://img.shields.io/badge/Version-1.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 4.0.7](https://img.shields.io/badge/AppVersion-4.0.7-informational?style=flat-square)

Run windows on Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://ujstor.github.io/helm-charts-system | secret-store | 1.0.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"harbor.k3s0.ujstor.com/docker/k8s-windows"` |  |
| image.tag | string | `"0.0.1"` |  |
| imagePullSecrets[0].name | string | `"regcred"` |  |
| ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/auth-realm" | string | `"Authentication Required"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/auth-secret" | string | `"win-basic-auth-secret"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/auth-type" | string | `"basic"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/backend-protocol" | string | `"HTTP"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/force-ssl-redirect" | string | `"false"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/ssl-redirect" | string | `"false"` |  |
| ingress.className | string | `"nginx"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"win.test.com"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls[0].hosts[0] | string | `"win.test.com"` |  |
| ingress.tls[0].secretName | string | `"win-tls"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.privileged | bool | `true` |  |
| replicaCount | int | `1` |  |
| resources[0].name | string | `"VERSION"` |  |
| resources[0].value | string | `"10"` |  |
| resources[1].name | string | `"RAM_SIZE"` |  |
| resources[1].value | string | `"8G"` |  |
| resources[2].name | string | `"CPU_CORES"` |  |
| resources[2].value | string | `"12"` |  |
| resources[3].name | string | `"DISK_SIZE"` |  |
| resources[3].value | string | `"120G"` |  |
| secret-store.secretStore.clusterWide | bool | `false` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.create | bool | `true` |  |
| secret-store.secretStore.provider.kubernetes.auth.serviceAccount.name | string | `"win-secret-store-sa"` |  |
| secret-store.secretStore.provider.type | string | `"kubernetes"` |  |
| securityContext.capabilities.add[0] | string | `"NET_ADMIN"` |  |
| securityContext.capabilities.add[1] | string | `"SYS_ADMIN"` |  |
| securityContext.fsGroup | int | `0` |  |
| securityContext.privileged | bool | `true` |  |
| securityContext.runAsUser | int | `0` |  |
| service.ports[0].name | string | `"http"` |  |
| service.ports[0].port | int | `80` |  |
| service.ports[0].protocol | string | `"TCP"` |  |
| service.ports[0].targetPort | int | `8006` |  |
| service.ports[1].name | string | `"tcp-3389"` |  |
| service.ports[1].port | int | `3389` |  |
| service.ports[1].protocol | string | `"TCP"` |  |
| service.ports[1].targetPort | int | `3389` |  |
| service.ports[2].name | string | `"udp-3389"` |  |
| service.ports[2].port | int | `3389` |  |
| service.ports[2].protocol | string | `"UDP"` |  |
| service.ports[2].targetPort | int | `3389` |  |
| service.type | string | `"ClusterIP"` |  |
| terminationGracePeriodSeconds | int | `120` |  |
| volumeMounts[0].mountPath | string | `"/storage"` |  |
| volumeMounts[0].name | string | `"storage"` |  |
| volumeMounts[1].mountPath | string | `"/dev/kvm"` |  |
| volumeMounts[1].name | string | `"dev-kvm"` |  |
| volumeMounts[2].mountPath | string | `"/dev/net/tun"` |  |
| volumeMounts[2].name | string | `"dev-tun"` |  |
| volumeMounts[2].type | string | `"CharDevice"` |  |
| volumes[0].name | string | `"storage"` |  |
| volumes[0].persistentVolumeClaim.claimName | string | `"windows-pvc"` |  |
| volumes[1].hostPath.path | string | `"/dev/kvm"` |  |
| volumes[1].name | string | `"dev-kvm"` |  |
| volumes[2].hostPath.path | string | `"/dev/net/tun"` |  |
| volumes[2].hostPath.type | string | `"CharDevice"` |  |
| volumes[2].name | string | `"dev-tun"` |  |

