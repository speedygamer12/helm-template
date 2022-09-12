## Helm Project

Get deployment urls:
- `minkube service list`
To access env variable
run:
`kubectl get pod --namespace default`
for each pods, run:
`kubectl exec <<pod_name>> -- env | grep secret-key`


