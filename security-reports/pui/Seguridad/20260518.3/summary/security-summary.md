# Security pipeline summary

- Status files: 9
- Blocking findings: True
- Operational failure: True (1)
- Dependency failure: True (1)
- Skipped: False

## ACI-Cleanup
- Outcome: success
- Blocking findings: False
- Operational failure: False

## ACI-Deployment
- Outcome: success
- Blocking findings: False
- Operational failure: False

## ACI-Diagnostics
- Outcome: success
- Blocking findings: False
- Operational failure: False
- Report folder: D:\a\1\a\security-status\aci-diagnostics
- Step exit codes: show=0, logs=0
- Tool availability: az=True
- Diagnostic paths:
  - showStatus=D:\a\1\a\security-status\aci-diagnostics\aci-show-summary.json
  - eventsStatus=D:\a\1\a\security-status\aci-diagnostics\aci-events.json
  - containerLog=D:\a\1\a\security-status\aci-diagnostics\aci-logs.txt
  - scriptStatus=D:\a\1\a\security-status\aci-diagnostics.json

## ACI-ReadyCheck
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Failure reasons: zap_readiness_timeout
- Error: ZAP no respondió al endpoint público de versión dentro del timeout. readinessMode=aci_state_observation_public_http_confirmation; resourceGroupName=PUI; containerGroupName=pui-zap-security; containerName=pui-zap-security; probeUrl=http://pui-zap-security-eoqgw0uuoo.mexicocentral.azurecontainer.io:8080/JSON/core/view/version/?***; timeoutSeconds=300; pollIntervalSeconds=10; requestTimeoutSeconds=10; lastHttpStatusCode=sin HTTP status; lastError=The request was canceled due to the configured HttpClient.Timeout of 10 seconds elapsing.

## DAST
- Outcome: dependency_failed
- Blocking findings: False
- Operational failure: False
- Dependency unmet: aci-ready.json
- Failure reasons: zap_readiness_not_successful
- Error: El paso de readiness no dejó a ZAP listo; se omite DAST remoto para evitar una ejecución engañosa posterior.

## InstallTools
- Outcome: success
- Blocking findings: False
- Operational failure: False

## SAST
- Outcome: blocking_findings
- Blocking findings: True
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260518_225438
- Step exit codes: layer1Build=0, codeqlDatabaseCreate=0, codeqlPackDownload=0, codeqlAnalyze=0
- Tool availability: codeql=True
- Error: SAST detectó hallazgos bloqueantes: layer1Sarif=20, layer2Sarif=38, layer1BuildErrors=0.
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SAST\20260518_225438
  - layer1Sarif=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer1_build.sarif
  - codeqlCreateLog=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql_create.txt
  - codeqlPackDownloadLog=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql_pack_download.txt
  - codeqlAnalyzeLog=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql_analyze.txt
  - codeqlCreateRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql_create_retry.txt
  - codeqlAnalyzeRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql_analyze_retry.txt
  - layer2Sarif=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\layer2_codeql.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SAST\20260518_225438\SAST_status.json

## SCA
- Outcome: success
- Blocking findings: False
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260518_225353
- Step exit codes: restore=0, build=0, dotnetList=0, trivyTable=0, trivySarif=0
- Tool availability: trivy=True
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SCA\20260518_225353
  - trivySarif=D:\a\1\s\reportes-seguridad\SCA\20260518_225353\SCA_trivy.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SCA\20260518_225353\SCA_status.json

## ZAP-ImagePublish
- Outcome: success
- Blocking findings: False
- Operational failure: False

