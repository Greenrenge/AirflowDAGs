# airflow

```yaml
affinity: {}
airflow:
  auth:
    forcePassword: false
    username: user
  baseUrl: http://127.0.0.1:8080
  cloneDagFilesFromGit:
    branch: master
    enabled: true
    repository: git@github.com:Greenrenge/airflow.git
  clonePluginsFromGit:
    enabled: false
  gitSyncInterval: 60
  loadExamples: true
  scheduler:
    resources:
      limits: {}
      requests: {}
  web:
    resources:
      limits: {}
      requests: {}
  worker:
    port: 8793
    replicas: 2
    resources:
      limits: {}
      requests: {}
externalDatabase:
  database: bitnami_airflow
  existingSecret: ""
  host: localhost
  password: ""
  port: 5432
  user: bn_airflow
externalRedis:
  existingSecret: ""
  host: localhost
  password: ""
  port: 6379
git:
  pullPolicy: IfNotPresent
  registry: docker.io
  repository: bitnami/git
  tag: 2.26.0-debian-10-r18
image:
  debug: false
  pullPolicy: IfNotPresent
  registry: docker.io
  repository: bitnami/airflow
  tag: 1.10.9-debian-10-r67
ingress:
  annotations: null
  certManager: false
  enabled: false
  hosts:
  - name: airflow.local
    path: /
    tls: false
    tlsSecret: airflow.local-tls
  secrets: null
ldap:
  base: ou=example,o=org
  binddn: cn=user,ou=example,o=org
  bindpw: ""
  enabled: false
  tls:
    CAcertificateFilename: ""
    CAcertificateSecret: ""
    allowSelfSigned: true
    enabled: false
  uidField: uid
  uri: ldap://ldap_server:389
livenessProbe:
  enabled: true
  failureThreshold: 6
  initialDelaySeconds: 180
  periodSeconds: 20
  successThreshold: 1
  timeoutSeconds: 5
metrics:
  enabled: true
  image:
    pullPolicy: IfNotPresent
    registry: docker.io
    repository: bitnami/airflow-exporter
    tag: 0.20180711.0-debian-10-r72
  podAnnotations:
    prometheus.io/port: "9112"
    prometheus.io/scrape: "true"
nodeSelector: {}
postgresql:
  enabled: true
  existingSecret: ""
  postgresqlDatabase: bitnami_airflow
  postgresqlUsername: bn_airflow
readinessProbe:
  enabled: true
  failureThreshold: 6
  initialDelaySeconds: 30
  periodSeconds: 10
  successThreshold: 1
  timeoutSeconds: 5
redis:
  enabled: true
  existingSecret: ""
schedulerImage:
  debug: true
  pullPolicy: IfNotPresent
  registry: docker.io
  repository: bitnami/airflow-scheduler
  tag: 1.10.9-debian-10-r63
securityContext:
  enabled: true
  fsGroup: 1001
  runAsUser: 1001
service:
  annotations: null
  port: 8080
  type: ClusterIP
tolerations: []
updateStrategy: RollingUpdate
workerImage:
  debug: true
  pullPolicy: IfNotPresent
  registry: docker.io
  repository: bitnami/airflow-worker
  tag: 1.10.9-debian-10-r61

```
