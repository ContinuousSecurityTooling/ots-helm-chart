# ots

![Version: 1.2.0](https://img.shields.io/badge/Version-1.2.0-informational?style=flat-square) ![AppVersion: 1.11.1](https://img.shields.io/badge/AppVersion-1.11.1-informational?style=flat-square)

A Helm chart for deploying OTS

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| customizations | map | `{"metricsAllowedSubnets":["127.0.0.1/24","10.0.0.0/8"]}` | customization options, see https://github.com/Luzifer/ots/wiki/Customization |
| env | map | `[{"name":"SECRET_EXPIRY","value":"172800"}]` | environment variables for app config |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"luzifer/ots"` |  |
| image.tag | string | `"v1.12.0"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hostname | string | `""` |  |
| ingress.tls | object | `{}` |  |
| metrics.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `true` |  |
| metrics.serviceMonitor.relabelings[0].replacement | string | `"ots"` |  |
| metrics.serviceMonitor.relabelings[0].targetLabel | string | `"application"` |  |
| metrics.serviceMonitor.relabelings[1].sourceLabels[0] | string | `"pod"` |  |
| metrics.serviceMonitor.relabelings[1].targetLabel | string | `"instance"` |  |
| metrics.serviceMonitor.scrapeTimeout | string | `"10s"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.storageClass | string | `""` |  |
| persistence.volumeSize | string | `"1Gi"` |  |
| podAnnotations | object | `{}` |  |
| redis.enabled | bool | `true` |  |
| redis.version | string | `"7.2.2"` |  |
| replicaCount | int | `1` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.13.1](https://github.com/norwoodj/helm-docs/releases/v1.13.1)
