# Security pipeline summary

- Status files: 8
- Blocking findings: True
- Operational failure: True (2)
- Dependency failure: True (2)
- Skipped: False

## ACI-Cleanup
- Outcome: success
- Blocking findings: False
- Operational failure: False

## ACI-Deployment
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Failure reasons: aci_missing_public_endpoint
- Error: ACI no devolvió FQDN ni IP pública para ZAP.

## ACI-ReadyCheck
- Outcome: dependency_failed
- Blocking findings: False
- Operational failure: False
- Dependency unmet: aci-deployment.json
- Error: No existe información válida del despliegue ACI para esperar ZAP.

## DAST
- Outcome: dependency_failed
- Blocking findings: False
- Operational failure: False
- Dependency unmet: aci-deployment.json
- Error: No existe información válida del despliegue de ZAP en ACI.

## InstallTools
- Outcome: success
- Blocking findings: False
- Operational failure: False

## SAST
- Outcome: operational_failure
- Blocking findings: True
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260515_045628
- Failure reasons: codeql_analyze_retry_incomplete, codeql_analyze_incomplete
- Missing evidence: layer2_codeql.sarif
- Step exit codes: layer1Build=0, codeqlDatabaseCreate=0, codeqlAnalyze=99, codeqlDatabaseCreateRetry=0, codeqlAnalyzeRetry=99
- Tool availability: codeql=True
- Error: SAST no completó correctamente.; failureReasons=codeql_analyze_retry_incomplete, codeql_analyze_incomplete; missingEvidence=layer2_codeql.sarif; stepExitCodes=codeqlAnalyze=99, codeqlAnalyzeRetry=99; scriptMessage=SAST terminó con fallos operativos o evidencia incompleta.; scriptError=SAST no completó correctamente.; failureReasons=codeql_analyze_retry_incomplete, codeql_analyze_incomplete; missingEvidence=layer2_codeql.sarif; stepExitCodes=codeqlAnalyze=99, codeqlAnalyzeRetry=99

## SCA
- Outcome: success
- Blocking findings: False
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260515_045530
- Step exit codes: restore=0, build=0, dotnetList=0, trivyTable=0, trivySarif=0
- Tool availability: trivy=True

## ZAP-ImagePublish
- Outcome: success
- Blocking findings: False
- Operational failure: False

