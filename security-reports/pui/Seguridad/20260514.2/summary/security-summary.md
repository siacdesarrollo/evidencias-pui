# Security pipeline summary

- Status files: 8
- Blocking findings: True
- Operational failure: True (3)
- Dependency failure: True (2)
- Skipped: True

## ACI-Cleanup
- Outcome: skipped
- Blocking findings: False
- Operational failure: False

## ACI-Deployment
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Error: You cannot call a method on a null-valued expression.

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
- Outcome: blocking_findings
- Blocking findings: True
- Operational failure: False
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260514_230632

## SCA
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260514_230538

## ZAP-ImagePublish
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Error: You cannot call a method on a null-valued expression.

