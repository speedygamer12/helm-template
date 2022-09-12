# Helm Project

## What is this project
NGINX served static page using kubernetes objects. packaged with Helm, and deployed with ArgoCD to different namespaces

## Features
- Multiple namespaces created
- Config map as volume mount for different namespace 
- Secrets as env variable for different namespace

## Getting started

### clone repo:
`git clone https://github.com/speedygamer12/helm-template`
`cd helm-template`

### To deploy:
| namespace| `command` |
| default name space | `kubectl apply -f application.yaml` |
| multiple name space | `kubectl apply -f applications.yaml` |

### Get deployment urls:
- `minkube service list`

### To access env variable
run:
`kubectl get pod --namespace default`
for each pods, run:
`kubectl exec <<pod_name>> -- env | grep secret-key`
