# gitlab

![Version: 1.1.0](https://img.shields.io/badge/Version-1.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 17.8.1](https://img.shields.io/badge/AppVersion-17.8.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.gitlab.io | gitlab-runner-1(gitlab-runner) | 0.73.3 |
| https://charts.gitlab.io | gitlab-runner-2(gitlab-runner) | 0.73.3 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| gitlab-runner-1.concurrent | int | `10` |  |
| gitlab-runner-1.gitlabUrl | string | `"http://gitlab-webservice-default.gitlab.svc.cluster.local:8181"` |  |
| gitlab-runner-1.rbac.create | bool | `true` |  |
| gitlab-runner-1.rbac.rules[0].apiGroups[0] | string | `""` |  |
| gitlab-runner-1.rbac.rules[0].resources[0] | string | `"pods"` |  |
| gitlab-runner-1.rbac.rules[0].resources[1] | string | `"pods/exec"` |  |
| gitlab-runner-1.rbac.rules[0].resources[2] | string | `"pods/attach"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[0] | string | `"get"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[1] | string | `"list"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[2] | string | `"watch"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[3] | string | `"create"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[4] | string | `"patch"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[5] | string | `"update"` |  |
| gitlab-runner-1.rbac.rules[0].verbs[6] | string | `"delete"` |  |
| gitlab-runner-1.rbac.rules[1].apiGroups[0] | string | `""` |  |
| gitlab-runner-1.rbac.rules[1].resources[0] | string | `"secrets"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[0] | string | `"get"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[1] | string | `"list"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[2] | string | `"watch"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[3] | string | `"create"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[4] | string | `"patch"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[5] | string | `"update"` |  |
| gitlab-runner-1.rbac.rules[1].verbs[6] | string | `"delete"` |  |
| gitlab-runner-1.rbac.rules[2].apiGroups[0] | string | `""` |  |
| gitlab-runner-1.rbac.rules[2].resources[0] | string | `"configmaps"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[0] | string | `"get"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[1] | string | `"list"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[2] | string | `"watch"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[3] | string | `"create"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[4] | string | `"patch"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[5] | string | `"update"` |  |
| gitlab-runner-1.rbac.rules[2].verbs[6] | string | `"delete"` |  |
| gitlab-runner-1.rbac.rules[3].apiGroups[0] | string | `""` |  |
| gitlab-runner-1.rbac.rules[3].resources[0] | string | `"services"` |  |
| gitlab-runner-1.rbac.rules[3].verbs[0] | string | `"get"` |  |
| gitlab-runner-1.rbac.rules[3].verbs[1] | string | `"list"` |  |
| gitlab-runner-1.rbac.rules[3].verbs[2] | string | `"watch"` |  |
| gitlab-runner-1.rbac.rules[4].apiGroups[0] | string | `""` |  |
| gitlab-runner-1.rbac.rules[4].resources[0] | string | `"serviceaccounts"` |  |
| gitlab-runner-1.rbac.rules[4].verbs[0] | string | `"get"` |  |
| gitlab-runner-1.rbac.rules[4].verbs[1] | string | `"list"` |  |
| gitlab-runner-1.rbac.rules[4].verbs[2] | string | `"watch"` |  |
| gitlab-runner-1.runners.config | string | `"[[runners]]\n  [runners.kubernetes]\n    namespace = \"{{.Release.Namespace}}\"\n    image = \"alpine\"\n    privileged = true\n    service_account = \"gitlab-gitlab-runner\"\n    service_account_overwrite_allowed = \"*\"\n    image_pull_secrets = [\"harbor-admin-secret\"]\n    [[runners.kubernetes.volumes.host_path]]\n      name = \"buildah-storage\"\n      mount_path = \"/var/lib/containers\"\n      read_only = false\n    [[runners.kubernetes.volumes.host_path]]\n      name = \"tmp-data\"\n      mount_path = \"/tmp\"\n      read_only = false\n    [runners.kubernetes.resource_limits]\n      memory = \"4Gi\"\n      cpu = \"2\"\n"` |  |
| gitlab-runner-1.secrets[0].items[0].key | string | `"runner-registration-token"` |  |
| gitlab-runner-1.secrets[0].items[0].path | string | `"runner-registration-token"` |  |
| gitlab-runner-1.secrets[0].name | string | `"gitlab-gitlab-runner-secret"` |  |
| gitlab-runner-2.concurrent | int | `10` |  |
| gitlab-runner-2.gitlabUrl | string | `"http://gitlab-webservice-default.gitlab.svc.cluster.local:8181"` |  |
| gitlab-runner-2.rbac.create | bool | `true` |  |
| gitlab-runner-2.rbac.rules[0].apiGroups[0] | string | `""` |  |
| gitlab-runner-2.rbac.rules[0].resources[0] | string | `"pods"` |  |
| gitlab-runner-2.rbac.rules[0].resources[1] | string | `"pods/exec"` |  |
| gitlab-runner-2.rbac.rules[0].resources[2] | string | `"pods/attach"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[0] | string | `"get"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[1] | string | `"list"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[2] | string | `"watch"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[3] | string | `"create"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[4] | string | `"patch"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[5] | string | `"update"` |  |
| gitlab-runner-2.rbac.rules[0].verbs[6] | string | `"delete"` |  |
| gitlab-runner-2.rbac.rules[1].apiGroups[0] | string | `""` |  |
| gitlab-runner-2.rbac.rules[1].resources[0] | string | `"secrets"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[0] | string | `"get"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[1] | string | `"list"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[2] | string | `"watch"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[3] | string | `"create"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[4] | string | `"patch"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[5] | string | `"update"` |  |
| gitlab-runner-2.rbac.rules[1].verbs[6] | string | `"delete"` |  |
| gitlab-runner-2.rbac.rules[2].apiGroups[0] | string | `""` |  |
| gitlab-runner-2.rbac.rules[2].resources[0] | string | `"configmaps"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[0] | string | `"get"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[1] | string | `"list"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[2] | string | `"watch"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[3] | string | `"create"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[4] | string | `"patch"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[5] | string | `"update"` |  |
| gitlab-runner-2.rbac.rules[2].verbs[6] | string | `"delete"` |  |
| gitlab-runner-2.rbac.rules[3].apiGroups[0] | string | `""` |  |
| gitlab-runner-2.rbac.rules[3].resources[0] | string | `"services"` |  |
| gitlab-runner-2.rbac.rules[3].verbs[0] | string | `"get"` |  |
| gitlab-runner-2.rbac.rules[3].verbs[1] | string | `"list"` |  |
| gitlab-runner-2.rbac.rules[3].verbs[2] | string | `"watch"` |  |
| gitlab-runner-2.rbac.rules[4].apiGroups[0] | string | `""` |  |
| gitlab-runner-2.rbac.rules[4].resources[0] | string | `"serviceaccounts"` |  |
| gitlab-runner-2.rbac.rules[4].verbs[0] | string | `"get"` |  |
| gitlab-runner-2.rbac.rules[4].verbs[1] | string | `"list"` |  |
| gitlab-runner-2.rbac.rules[4].verbs[2] | string | `"watch"` |  |
| gitlab-runner-2.runners.config | string | `"[[runners]]\n  [runners.kubernetes]\n    namespace = \"{{.Release.Namespace}}\"\n    image = \"alpine\"\n    privileged = true\n    service_account = \"gitlab-gitlab-runner\"\n    service_account_overwrite_allowed = \"*\"\n    image_pull_secrets = [\"harbor-admin-secret\"]\n    [[runners.kubernetes.volumes.host_path]]\n      name = \"buildah-storage\"\n      mount_path = \"/var/lib/containers\"\n      read_only = false\n    [[runners.kubernetes.volumes.host_path]]\n      name = \"tmp-data\"\n      mount_path = \"/tmp\"\n      read_only = false\n    [runners.kubernetes.resource_limits]\n      memory = \"4Gi\"\n      cpu = \"2\"\n"` |  |
| gitlab-runner-2.secrets[0].items[0].key | string | `"runner-registration-token"` |  |
| gitlab-runner-2.secrets[0].items[0].path | string | `"runner-registration-token"` |  |
| gitlab-runner-2.secrets[0].name | string | `"gitlab-gitlab-runner-secret"` |  |
| gitlab.certIssuerEmail | string | `"mail@mail.com"` |  |
| gitlab.domain | string | `"domain.com"` |  |
| gitlab.email.display_name | string | `"GitLab"` |  |
| gitlab.email.from | string | `"gitlab@example.com"` |  |
| gitlab.email.reply_to | string | `"noreply@example.com"` |  |
| gitlab.ingressClassName | string | `nil` |  |
| gitlab.smtp.address | string | `"smtp.example.com"` |  |
| gitlab.smtp.authentication | string | `"plain"` |  |
| gitlab.smtp.enabled | bool | `true` |  |
| gitlab.smtp.password.key | string | `"password"` |  |
| gitlab.smtp.password.secret | string | `"smtp-password"` |  |
| gitlab.smtp.port | int | `587` |  |
| gitlab.smtp.starttls_auto | bool | `true` |  |
| gitlab.smtp.tls | bool | `false` |  |
| gitlab.smtp.user_name | string | `"example"` |  |
| gitlab.version | string | `"8.8.1"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |

