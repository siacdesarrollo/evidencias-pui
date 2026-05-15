# Security pipeline summary

- Status files: 8
- Blocking findings: True
- Operational failure: True (3)
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
- Error: ZAP no respondió en 300 segundos.

## DAST
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\DAST\20260515_053934
- Error: Cannot bind parameter 'Uri'. Cannot convert value "http:///JSON/core/view/version/?apikey=***" to type "System.Uri". Error: "Invalid URI: The hostname could not be parsed."

## InstallTools
- Outcome: success
- Blocking findings: False
- Operational failure: False

## SAST
- Outcome: operational_failure
- Blocking findings: True
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260515_052550
- Failure reasons: codeql_analyze_retry_incomplete, codeql_analyze_incomplete
- Missing evidence: layer2_codeql.sarif
- Step exit codes: layer1Build=0, codeqlDatabaseCreate=0, codeqlAnalyze=99, codeqlDatabaseCreateRetry=0, codeqlAnalyzeRetry=99
- Tool availability: codeql=True
- Error: SAST no completó correctamente.; failureReasons=codeql_analyze_retry_incomplete, codeql_analyze_incomplete; missingEvidence=layer2_codeql.sarif; stepExitCodes=codeqlAnalyze=99, codeqlAnalyzeRetry=99; diagnosticPaths=runFolder=D:\a\1\s\reportes-seguridad\SAST\20260515_052550, layer1Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer1_build.sarif, codeqlCreateLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_create.txt, codeqlAnalyzeLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_analyze.txt, codeqlCreateRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_create_retry.txt, codeqlAnalyzeRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_analyze_retry.txt, layer2Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql.sarif, scriptStatus=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\SAST_status.json; scriptMessage=SAST terminó con fallos operativos o evidencia incompleta.
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SAST\20260515_052550
  - layer1Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer1_build.sarif
  - codeqlCreateLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_create.txt
  - codeqlAnalyzeLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_analyze.txt
  - codeqlCreateRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_create_retry.txt
  - codeqlAnalyzeRetryLog=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql_analyze_retry.txt
  - layer2Sarif=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\layer2_codeql.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SAST\20260515_052550\SAST_status.json

## SCA
- Outcome: success
- Blocking findings: False
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260515_052507
- Step exit codes: restore=0, build=0, dotnetList=0, trivyTable=0, trivySarif=0
- Tool availability: trivy=True
- Diagnostic paths:
  - runFolder=D:\a\1\s\reportes-seguridad\SCA\20260515_052507
  - trivySarif=D:\a\1\s\reportes-seguridad\SCA\20260515_052507\SCA_trivy.sarif
  - scriptStatus=D:\a\1\s\reportes-seguridad\SCA\20260515_052507\SCA_status.json

## ZAP-ImagePublish
- Outcome: success
- Blocking findings: False
- Operational failure: False

