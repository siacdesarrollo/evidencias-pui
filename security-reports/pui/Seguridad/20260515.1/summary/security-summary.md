# Security pipeline summary

- Status files: 8
- Blocking findings: True
- Operational failure: True (2)
- Dependency failure: False (0)
- Skipped: False

## ACI-Cleanup
- Outcome: success
- Blocking findings: False
- Operational failure: False

## ACI-Deployment
- Outcome: success
- Blocking findings: False
- Operational failure: False

## ACI-ReadyCheck
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Error: ZAP no respondió en 300 segundos. Último estado: sin código HTTP. Último error: The request was canceled due to the configured HttpClient.Timeout of 10 seconds elapsing.

## DAST
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\DAST\20260515_074251
- Error: Response status code does not indicate success: 504 (Gateway Timeout).

## InstallTools
- Outcome: success
- Blocking findings: False
- Operational failure: False

## SAST
- Outcome: blocking_findings
- Blocking findings: True
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260515_073250
- Step exit codes: layer1Build=0, codeqlDatabaseCreate=0, codeqlAnalyze=0
- Tool availability: codeql=True
- Error: SAST detectó hallazgos bloqueantes: layer1Sarif=20, layer2Sarif=5, explicitBuildErrors=0.
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SAST\20260515_073250
  - layer1Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer1_build.sarif
  - codeqlCreateLog=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer2_codeql_create.txt
  - codeqlAnalyzeLog=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer2_codeql_analyze.txt
  - codeqlCreateRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer2_codeql_create_retry.txt
  - codeqlAnalyzeRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer2_codeql_analyze_retry.txt
  - layer2Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\layer2_codeql.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SAST\20260515_073250\SAST_status.json

## SCA
- Outcome: success
- Blocking findings: False
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260515_073203
- Step exit codes: restore=0, build=0, dotnetList=0, trivyTable=0, trivySarif=0
- Tool availability: trivy=True
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SCA\20260515_073203
  - trivySarif=D:\a\1\s\reportes-seguridad\SCA\20260515_073203\SCA_trivy.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SCA\20260515_073203\SCA_status.json

## ZAP-ImagePublish
- Outcome: success
- Blocking findings: False
- Operational failure: False

