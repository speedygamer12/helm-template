## Helm Project

To access env variable
run:
` export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=helm-template,app.kubernetes.io/instance=helm-template" -o jsonpath="{.items[0].metadata.name}")`
`kubectl get pod --namespace default $POD_NAME`

`kubectl exec <<pod_name>> -- env | grep secret-key`


