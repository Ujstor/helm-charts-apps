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

# common

![Version: 2.8.0](https://img.shields.io/badge/Version-2.8.0-informational?style=flat-square) ![Type: library](https://img.shields.io/badge/Type-library-informational?style=flat-square) ![AppVersion: 2.8.0](https://img.shields.io/badge/AppVersion-2.8.0-informational?style=flat-square)

A Library Helm Chart for grouping common logic between bitnami charts. This chart is not deployable by itself.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| exampleValue | string | `"common-chart"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# common

![Version: 2.8.0](https://img.shields.io/badge/Version-2.8.0-informational?style=flat-square) ![Type: library](https://img.shields.io/badge/Type-library-informational?style=flat-square) ![AppVersion: 2.8.0](https://img.shields.io/badge/AppVersion-2.8.0-informational?style=flat-square)

A Library Helm Chart for grouping common logic between bitnami charts. This chart is not deployable by itself.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| exampleValue | string | `"common-chart"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# zookeeper

![Version: 11.4.11](https://img.shields.io/badge/Version-11.4.11-informational?style=flat-square) ![AppVersion: 3.8.2](https://img.shields.io/badge/AppVersion-3.8.2-informational?style=flat-square)

Apache ZooKeeper provides a reliable, centralized register of configuration data and services for distributed applications.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts/tree/main/bitnami/zookeeper>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| oci://registry-1.docker.io/bitnamicharts | common | 2.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args | list | `[]` |  |
| auth.client.clientPassword | string | `""` |  |
| auth.client.clientUser | string | `""` |  |
| auth.client.enabled | bool | `false` |  |
| auth.client.existingSecret | string | `""` |  |
| auth.client.serverPasswords | string | `""` |  |
| auth.client.serverUsers | string | `""` |  |
| auth.quorum.enabled | bool | `false` |  |
| auth.quorum.existingSecret | string | `""` |  |
| auth.quorum.learnerPassword | string | `""` |  |
| auth.quorum.learnerUser | string | `""` |  |
| auth.quorum.serverPasswords | string | `""` |  |
| auth.quorum.serverUsers | string | `""` |  |
| autopurge.purgeInterval | int | `0` |  |
| autopurge.snapRetainCount | int | `3` |  |
| clusterDomain | string | `"cluster.local"` |  |
| command[0] | string | `"/scripts/setup.sh"` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| configuration | string | `""` |  |
| containerPorts.client | int | `2181` |  |
| containerPorts.election | int | `3888` |  |
| containerPorts.follower | int | `2888` |  |
| containerPorts.tls | int | `3181` |  |
| containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| containerSecurityContext.enabled | bool | `true` |  |
| containerSecurityContext.runAsNonRoot | bool | `true` |  |
| containerSecurityContext.runAsUser | int | `1001` |  |
| customLivenessProbe | object | `{}` |  |
| customReadinessProbe | object | `{}` |  |
| customStartupProbe | object | `{}` |  |
| dataLogDir | string | `""` |  |
| diagnosticMode.args[0] | string | `"infinity"` |  |
| diagnosticMode.command[0] | string | `"sleep"` |  |
| diagnosticMode.enabled | bool | `false` |  |
| existingConfigmap | string | `""` |  |
| extraDeploy | list | `[]` |  |
| extraEnvVars | list | `[]` |  |
| extraEnvVarsCM | string | `""` |  |
| extraEnvVarsSecret | string | `""` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fourlwCommandsWhitelist | string | `"srvr, mntr, ruok"` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.storageClass | string | `""` |  |
| heapSize | int | `1024` |  |
| hostAliases | list | `[]` |  |
| image.debug | bool | `false` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"bitnami/zookeeper"` |  |
| image.tag | string | `"3.8.2-debian-11-r27"` |  |
| initContainers | list | `[]` |  |
| initLimit | int | `10` |  |
| jvmFlags | string | `""` |  |
| kubeVersion | string | `""` |  |
| lifecycleHooks | object | `{}` |  |
| listenOnAllIPs | bool | `false` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.probeCommandTimeout | int | `2` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| logLevel | string | `"ERROR"` |  |
| maxClientCnxns | int | `60` |  |
| maxSessionTimeout | int | `40000` |  |
| metrics.containerPort | int | `9141` |  |
| metrics.enabled | bool | `false` |  |
| metrics.prometheusRule.additionalLabels | object | `{}` |  |
| metrics.prometheusRule.enabled | bool | `false` |  |
| metrics.prometheusRule.namespace | string | `""` |  |
| metrics.prometheusRule.rules | list | `[]` |  |
| metrics.service.annotations."prometheus.io/path" | string | `"/metrics"` |  |
| metrics.service.annotations."prometheus.io/port" | string | `"{{ .Values.metrics.service.port }}"` |  |
| metrics.service.annotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.service.port | int | `9141` |  |
| metrics.service.type | string | `"ClusterIP"` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `""` |  |
| metrics.serviceMonitor.jobLabel | string | `""` |  |
| metrics.serviceMonitor.metricRelabelings | list | `[]` |  |
| metrics.serviceMonitor.namespace | string | `""` |  |
| metrics.serviceMonitor.relabelings | list | `[]` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `""` |  |
| metrics.serviceMonitor.selector | object | `{}` |  |
| minServerId | int | `1` |  |
| nameOverride | string | `""` |  |
| namespaceOverride | string | `""` |  |
| networkPolicy.allowExternal | bool | `true` |  |
| networkPolicy.enabled | bool | `false` |  |
| nodeAffinityPreset.key | string | `""` |  |
| nodeAffinityPreset.type | string | `""` |  |
| nodeAffinityPreset.values | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| pdb.create | bool | `false` |  |
| pdb.maxUnavailable | int | `1` |  |
| pdb.minAvailable | string | `""` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.dataLogDir.existingClaim | string | `""` |  |
| persistence.dataLogDir.selector | object | `{}` |  |
| persistence.dataLogDir.size | string | `"8Gi"` |  |
| persistence.enabled | bool | `true` |  |
| persistence.existingClaim | string | `""` |  |
| persistence.labels | object | `{}` |  |
| persistence.selector | object | `{}` |  |
| persistence.size | string | `"8Gi"` |  |
| persistence.storageClass | string | `""` |  |
| podAffinityPreset | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podAntiAffinityPreset | string | `"soft"` |  |
| podLabels | object | `{}` |  |
| podManagementPolicy | string | `"Parallel"` |  |
| podSecurityContext.enabled | bool | `true` |  |
| podSecurityContext.fsGroup | int | `1001` |  |
| preAllocSize | int | `65536` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `6` |  |
| readinessProbe.initialDelaySeconds | int | `5` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.probeCommandTimeout | int | `2` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `5` |  |
| replicaCount | int | `1` |  |
| resources.limits | object | `{}` |  |
| resources.requests.cpu | string | `"250m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| schedulerName | string | `""` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `""` |  |
| service.disableBaseClientPort | bool | `false` |  |
| service.externalTrafficPolicy | string | `"Cluster"` |  |
| service.extraPorts | list | `[]` |  |
| service.headless.annotations | object | `{}` |  |
| service.headless.publishNotReadyAddresses | bool | `true` |  |
| service.headless.servicenameOverride | string | `""` |  |
| service.loadBalancerIP | string | `""` |  |
| service.loadBalancerSourceRanges | list | `[]` |  |
| service.nodePorts.client | string | `""` |  |
| service.nodePorts.tls | string | `""` |  |
| service.ports.client | int | `2181` |  |
| service.ports.election | int | `3888` |  |
| service.ports.follower | int | `2888` |  |
| service.ports.tls | int | `3181` |  |
| service.sessionAffinity | string | `"None"` |  |
| service.sessionAffinityConfig | object | `{}` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| sidecars | list | `[]` |  |
| snapCount | int | `100000` |  |
| startupProbe.enabled | bool | `false` |  |
| startupProbe.failureThreshold | int | `15` |  |
| startupProbe.initialDelaySeconds | int | `30` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| syncLimit | int | `5` |  |
| tickTime | int | `2000` |  |
| tls.client.auth | string | `"none"` |  |
| tls.client.autoGenerated | bool | `false` |  |
| tls.client.enabled | bool | `false` |  |
| tls.client.existingSecret | string | `""` |  |
| tls.client.existingSecretKeystoreKey | string | `""` |  |
| tls.client.existingSecretTruststoreKey | string | `""` |  |
| tls.client.keystorePassword | string | `""` |  |
| tls.client.keystorePath | string | `"/opt/bitnami/zookeeper/config/certs/client/zookeeper.keystore.jks"` |  |
| tls.client.passwordsSecretKeystoreKey | string | `""` |  |
| tls.client.passwordsSecretName | string | `""` |  |
| tls.client.passwordsSecretTruststoreKey | string | `""` |  |
| tls.client.truststorePassword | string | `""` |  |
| tls.client.truststorePath | string | `"/opt/bitnami/zookeeper/config/certs/client/zookeeper.truststore.jks"` |  |
| tls.quorum.auth | string | `"none"` |  |
| tls.quorum.autoGenerated | bool | `false` |  |
| tls.quorum.enabled | bool | `false` |  |
| tls.quorum.existingSecret | string | `""` |  |
| tls.quorum.existingSecretKeystoreKey | string | `""` |  |
| tls.quorum.existingSecretTruststoreKey | string | `""` |  |
| tls.quorum.keystorePassword | string | `""` |  |
| tls.quorum.keystorePath | string | `"/opt/bitnami/zookeeper/config/certs/quorum/zookeeper.keystore.jks"` |  |
| tls.quorum.passwordsSecretKeystoreKey | string | `""` |  |
| tls.quorum.passwordsSecretName | string | `""` |  |
| tls.quorum.passwordsSecretTruststoreKey | string | `""` |  |
| tls.quorum.truststorePassword | string | `""` |  |
| tls.quorum.truststorePath | string | `"/opt/bitnami/zookeeper/config/certs/quorum/zookeeper.truststore.jks"` |  |
| tls.resources.limits | object | `{}` |  |
| tls.resources.requests | object | `{}` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |
| updateStrategy.rollingUpdate | object | `{}` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |
| volumePermissions.containerSecurityContext.enabled | bool | `true` |  |
| volumePermissions.containerSecurityContext.runAsUser | int | `0` |  |
| volumePermissions.enabled | bool | `false` |  |
| volumePermissions.image.digest | string | `""` |  |
| volumePermissions.image.pullPolicy | string | `"IfNotPresent"` |  |
| volumePermissions.image.pullSecrets | list | `[]` |  |
| volumePermissions.image.registry | string | `"docker.io"` |  |
| volumePermissions.image.repository | string | `"bitnami/os-shell"` |  |
| volumePermissions.image.tag | string | `"11-debian-11-r40"` |  |
| volumePermissions.resources.limits | object | `{}` |  |
| volumePermissions.resources.requests | object | `{}` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# clickhouse

![Version: 3.6.7](https://img.shields.io/badge/Version-3.6.7-informational?style=flat-square) ![AppVersion: 23.7.4](https://img.shields.io/badge/AppVersion-23.7.4-informational?style=flat-square)

ClickHouse is an open-source column-oriented OLAP database management system. Use it to boost your database performance while providing linear scalability and hardware efficiency.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts/tree/main/bitnami/clickhouse>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| oci://registry-1.docker.io/bitnamicharts | common | 2.x.x |
| oci://registry-1.docker.io/bitnamicharts | zookeeper | 11.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args | list | `[]` |  |
| auth.existingSecret | string | `""` |  |
| auth.existingSecretKey | string | `""` |  |
| auth.password | string | `""` |  |
| auth.username | string | `"default"` |  |
| clusterDomain | string | `"cluster.local"` |  |
| command[0] | string | `"/scripts/setup.sh"` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| containerPorts.http | int | `8123` |  |
| containerPorts.https | int | `8443` |  |
| containerPorts.interserver | int | `9009` |  |
| containerPorts.keeper | int | `2181` |  |
| containerPorts.keeperInter | int | `9444` |  |
| containerPorts.keeperSecure | int | `3181` |  |
| containerPorts.metrics | int | `8001` |  |
| containerPorts.mysql | int | `9004` |  |
| containerPorts.postgresql | int | `9005` |  |
| containerPorts.tcp | int | `9000` |  |
| containerPorts.tcpSecure | int | `9440` |  |
| containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| containerSecurityContext.enabled | bool | `true` |  |
| containerSecurityContext.runAsNonRoot | bool | `true` |  |
| containerSecurityContext.runAsUser | int | `1001` |  |
| customLivenessProbe | object | `{}` |  |
| customReadinessProbe | object | `{}` |  |
| customStartupProbe | object | `{}` |  |
| defaultConfigurationOverrides | string | `"<clickhouse>\n  <!-- Macros -->\n  <macros>\n    <shard from_env=\"CLICKHOUSE_SHARD_ID\"></shard>\n    <replica from_env=\"CLICKHOUSE_REPLICA_ID\"></replica>\n    <layer>{{ include \"common.names.fullname\" . }}</layer>\n  </macros>\n  <!-- Log Level -->\n  <logger>\n    <level>{{ .Values.logLevel }}</level>\n  </logger>\n  {{- if or (ne (int .Values.shards) 1) (ne (int .Values.replicaCount) 1)}}\n  <!-- Cluster configuration - Any update of the shards and replicas requires helm upgrade -->\n  <remote_servers>\n    <default>\n      {{- $shards := $.Values.shards | int }}\n      {{- range $shard, $e := until $shards }}\n      <shard>\n          {{- $replicas := $.Values.replicaCount | int }}\n          {{- range $i, $_e := until $replicas }}\n          <replica>\n              <host>{{ printf \"%s-shard%d-%d.%s.%s.svc.%s\" (include \"common.names.fullname\" $ ) $shard $i (include \"clickhouse.headlessServiceName\" $) (include \"common.names.namespace\" $) $.Values.clusterDomain }}</host>\n              <port>{{ $.Values.service.ports.tcp }}</port>\n          </replica>\n          {{- end }}\n      </shard>\n      {{- end }}\n    </default>\n  </remote_servers>\n  {{- end }}\n  {{- if .Values.keeper.enabled }}\n  <!-- keeper configuration -->\n  <keeper_server>\n    {{/*ClickHouse keeper configuration using the helm chart */}}\n    <tcp_port>{{ $.Values.containerPorts.keeper }}</tcp_port>\n    {{- if .Values.tls.enabled }}\n    <tcp_port_secure>{{ $.Values.containerPorts.keeperSecure }}</tcp_port_secure>\n    {{- end }}\n    <server_id from_env=\"KEEPER_SERVER_ID\"></server_id>\n    <log_storage_path>/bitnami/clickhouse/keeper/coordination/log</log_storage_path>\n    <snapshot_storage_path>/bitnami/clickhouse/keeper/coordination/snapshots</snapshot_storage_path>\n\n    <coordination_settings>\n        <operation_timeout_ms>10000</operation_timeout_ms>\n        <session_timeout_ms>30000</session_timeout_ms>\n        <raft_logs_level>trace</raft_logs_level>\n    </coordination_settings>\n\n    <raft_configuration>\n    {{- $nodes := .Values.replicaCount | int }}\n    {{- range $node, $e := until $nodes }}\n    <server>\n      <id>{{ $node | int }}</id>\n      <hostname from_env=\"{{ printf \"KEEPER_NODE_%d\" $node }}\"></hostname>\n      <port>{{ $.Values.service.ports.keeperInter }}</port>\n    </server>\n    {{- end }}\n    </raft_configuration>\n  </keeper_server>\n  {{- end }}\n  {{- if or .Values.keeper.enabled .Values.zookeeper.enabled .Values.externalZookeeper.servers }}\n  <!-- Zookeeper configuration -->\n  <zookeeper>\n    {{- if or .Values.keeper.enabled }}\n    {{- $nodes := .Values.replicaCount | int }}\n    {{- range $node, $e := until $nodes }}\n    <node>\n      <host from_env=\"{{ printf \"KEEPER_NODE_%d\" $node }}\"></host>\n      <port>{{ $.Values.service.ports.keeper }}</port>\n    </node>\n    {{- end }}\n    {{- else if .Values.zookeeper.enabled }}\n    {{/* Zookeeper configuration using the helm chart */}}\n    {{- $nodes := .Values.zookeeper.replicaCount | int }}\n    {{- range $node, $e := until $nodes }}\n    <node>\n      <host from_env=\"{{ printf \"KEEPER_NODE_%d\" $node }}\"></host>\n      <port>{{ $.Values.zookeeper.service.ports.client }}</port>\n    </node>\n    {{- end }}\n    {{- else if .Values.externalZookeeper.servers }}\n    {{/* Zookeeper configuration using an external instance */}}\n    {{- range $node :=.Values.externalZookeeper.servers }}\n    <node>\n      <host>{{ $node }}</host>\n      <port>{{ $.Values.externalZookeeper.port }}</port>\n    </node>\n    {{- end }}\n    {{- end }}\n  </zookeeper>\n  {{- end }}\n  {{- if .Values.tls.enabled }}\n  <!-- TLS configuration -->\n  <tcp_port_secure from_env=\"CLICKHOUSE_TCP_SECURE_PORT\"></tcp_port_secure>\n  <https_port from_env=\"CLICKHOUSE_HTTPS_PORT\"></https_port>\n  <openSSL>\n      <server>\n          {{- $certFileName := default \"tls.crt\" .Values.tls.certFilename }}\n          {{- $keyFileName := default \"tls.key\" .Values.tls.certKeyFilename }}\n          <certificateFile>/bitnami/clickhouse/certs/{{$certFileName}}</certificateFile>\n          <privateKeyFile>/bitnami/clickhouse/certs/{{$keyFileName}}</privateKeyFile>\n          <verificationMode>none</verificationMode>\n          <cacheSessions>true</cacheSessions>\n          <disableProtocols>sslv2,sslv3</disableProtocols>\n          <preferServerCiphers>true</preferServerCiphers>\n          {{- if or .Values.tls.autoGenerated .Values.tls.certCAFilename }}\n          {{- $caFileName := default \"ca.crt\" .Values.tls.certCAFilename }}\n          <caConfig>/bitnami/clickhouse/certs/{{$caFileName}}</caConfig>\n          {{- else }}\n          <loadDefaultCAFile>true</loadDefaultCAFile>\n          {{- end }}\n      </server>\n      <client>\n          <loadDefaultCAFile>true</loadDefaultCAFile>\n          <cacheSessions>true</cacheSessions>\n          <disableProtocols>sslv2,sslv3</disableProtocols>\n          <preferServerCiphers>true</preferServerCiphers>\n          <verificationMode>none</verificationMode>\n          <invalidCertificateHandler>\n              <name>AcceptCertificateHandler</name>\n          </invalidCertificateHandler>\n      </client>\n  </openSSL>\n  {{- end }}\n  {{- if .Values.metrics.enabled }}\n   <!-- Prometheus metrics -->\n   <prometheus>\n      <endpoint>/metrics</endpoint>\n      <port from_env=\"CLICKHOUSE_METRICS_PORT\"></port>\n      <metrics>true</metrics>\n      <events>true</events>\n      <asynchronous_metrics>true</asynchronous_metrics>\n  </prometheus>\n  {{- end }}\n</clickhouse>\n"` |  |
| diagnosticMode.args[0] | string | `"infinity"` |  |
| diagnosticMode.command[0] | string | `"sleep"` |  |
| diagnosticMode.enabled | bool | `false` |  |
| existingOverridesConfigmap | string | `""` |  |
| externalAccess.enabled | bool | `false` |  |
| externalAccess.service.annotations | object | `{}` |  |
| externalAccess.service.extraPorts | list | `[]` |  |
| externalAccess.service.labels | object | `{}` |  |
| externalAccess.service.loadBalancerAnnotations | list | `[]` |  |
| externalAccess.service.loadBalancerIPs | list | `[]` |  |
| externalAccess.service.loadBalancerSourceRanges | list | `[]` |  |
| externalAccess.service.nodePorts.http | list | `[]` |  |
| externalAccess.service.nodePorts.https | list | `[]` |  |
| externalAccess.service.nodePorts.interserver | list | `[]` |  |
| externalAccess.service.nodePorts.keeper | list | `[]` |  |
| externalAccess.service.nodePorts.keeperInter | list | `[]` |  |
| externalAccess.service.nodePorts.keeperSecure | list | `[]` |  |
| externalAccess.service.nodePorts.metrics | list | `[]` |  |
| externalAccess.service.nodePorts.mysql | list | `[]` |  |
| externalAccess.service.nodePorts.postgresql | list | `[]` |  |
| externalAccess.service.nodePorts.tcp | list | `[]` |  |
| externalAccess.service.nodePorts.tcpSecure | list | `[]` |  |
| externalAccess.service.ports.http | int | `80` |  |
| externalAccess.service.ports.https | int | `443` |  |
| externalAccess.service.ports.interserver | int | `9009` |  |
| externalAccess.service.ports.keeper | int | `2181` |  |
| externalAccess.service.ports.keeperInter | int | `9444` |  |
| externalAccess.service.ports.keeperSecure | int | `3181` |  |
| externalAccess.service.ports.metrics | int | `8001` |  |
| externalAccess.service.ports.mysql | int | `9004` |  |
| externalAccess.service.ports.postgresql | int | `9005` |  |
| externalAccess.service.ports.tcp | int | `9000` |  |
| externalAccess.service.ports.tcpSecure | int | `9440` |  |
| externalAccess.service.type | string | `"LoadBalancer"` |  |
| externalZookeeper.port | int | `2888` |  |
| externalZookeeper.servers | list | `[]` |  |
| extraDeploy | list | `[]` |  |
| extraEnvVars | list | `[]` |  |
| extraEnvVarsCM | string | `""` |  |
| extraEnvVarsSecret | string | `""` |  |
| extraOverrides | string | `""` |  |
| extraOverridesConfigmap | string | `""` |  |
| extraOverridesSecret | string | `""` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.storageClass | string | `""` |  |
| hostAliases | list | `[]` |  |
| image.debug | bool | `false` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"bitnami/clickhouse"` |  |
| image.tag | string | `"23.7.4-debian-11-r2"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.apiVersion | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.extraHosts | list | `[]` |  |
| ingress.extraPaths | list | `[]` |  |
| ingress.extraRules | list | `[]` |  |
| ingress.extraTls | list | `[]` |  |
| ingress.hostname | string | `"clickhouse.local"` |  |
| ingress.ingressClassName | string | `""` |  |
| ingress.path | string | `"/"` |  |
| ingress.pathType | string | `"ImplementationSpecific"` |  |
| ingress.secrets | list | `[]` |  |
| ingress.selfSigned | bool | `false` |  |
| ingress.tls | bool | `false` |  |
| initContainers | list | `[]` |  |
| initdbScripts | object | `{}` |  |
| initdbScriptsSecret | string | `""` |  |
| keeper.enabled | bool | `false` |  |
| kubeVersion | string | `""` |  |
| lifecycleHooks | object | `{}` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `10` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| logLevel | string | `"information"` |  |
| metrics.enabled | bool | `false` |  |
| metrics.podAnnotations."prometheus.io/port" | string | `"{{ .Values.containerPorts.metrics }}"` |  |
| metrics.podAnnotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.prometheusRule.additionalLabels | object | `{}` |  |
| metrics.prometheusRule.enabled | bool | `false` |  |
| metrics.prometheusRule.namespace | string | `""` |  |
| metrics.prometheusRule.rules | list | `[]` |  |
| metrics.serviceMonitor.annotations | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `""` |  |
| metrics.serviceMonitor.jobLabel | string | `""` |  |
| metrics.serviceMonitor.labels | object | `{}` |  |
| metrics.serviceMonitor.metricRelabelings | list | `[]` |  |
| metrics.serviceMonitor.namespace | string | `""` |  |
| metrics.serviceMonitor.relabelings | list | `[]` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `""` |  |
| metrics.serviceMonitor.selector | object | `{}` |  |
| nameOverride | string | `""` |  |
| namespaceOverride | string | `""` |  |
| nodeAffinityPreset.key | string | `""` |  |
| nodeAffinityPreset.type | string | `""` |  |
| nodeAffinityPreset.values | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.dataSource | object | `{}` |  |
| persistence.enabled | bool | `true` |  |
| persistence.existingClaim | string | `""` |  |
| persistence.labels | object | `{}` |  |
| persistence.selector | object | `{}` |  |
| persistence.size | string | `"8Gi"` |  |
| persistence.storageClass | string | `""` |  |
| podAffinityPreset | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podAntiAffinityPreset | string | `"soft"` |  |
| podLabels | object | `{}` |  |
| podManagementPolicy | string | `"Parallel"` |  |
| podSecurityContext.enabled | bool | `true` |  |
| podSecurityContext.fsGroup | int | `1001` |  |
| podSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `10` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `3` |  |
| resources.limits | object | `{}` |  |
| resources.requests | object | `{}` |  |
| schedulerName | string | `""` |  |
| service.annotations | object | `{}` |  |
| service.clusterIP | string | `""` |  |
| service.externalTrafficPolicy | string | `"Cluster"` |  |
| service.extraPorts | list | `[]` |  |
| service.headless.annotations | object | `{}` |  |
| service.loadBalancerIP | string | `""` |  |
| service.loadBalancerSourceRanges | list | `[]` |  |
| service.nodePorts.http | string | `""` |  |
| service.nodePorts.https | string | `""` |  |
| service.nodePorts.interserver | string | `""` |  |
| service.nodePorts.keeper | string | `""` |  |
| service.nodePorts.keeperInter | string | `""` |  |
| service.nodePorts.keeperSecure | string | `""` |  |
| service.nodePorts.metrics | string | `""` |  |
| service.nodePorts.mysql | string | `""` |  |
| service.nodePorts.postgresql | string | `""` |  |
| service.nodePorts.tcp | string | `""` |  |
| service.nodePorts.tcpSecure | string | `""` |  |
| service.ports.http | int | `8123` |  |
| service.ports.https | int | `443` |  |
| service.ports.interserver | int | `9009` |  |
| service.ports.keeper | int | `2181` |  |
| service.ports.keeperInter | int | `9444` |  |
| service.ports.keeperSecure | int | `3181` |  |
| service.ports.metrics | int | `8001` |  |
| service.ports.mysql | int | `9004` |  |
| service.ports.postgresql | int | `9005` |  |
| service.ports.tcp | int | `9000` |  |
| service.ports.tcpSecure | int | `9440` |  |
| service.sessionAffinity | string | `"None"` |  |
| service.sessionAffinityConfig | object | `{}` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| shards | int | `2` |  |
| sidecars | list | `[]` |  |
| startdbScripts | object | `{}` |  |
| startdbScriptsSecret | string | `""` |  |
| startupProbe.enabled | bool | `false` |  |
| startupProbe.failureThreshold | int | `3` |  |
| startupProbe.initialDelaySeconds | int | `10` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| terminationGracePeriodSeconds | string | `""` |  |
| tls.autoGenerated | bool | `false` |  |
| tls.certCAFilename | string | `""` |  |
| tls.certFilename | string | `""` |  |
| tls.certKeyFilename | string | `""` |  |
| tls.certificatesSecret | string | `""` |  |
| tls.enabled | bool | `false` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |
| usersExtraOverrides | string | `""` |  |
| usersExtraOverridesConfigmap | string | `""` |  |
| usersExtraOverridesSecret | string | `""` |  |
| volumePermissions.containerSecurityContext.runAsUser | int | `0` |  |
| volumePermissions.enabled | bool | `false` |  |
| volumePermissions.image.pullPolicy | string | `"IfNotPresent"` |  |
| volumePermissions.image.pullSecrets | list | `[]` |  |
| volumePermissions.image.registry | string | `"docker.io"` |  |
| volumePermissions.image.repository | string | `"bitnami/os-shell"` |  |
| volumePermissions.image.tag | string | `"11-debian-11-r40"` |  |
| volumePermissions.resources.limits | object | `{}` |  |
| volumePermissions.resources.requests | object | `{}` |  |
| zookeeper.enabled | bool | `true` |  |
| zookeeper.replicaCount | int | `3` |  |
| zookeeper.service.ports.client | int | `2181` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# common

![Version: 2.8.0](https://img.shields.io/badge/Version-2.8.0-informational?style=flat-square) ![Type: library](https://img.shields.io/badge/Type-library-informational?style=flat-square) ![AppVersion: 2.8.0](https://img.shields.io/badge/AppVersion-2.8.0-informational?style=flat-square)

A Library Helm Chart for grouping common logic between bitnami charts. This chart is not deployable by itself.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| exampleValue | string | `"common-chart"` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# postgresql

![Version: 12.8.2](https://img.shields.io/badge/Version-12.8.2-informational?style=flat-square) ![AppVersion: 15.4.0](https://img.shields.io/badge/AppVersion-15.4.0-informational?style=flat-square)

PostgreSQL (Postgres) is an open source object-relational database known for reliability and data integrity. ACID-compliant, it supports foreign keys, joins, views, triggers and stored procedures.

**Homepage:** <https://bitnami.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| VMware, Inc. |  | <https://github.com/bitnami/charts> |

## Source Code

* <https://github.com/bitnami/charts/tree/main/bitnami/postgresql>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| oci://registry-1.docker.io/bitnamicharts | common | 2.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| architecture | string | `"standalone"` |  |
| audit.clientMinMessages | string | `"error"` |  |
| audit.logConnections | bool | `false` |  |
| audit.logDisconnections | bool | `false` |  |
| audit.logHostname | bool | `false` |  |
| audit.logLinePrefix | string | `""` |  |
| audit.logTimezone | string | `""` |  |
| audit.pgAuditLog | string | `""` |  |
| audit.pgAuditLogCatalog | string | `"off"` |  |
| auth.database | string | `""` |  |
| auth.enablePostgresUser | bool | `true` |  |
| auth.existingSecret | string | `""` |  |
| auth.password | string | `""` |  |
| auth.postgresPassword | string | `""` |  |
| auth.replicationPassword | string | `""` |  |
| auth.replicationUsername | string | `"repl_user"` |  |
| auth.secretKeys.adminPasswordKey | string | `"postgres-password"` |  |
| auth.secretKeys.replicationPasswordKey | string | `"replication-password"` |  |
| auth.secretKeys.userPasswordKey | string | `"password"` |  |
| auth.usePasswordFiles | bool | `false` |  |
| auth.username | string | `""` |  |
| backup.cronjob.annotations | object | `{}` |  |
| backup.cronjob.command[0] | string | `"/bin/sh"` |  |
| backup.cronjob.command[1] | string | `"-c"` |  |
| backup.cronjob.command[2] | string | `"pg_dumpall --clean --if-exists --load-via-partition-root --quote-all-identifiers --no-password --file=${PGDUMP_DIR}/pg_dumpall-$(date '+%Y-%m-%d-%H-%M').pgdump"` |  |
| backup.cronjob.concurrencyPolicy | string | `"Allow"` |  |
| backup.cronjob.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| backup.cronjob.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| backup.cronjob.containerSecurityContext.readOnlyRootFilesystem | bool | `true` |  |
| backup.cronjob.containerSecurityContext.runAsGroup | int | `0` |  |
| backup.cronjob.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| backup.cronjob.containerSecurityContext.runAsUser | int | `1001` |  |
| backup.cronjob.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| backup.cronjob.failedJobsHistoryLimit | int | `1` |  |
| backup.cronjob.labels | object | `{}` |  |
| backup.cronjob.restartPolicy | string | `"OnFailure"` |  |
| backup.cronjob.schedule | string | `"@daily"` |  |
| backup.cronjob.startingDeadlineSeconds | string | `""` |  |
| backup.cronjob.storage.accessModes[0] | string | `"ReadWriteOnce"` |  |
| backup.cronjob.storage.annotations | object | `{}` |  |
| backup.cronjob.storage.existingClaim | string | `""` |  |
| backup.cronjob.storage.mountPath | string | `"/backup/pgdump"` |  |
| backup.cronjob.storage.resourcePolicy | string | `""` |  |
| backup.cronjob.storage.size | string | `"8Gi"` |  |
| backup.cronjob.storage.storageClass | string | `""` |  |
| backup.cronjob.storage.subPath | string | `""` |  |
| backup.cronjob.storage.volumeClaimTemplates.selector | object | `{}` |  |
| backup.cronjob.successfulJobsHistoryLimit | int | `3` |  |
| backup.cronjob.ttlSecondsAfterFinished | string | `""` |  |
| backup.enabled | bool | `false` |  |
| clusterDomain | string | `"cluster.local"` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| containerPorts.postgresql | int | `5432` |  |
| diagnosticMode.args[0] | string | `"infinity"` |  |
| diagnosticMode.command[0] | string | `"sleep"` |  |
| diagnosticMode.enabled | bool | `false` |  |
| extraDeploy | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.postgresql.auth.database | string | `""` |  |
| global.postgresql.auth.existingSecret | string | `""` |  |
| global.postgresql.auth.password | string | `""` |  |
| global.postgresql.auth.postgresPassword | string | `""` |  |
| global.postgresql.auth.secretKeys.adminPasswordKey | string | `""` |  |
| global.postgresql.auth.secretKeys.replicationPasswordKey | string | `""` |  |
| global.postgresql.auth.secretKeys.userPasswordKey | string | `""` |  |
| global.postgresql.auth.username | string | `""` |  |
| global.postgresql.service.ports.postgresql | string | `""` |  |
| global.storageClass | string | `""` |  |
| image.debug | bool | `false` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"bitnami/postgresql"` |  |
| image.tag | string | `"15.4.0-debian-11-r0"` |  |
| kubeVersion | string | `""` |  |
| ldap.basedn | string | `""` |  |
| ldap.binddn | string | `""` |  |
| ldap.bindpw | string | `""` |  |
| ldap.enabled | bool | `false` |  |
| ldap.port | string | `""` |  |
| ldap.prefix | string | `""` |  |
| ldap.scheme | string | `""` |  |
| ldap.searchAttribute | string | `""` |  |
| ldap.searchFilter | string | `""` |  |
| ldap.server | string | `""` |  |
| ldap.suffix | string | `""` |  |
| ldap.tls.enabled | bool | `false` |  |
| ldap.uri | string | `""` |  |
| metrics.containerPorts.metrics | int | `9187` |  |
| metrics.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| metrics.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| metrics.containerSecurityContext.enabled | bool | `true` |  |
| metrics.containerSecurityContext.runAsGroup | int | `0` |  |
| metrics.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| metrics.containerSecurityContext.runAsUser | int | `1001` |  |
| metrics.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| metrics.customLivenessProbe | object | `{}` |  |
| metrics.customMetrics | object | `{}` |  |
| metrics.customReadinessProbe | object | `{}` |  |
| metrics.customStartupProbe | object | `{}` |  |
| metrics.enabled | bool | `false` |  |
| metrics.extraEnvVars | list | `[]` |  |
| metrics.image.digest | string | `""` |  |
| metrics.image.pullPolicy | string | `"IfNotPresent"` |  |
| metrics.image.pullSecrets | list | `[]` |  |
| metrics.image.registry | string | `"docker.io"` |  |
| metrics.image.repository | string | `"bitnami/postgres-exporter"` |  |
| metrics.image.tag | string | `"0.13.2-debian-11-r15"` |  |
| metrics.livenessProbe.enabled | bool | `true` |  |
| metrics.livenessProbe.failureThreshold | int | `6` |  |
| metrics.livenessProbe.initialDelaySeconds | int | `5` |  |
| metrics.livenessProbe.periodSeconds | int | `10` |  |
| metrics.livenessProbe.successThreshold | int | `1` |  |
| metrics.livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.prometheusRule.enabled | bool | `false` |  |
| metrics.prometheusRule.labels | object | `{}` |  |
| metrics.prometheusRule.namespace | string | `""` |  |
| metrics.prometheusRule.rules | list | `[]` |  |
| metrics.readinessProbe.enabled | bool | `true` |  |
| metrics.readinessProbe.failureThreshold | int | `6` |  |
| metrics.readinessProbe.initialDelaySeconds | int | `5` |  |
| metrics.readinessProbe.periodSeconds | int | `10` |  |
| metrics.readinessProbe.successThreshold | int | `1` |  |
| metrics.readinessProbe.timeoutSeconds | int | `5` |  |
| metrics.resources.limits | object | `{}` |  |
| metrics.resources.requests | object | `{}` |  |
| metrics.service.annotations."prometheus.io/port" | string | `"{{ .Values.metrics.service.ports.metrics }}"` |  |
| metrics.service.annotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.service.clusterIP | string | `""` |  |
| metrics.service.ports.metrics | int | `9187` |  |
| metrics.service.sessionAffinity | string | `"None"` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `""` |  |
| metrics.serviceMonitor.jobLabel | string | `""` |  |
| metrics.serviceMonitor.labels | object | `{}` |  |
| metrics.serviceMonitor.metricRelabelings | list | `[]` |  |
| metrics.serviceMonitor.namespace | string | `""` |  |
| metrics.serviceMonitor.relabelings | list | `[]` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `""` |  |
| metrics.serviceMonitor.selector | object | `{}` |  |
| metrics.startupProbe.enabled | bool | `false` |  |
| metrics.startupProbe.failureThreshold | int | `15` |  |
| metrics.startupProbe.initialDelaySeconds | int | `10` |  |
| metrics.startupProbe.periodSeconds | int | `10` |  |
| metrics.startupProbe.successThreshold | int | `1` |  |
| metrics.startupProbe.timeoutSeconds | int | `1` |  |
| nameOverride | string | `""` |  |
| networkPolicy.egressRules.customRules | list | `[]` |  |
| networkPolicy.egressRules.denyConnectionsToExternal | bool | `false` |  |
| networkPolicy.enabled | bool | `false` |  |
| networkPolicy.ingressRules.primaryAccessOnlyFrom.customRules | list | `[]` |  |
| networkPolicy.ingressRules.primaryAccessOnlyFrom.enabled | bool | `false` |  |
| networkPolicy.ingressRules.primaryAccessOnlyFrom.namespaceSelector | object | `{}` |  |
| networkPolicy.ingressRules.primaryAccessOnlyFrom.podSelector | object | `{}` |  |
| networkPolicy.ingressRules.readReplicasAccessOnlyFrom.customRules | list | `[]` |  |
| networkPolicy.ingressRules.readReplicasAccessOnlyFrom.enabled | bool | `false` |  |
| networkPolicy.ingressRules.readReplicasAccessOnlyFrom.namespaceSelector | object | `{}` |  |
| networkPolicy.ingressRules.readReplicasAccessOnlyFrom.podSelector | object | `{}` |  |
| networkPolicy.metrics.enabled | bool | `false` |  |
| networkPolicy.metrics.namespaceSelector | object | `{}` |  |
| networkPolicy.metrics.podSelector | object | `{}` |  |
| postgresqlDataDir | string | `"/bitnami/postgresql/data"` |  |
| postgresqlSharedPreloadLibraries | string | `"pgaudit"` |  |
| primary.affinity | object | `{}` |  |
| primary.annotations | object | `{}` |  |
| primary.args | list | `[]` |  |
| primary.command | list | `[]` |  |
| primary.configuration | string | `""` |  |
| primary.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| primary.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| primary.containerSecurityContext.enabled | bool | `true` |  |
| primary.containerSecurityContext.runAsGroup | int | `0` |  |
| primary.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| primary.containerSecurityContext.runAsUser | int | `1001` |  |
| primary.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| primary.customLivenessProbe | object | `{}` |  |
| primary.customReadinessProbe | object | `{}` |  |
| primary.customStartupProbe | object | `{}` |  |
| primary.existingConfigmap | string | `""` |  |
| primary.existingExtendedConfigmap | string | `""` |  |
| primary.extendedConfiguration | string | `""` |  |
| primary.extraEnvVars | list | `[]` |  |
| primary.extraEnvVarsCM | string | `""` |  |
| primary.extraEnvVarsSecret | string | `""` |  |
| primary.extraPodSpec | object | `{}` |  |
| primary.extraVolumeMounts | list | `[]` |  |
| primary.extraVolumes | list | `[]` |  |
| primary.hostAliases | list | `[]` |  |
| primary.hostIPC | bool | `false` |  |
| primary.hostNetwork | bool | `false` |  |
| primary.initContainers | list | `[]` |  |
| primary.initdb.args | string | `""` |  |
| primary.initdb.password | string | `""` |  |
| primary.initdb.postgresqlWalDir | string | `""` |  |
| primary.initdb.scripts | object | `{}` |  |
| primary.initdb.scriptsConfigMap | string | `""` |  |
| primary.initdb.scriptsSecret | string | `""` |  |
| primary.initdb.user | string | `""` |  |
| primary.labels | object | `{}` |  |
| primary.lifecycleHooks | object | `{}` |  |
| primary.livenessProbe.enabled | bool | `true` |  |
| primary.livenessProbe.failureThreshold | int | `6` |  |
| primary.livenessProbe.initialDelaySeconds | int | `30` |  |
| primary.livenessProbe.periodSeconds | int | `10` |  |
| primary.livenessProbe.successThreshold | int | `1` |  |
| primary.livenessProbe.timeoutSeconds | int | `5` |  |
| primary.name | string | `"primary"` |  |
| primary.nodeAffinityPreset.key | string | `""` |  |
| primary.nodeAffinityPreset.type | string | `""` |  |
| primary.nodeAffinityPreset.values | list | `[]` |  |
| primary.nodeSelector | object | `{}` |  |
| primary.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| primary.persistence.annotations | object | `{}` |  |
| primary.persistence.dataSource | object | `{}` |  |
| primary.persistence.enabled | bool | `true` |  |
| primary.persistence.existingClaim | string | `""` |  |
| primary.persistence.labels | object | `{}` |  |
| primary.persistence.mountPath | string | `"/bitnami/postgresql"` |  |
| primary.persistence.selector | object | `{}` |  |
| primary.persistence.size | string | `"8Gi"` |  |
| primary.persistence.storageClass | string | `""` |  |
| primary.persistence.subPath | string | `""` |  |
| primary.pgHbaConfiguration | string | `""` |  |
| primary.podAffinityPreset | string | `""` |  |
| primary.podAnnotations | object | `{}` |  |
| primary.podAntiAffinityPreset | string | `"soft"` |  |
| primary.podLabels | object | `{}` |  |
| primary.podSecurityContext.enabled | bool | `true` |  |
| primary.podSecurityContext.fsGroup | int | `1001` |  |
| primary.priorityClassName | string | `""` |  |
| primary.readinessProbe.enabled | bool | `true` |  |
| primary.readinessProbe.failureThreshold | int | `6` |  |
| primary.readinessProbe.initialDelaySeconds | int | `5` |  |
| primary.readinessProbe.periodSeconds | int | `10` |  |
| primary.readinessProbe.successThreshold | int | `1` |  |
| primary.readinessProbe.timeoutSeconds | int | `5` |  |
| primary.resources.limits | object | `{}` |  |
| primary.resources.requests.cpu | string | `"250m"` |  |
| primary.resources.requests.memory | string | `"256Mi"` |  |
| primary.schedulerName | string | `""` |  |
| primary.service.annotations | object | `{}` |  |
| primary.service.clusterIP | string | `""` |  |
| primary.service.externalTrafficPolicy | string | `"Cluster"` |  |
| primary.service.extraPorts | list | `[]` |  |
| primary.service.headless.annotations | object | `{}` |  |
| primary.service.loadBalancerIP | string | `""` |  |
| primary.service.loadBalancerSourceRanges | list | `[]` |  |
| primary.service.nodePorts.postgresql | string | `""` |  |
| primary.service.ports.postgresql | int | `5432` |  |
| primary.service.sessionAffinity | string | `"None"` |  |
| primary.service.sessionAffinityConfig | object | `{}` |  |
| primary.service.type | string | `"ClusterIP"` |  |
| primary.sidecars | list | `[]` |  |
| primary.standby.enabled | bool | `false` |  |
| primary.standby.primaryHost | string | `""` |  |
| primary.standby.primaryPort | string | `""` |  |
| primary.startupProbe.enabled | bool | `false` |  |
| primary.startupProbe.failureThreshold | int | `15` |  |
| primary.startupProbe.initialDelaySeconds | int | `30` |  |
| primary.startupProbe.periodSeconds | int | `10` |  |
| primary.startupProbe.successThreshold | int | `1` |  |
| primary.startupProbe.timeoutSeconds | int | `1` |  |
| primary.terminationGracePeriodSeconds | string | `""` |  |
| primary.tolerations | list | `[]` |  |
| primary.topologySpreadConstraints | list | `[]` |  |
| primary.updateStrategy.rollingUpdate | object | `{}` |  |
| primary.updateStrategy.type | string | `"RollingUpdate"` |  |
| psp.create | bool | `false` |  |
| rbac.create | bool | `false` |  |
| rbac.rules | list | `[]` |  |
| readReplicas.affinity | object | `{}` |  |
| readReplicas.annotations | object | `{}` |  |
| readReplicas.args | list | `[]` |  |
| readReplicas.command | list | `[]` |  |
| readReplicas.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| readReplicas.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| readReplicas.containerSecurityContext.enabled | bool | `true` |  |
| readReplicas.containerSecurityContext.runAsGroup | int | `0` |  |
| readReplicas.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| readReplicas.containerSecurityContext.runAsUser | int | `1001` |  |
| readReplicas.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| readReplicas.customLivenessProbe | object | `{}` |  |
| readReplicas.customReadinessProbe | object | `{}` |  |
| readReplicas.customStartupProbe | object | `{}` |  |
| readReplicas.extendedConfiguration | string | `""` |  |
| readReplicas.extraEnvVars | list | `[]` |  |
| readReplicas.extraEnvVarsCM | string | `""` |  |
| readReplicas.extraEnvVarsSecret | string | `""` |  |
| readReplicas.extraPodSpec | object | `{}` |  |
| readReplicas.extraVolumeMounts | list | `[]` |  |
| readReplicas.extraVolumes | list | `[]` |  |
| readReplicas.hostAliases | list | `[]` |  |
| readReplicas.hostIPC | bool | `false` |  |
| readReplicas.hostNetwork | bool | `false` |  |
| readReplicas.initContainers | list | `[]` |  |
| readReplicas.labels | object | `{}` |  |
| readReplicas.lifecycleHooks | object | `{}` |  |
| readReplicas.livenessProbe.enabled | bool | `true` |  |
| readReplicas.livenessProbe.failureThreshold | int | `6` |  |
| readReplicas.livenessProbe.initialDelaySeconds | int | `30` |  |
| readReplicas.livenessProbe.periodSeconds | int | `10` |  |
| readReplicas.livenessProbe.successThreshold | int | `1` |  |
| readReplicas.livenessProbe.timeoutSeconds | int | `5` |  |
| readReplicas.name | string | `"read"` |  |
| readReplicas.nodeAffinityPreset.key | string | `""` |  |
| readReplicas.nodeAffinityPreset.type | string | `""` |  |
| readReplicas.nodeAffinityPreset.values | list | `[]` |  |
| readReplicas.nodeSelector | object | `{}` |  |
| readReplicas.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| readReplicas.persistence.annotations | object | `{}` |  |
| readReplicas.persistence.dataSource | object | `{}` |  |
| readReplicas.persistence.enabled | bool | `true` |  |
| readReplicas.persistence.existingClaim | string | `""` |  |
| readReplicas.persistence.labels | object | `{}` |  |
| readReplicas.persistence.mountPath | string | `"/bitnami/postgresql"` |  |
| readReplicas.persistence.selector | object | `{}` |  |
| readReplicas.persistence.size | string | `"8Gi"` |  |
| readReplicas.persistence.storageClass | string | `""` |  |
| readReplicas.persistence.subPath | string | `""` |  |
| readReplicas.podAffinityPreset | string | `""` |  |
| readReplicas.podAnnotations | object | `{}` |  |
| readReplicas.podAntiAffinityPreset | string | `"soft"` |  |
| readReplicas.podLabels | object | `{}` |  |
| readReplicas.podSecurityContext.enabled | bool | `true` |  |
| readReplicas.podSecurityContext.fsGroup | int | `1001` |  |
| readReplicas.priorityClassName | string | `""` |  |
| readReplicas.readinessProbe.enabled | bool | `true` |  |
| readReplicas.readinessProbe.failureThreshold | int | `6` |  |
| readReplicas.readinessProbe.initialDelaySeconds | int | `5` |  |
| readReplicas.readinessProbe.periodSeconds | int | `10` |  |
| readReplicas.readinessProbe.successThreshold | int | `1` |  |
| readReplicas.readinessProbe.timeoutSeconds | int | `5` |  |
| readReplicas.replicaCount | int | `1` |  |
| readReplicas.resources.limits | object | `{}` |  |
| readReplicas.resources.requests.cpu | string | `"250m"` |  |
| readReplicas.resources.requests.memory | string | `"256Mi"` |  |
| readReplicas.schedulerName | string | `""` |  |
| readReplicas.service.annotations | object | `{}` |  |
| readReplicas.service.clusterIP | string | `""` |  |
| readReplicas.service.externalTrafficPolicy | string | `"Cluster"` |  |
| readReplicas.service.extraPorts | list | `[]` |  |
| readReplicas.service.headless.annotations | object | `{}` |  |
| readReplicas.service.loadBalancerIP | string | `""` |  |
| readReplicas.service.loadBalancerSourceRanges | list | `[]` |  |
| readReplicas.service.nodePorts.postgresql | string | `""` |  |
| readReplicas.service.ports.postgresql | int | `5432` |  |
| readReplicas.service.sessionAffinity | string | `"None"` |  |
| readReplicas.service.sessionAffinityConfig | object | `{}` |  |
| readReplicas.service.type | string | `"ClusterIP"` |  |
| readReplicas.sidecars | list | `[]` |  |
| readReplicas.startupProbe.enabled | bool | `false` |  |
| readReplicas.startupProbe.failureThreshold | int | `15` |  |
| readReplicas.startupProbe.initialDelaySeconds | int | `30` |  |
| readReplicas.startupProbe.periodSeconds | int | `10` |  |
| readReplicas.startupProbe.successThreshold | int | `1` |  |
| readReplicas.startupProbe.timeoutSeconds | int | `1` |  |
| readReplicas.terminationGracePeriodSeconds | string | `""` |  |
| readReplicas.tolerations | list | `[]` |  |
| readReplicas.topologySpreadConstraints | list | `[]` |  |
| readReplicas.updateStrategy.rollingUpdate | object | `{}` |  |
| readReplicas.updateStrategy.type | string | `"RollingUpdate"` |  |
| replication.applicationName | string | `"my_application"` |  |
| replication.numSynchronousReplicas | int | `0` |  |
| replication.synchronousCommit | string | `"off"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| serviceBindings.enabled | bool | `false` |  |
| shmVolume.enabled | bool | `true` |  |
| shmVolume.sizeLimit | string | `""` |  |
| tls.autoGenerated | bool | `false` |  |
| tls.certCAFilename | string | `""` |  |
| tls.certFilename | string | `""` |  |
| tls.certKeyFilename | string | `""` |  |
| tls.certificatesSecret | string | `""` |  |
| tls.crlFilename | string | `""` |  |
| tls.enabled | bool | `false` |  |
| tls.preferServerCiphers | bool | `true` |  |
| volumePermissions.containerSecurityContext.runAsGroup | int | `0` |  |
| volumePermissions.containerSecurityContext.runAsNonRoot | bool | `false` |  |
| volumePermissions.containerSecurityContext.runAsUser | int | `0` |  |
| volumePermissions.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| volumePermissions.enabled | bool | `false` |  |
| volumePermissions.image.digest | string | `""` |  |
| volumePermissions.image.pullPolicy | string | `"IfNotPresent"` |  |
| volumePermissions.image.pullSecrets | list | `[]` |  |
| volumePermissions.image.registry | string | `"docker.io"` |  |
| volumePermissions.image.repository | string | `"bitnami/os-shell"` |  |
| volumePermissions.image.tag | string | `"11-debian-11-r34"` |  |
| volumePermissions.resources.limits | object | `{}` |  |
| volumePermissions.resources.requests | object | `{}` |  |


![purple-divider](https://user-images.githubusercontent.com/7065401/52071927-c1cd7100-2562-11e9-908a-dde91ba14e59.png)

# plausible-analytics

![Version: 0.3.3](https://img.shields.io/badge/Version-0.3.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.1.1](https://img.shields.io/badge/AppVersion-2.1.1-informational?style=flat-square)

A Helm Chart for Plausible Analytics - Simple, open-source, lightweight (< 1 KB) and privacy-friendly web analytics alternative to Google Analytics.

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| IMIO |  | <https://github.com/IMIO/> |

## Source Code

* <https://github.com/plausible/analytics>
* <https://github.com/imio/helm-charts>
* <https://github.com/imio/helm-plausible-analytics>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | clickhouse(clickhouse) | 3.6.7 |
| https://charts.bitnami.com/bitnami | postgresql(postgresql) | 12.8.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| baseURL | string | `"http://plausible-analytics.local"` |  |
| clickhouse | object | `{"auth":{"database":"plausible_events_db","password":"password","username":"clickhouse"},"enabled":true,"initContainers":[],"initdbScripts":{"db-init.sql":"CREATE DATABASE IF NOT EXISTS plausible_events_db\n"},"persistence":{"enabled":false},"replicaCount":1,"shards":1,"zookeeper":{"enabled":false}}` | ---------------------------------------------------------------------------- |
| clickhouseDatabaseURL | string | `"http://clickhouse:password@plausible-analytics-clickhouse:8123/plausible_events_db"` |  |
| clickhouseFlushIntervalMS | string | `""` |  |
| clickhouseMaxBufferSize | string | `""` |  |
| databaseCA | string | `nil` |  |
| databaseURL | string | `"postgres://postgres:postgres@plausible-analytics-postgresql:5432/plausible_db"` |  |
| disableRegistration | bool | `false` |  |
| extraEnv | list | `[]` |  |
| extra_geolocation.enabled | bool | `false` |  |
| extra_geolocation.geolite2CountryDB | string | `""` |  |
| extra_geolocation.geonamesSourceFile | string | `""` |  |
| extra_geolocation.maxmind.edition | string | `""` |  |
| extra_geolocation.maxmind.licenseKey | string | `""` |  |
| fullnameOverride | string | `""` |  |
| google.clientID | string | `nil` |  |
| google.clientSecret | string | `nil` |  |
| google.enabled | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| image.tag | string | `"v2.1.4"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts | list | `[]` |  |
| ingress.path | string | `"/"` |  |
| ingress.pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| labels | object | `{}` |  |
| listenIP | string | `"0.0.0.0"` |  |
| livenessProbe.httpGet.path | string | `"/"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| logFailedLoginAttempts | bool | `false` |  |
| mailer.adapter | string | `""` |  |
| mailer.email | string | `""` |  |
| mailer.enabled | bool | `false` |  |
| mailer.mailgun.apiKey | string | `""` |  |
| mailer.mailgun.baseURI | string | `""` |  |
| mailer.mailgun.domain | string | `""` |  |
| mailer.mandrillApiKey | string | `""` |  |
| mailer.postmarkApiKey | string | `""` |  |
| mailer.sendgridApiKey | string | `""` |  |
| mailer.smtp.auth | bool | `false` |  |
| mailer.smtp.host | string | `""` |  |
| mailer.smtp.password | string | `""` |  |
| mailer.smtp.port | string | `""` |  |
| mailer.smtp.retries | string | `""` |  |
| mailer.smtp.ssl | bool | `false` |  |
| mailer.smtp.username | string | `""` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| plausibleInitContainers.clickhouse.image.repository | string | `"bitnami/clickhouse"` |  |
| plausibleInitContainers.clickhouse.image.tag | string | `"23.3.9"` |  |
| plausibleInitContainers.curl.enabled | bool | `false` |  |
| plausibleInitContainers.curl.image.repository | string | `"curlimages/curl"` |  |
| plausibleInitContainers.curl.image.tag | string | `"8.2.1"` |  |
| plausibleInitContainers.enabled | bool | `true` |  |
| plausibleInitContainers.postgresql.image.repository | string | `"postgres"` |  |
| plausibleInitContainers.postgresql.image.tag | string | `"13.3-alpine"` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresql | object | `{"auth":{"database":"plausible_db","password":"postgres","username":"postgres"},"enabled":true,"metrics":{"enabled":false},"port":5432,"primary":{"persistence":{"enabled":false}},"replication":{"enabled":false}}` | ---------------------------------------------------------------------------- |
| readinessProbe.httpGet.path | string | `"/"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| readinessProbe.initialDelaySeconds | int | `30` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| secret.create | bool | `true` |  |
| secret.existingSecret | string | `""` |  |
| secretKeyBase | string | `""` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| totpVaultKey | string | `"dsxvbn3jxDd16az2QpsX5B8O+llxjQ2SJE2i5Bzx38I="` |  |


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
| disableRegistration | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/plausible/community-edition"` |  |
| image.tag | string | `"v2.1.4"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts | list | `[]` |  |
| ingress.path | string | `"/"` |  |
| ingress.pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
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


