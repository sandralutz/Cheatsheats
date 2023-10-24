# Kubernetes

## Creating/Updating resources

Apply resource to cluster
```
kubectl apply -f myresource.yaml
```
Scale deployment to 10 replicas
```
kubctl scale deploy \<name> --replicas=10
```
Opens editor to change YAML
```
kubectl edit deploy \<name>

```
<br>
<br>

## Quick commands

Launch a pod called \<name> using image \<image-name>
```
kubectl run --image \<image-name> \<image>
```
Create a service described in \<manifest.yaml>
```
kubectl create -f \<manifest.yaml>
```
Drain worker node
```
kubectl drain \<n> --delete-local-data --force --ignore-daemonsets
```
Create namespace \<name>
```
kubectl crreat namespace \<namespace>

```
<br>
<br>

## Debuging

Execute \<command> on \<service> optionally
Selecting container \<container>
```
kubectl exec \<service> [-c \<container>] --\<command>
```
Get logs from service \<name> optionally
Selecting \<$container> 
```
kubectl logs -f \<name> [-c <container>]
```
Show metrics for nodes
```
kubectl top node
```
Show merics for pods
```
kubectl top pod
```
Forward port of pod to localhost
```
kubectl port-forward \<pod-name> \<local:port>:\<pod-port>

```
<br>
<br>

## Pod and Node commands

List current pods [services, nodes, deployments]
```
kubectl get pods [svc, nodes, deploy]
```
Describe current pods [service, nodes, deploy]
```
kubectl describe pods [service, nodes, deploy] \<name>
```
Delete Pod [Node]
```
kubectl delete pod [node] \<name>
```
Tail my app logs
```
kubectl logs -f \<pod-name> [-c <container-name>]
```
Get all pods with a certain label
```
kubectl get pods -l application=app
```
Watch nodes continuously
```
kubectl get nodes -w
```
Show metrics for a pod by container
```
kubectl top pod --containers
```
Get definition of pod
```
kubectl get pod \<name> -o yaml

```
<br>
<br>

## API objects

|Objects|Short|
|---|---|
|all||
|certificates||
|cluserrolebindings||
|clusterroles||
|configmap|cm|
|customresourcedefinition|crd|
|cronjobs||
|deployments|deploy|
|daemonsets|ds|
|endpoints|ep|
|events|ev|
|horizontalpodautoscalers|hpa|
|ingresses|ing|
|jobs||
|limitranges|limits|
|mysqlclusters||
|nodes|no|
|namespaces|ns|
|poddisruptionbudget|pdb|
|pods|po|
|persistentvolumes|pv|
|persistentvolumeclaims|pvc|
|resourcequotas|quota|
|rolebindings||
|roles||
|replicasets|rs|
|serviceaccounts|sa|
|storageclasses|sc|
|secrets||
|statefulsets|sts|
|services|svs|

