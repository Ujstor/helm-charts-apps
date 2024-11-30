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

