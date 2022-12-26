---
title: KUBERNETES
description: 'Cheatsheet and guide to master Kubernetes'
created: 12-03-2022
tags:
- program
- docker
- containers
---

## TERMS

```bash 
mamespaces
```
Group of different resources and configuration objects.

## COMMANDS

 ```bash
- kubectl cluster-info- Infomación del cluster
- kubectl get nodes - Información de los nodos
- kubectl get pods - Infomacion de los pods
- kubectl get deployment or kubectl get deploy - Informacion de los deployments
- kubectl get services` orkubectl get svc` - Información de los Servicios.
- kubectl get namespaces` - Informacion de namespaces
- kubectl get pods --namespace=nombre del namespace` - ver los pods que corren en esenamespace`
- kubectl run (nombre de la imagen) --image=(nombre de la imagen en docker hub` - Crear pod manualmente.
- kubectl describe pod nginx - Ver la información de un pod.
- kubectl get pods -o -wide` - Más informacion del pod.
- kubectl delete pod (name of the image)`- Borra una imagen o 'contenedor'.
- kubectl create deployment nginx --image=nginx` - desplegar un pod. Se puede ver informacion conkubectl describe deployments` okubectl get deployment`.
- kubectl scale deployment (name of de deployment) --replicas=5` - Para replicar un deployment la veces que se quiera, en este caso '5'. Para disminuir el número de réplicas, simplemente cambiar el número dereplicas=5`. Por ejemploreplicas=3`.
- kubectl expose deployment (nobre del deployment) --port=8080 --target-port=80`. - Exponer un puerto interno de un deployment.
```


