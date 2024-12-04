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
| gitlab-runner.gitlabUrl | string | `"http://gitlab-webservice-default.gitlab-instance.svc.cluster.local:8181"` |  |
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
| gitlab-runner.runners.config | string | `"[[runners]]\n  [runners.kubernetes]\n    namespace = \"{{.Release.Namespace}}\"\n    image = \"alpine\"\n    privileged = false\n    test\n"` |  |
| gitlab-runner.secrets[0].items[0].key | string | `"runner-registration-token"` |  |
| gitlab-runner.secrets[0].items[0].path | string | `"runner-registration-token"` |  |
| gitlab-runner.secrets[0].name | string | `"gitlab-gitlab-runner-secret"` |  |
| gitlab.certIssuerEmail | string | `"mail@mail.com"` |  |
| gitlab.domain | string | `"domain.com"` |  |
| gitlab.ingressClassName | string | `nil` |  |
| gitlab.version | string | `nil` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |

