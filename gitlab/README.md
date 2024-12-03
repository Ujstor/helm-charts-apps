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
| gitlab-runner.gitlabUrl | string | `nil` |  |
| gitlab-runner.runners.config | string | `"[[runners]]\n  [runners.kubernetes]\n    namespace = \"{{.Release.Namespace}}\"\n    image = \"alpine\"\n"` |  |
| gitlab-runner.secrets | list | `[]` |  |
| gitlab.certIssuerEmail | string | `"astipan@gmail.com"` |  |
| gitlab.domain | string | `"k3s.ujstor.com"` |  |
| gitlab.ingressClassName | string | `nil` |  |
| gitlab.version | string | `nil` |  |
| serviceAccount | bool | `true` |  |

