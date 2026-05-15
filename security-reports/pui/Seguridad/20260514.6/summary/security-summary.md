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
- Failure reasons: aci_container_create_invalid_json
- Error: az container create devolvió una respuesta no interpretable.; failureCategory=invalid_json; exitCode=0; command=az container create --resource-group PUI --name pui-zap-security --location mexicocentral --image siacacr-h6c7ekdph3h2fhgb.azurecr.io/security/zaproxy:2.17.0 --cpu 2 --memory 4 --ports 8080 --ip-address Public --restart-policy Always --os-type Linux --environment-variables ZAP_PORT=8080 --secure-environment-variables ZAP_API_KEY=*** --command-line "/bin/sh -c \"zap.sh -daemon -host 0.0.0.0 -port ${ZAP_PORT} -config api.disablekey=false -config api.key=${ZAP_API_KEY} -config api.addrs.addr.name=.* -config api.addrs.addr.regex=true\"" --dns-name-label pui-zap-security-eOqgW0UuoO --registry-login-server siacacr-h6c7ekdph3h2fhgb.azurecr.io --registry-username siacacr --registry-password *** --only-show-errors --output json; parseError=Conversion from JSON failed with error: Unexpected character encountered while parsing value: C. Path '', line 0, position 0.; stdout=Command az container create : Create a container group. Arguments --resource-group -g [Required] : Name of resource group. You can configure the default group using `az configure --defaults group=<name>`. --command-line : The command line to run when the container is started, e.g. '/bin/bash -c myscript.sh'. --config-map : A list of config map key-value pairs for the container. Space-separated values in 'key=value' format. --cpu : The required number of CPU cores of the containers, accurate to one decimal place. --dns-name-label : The dns name label for container group with public IP. --env...

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
- Report folder: D:\a\1\s\reportes-seguridad\SAST\20260515_032526
- Failure reasons: codeql_analyze_incomplete
- Missing evidence: layer2_codeql.sarif
- Step exit codes: layer1Build=0, codeqlDatabaseCreate=0, codeqlAnalyze=99
- Tool availability: codeql=True
- Error: SAST no completó correctamente.; failureReasons=codeql_analyze_incomplete; missingEvidence=layer2_codeql.sarif; stepExitCodes=codeqlAnalyze=99

## SCA
- Outcome: operational_failure
- Blocking findings: False
- Operational failure: True
- Report folder: D:\a\1\s\reportes-seguridad\SCA\20260515_032435
- Step exit codes: restore=0, build=0, dotnetList=0, trivyTable=0, trivySarif=0
- Tool availability: trivy=True
- Error: SCA no completó correctamente.

## ZAP-ImagePublish
- Outcome: success
- Blocking findings: False
- Operational failure: False

