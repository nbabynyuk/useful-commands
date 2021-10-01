Useful kubectl commands

**List all context(clusters)**
```
kubectl config get-contexts
```
**Change current configured cluster**
```
kubectl config use-context <context-name>
```
**Make a port forwarding**
```
k port-forward <my-pod-name> <host-port>:<container-port>
Example: k port-forward my-nginx 8080:80
```
**Create/Edit resources**
```
k apply -f <finame-with-a-spec>
```
**Delete Resources**
```
k delete -f <filename-with-resources-to-de-deleted>
```
**Get details about pods(describe)**
```
k describe pod <pod-name>
```
**Get shell inside in pods**
```
k exec -it <target-pod-name> -c <target-container-if-many> -- /bin/sh
```
**Create config map from env file**
```
k create configmap sample-app-config --from-env-file app-sample.env
Sample of env file
SAMPLE-APP-CONFIG-VALUE=Some-Config-Value
```
**Create a secret**
```
k create secret generic app-secret --from-literal=DB_PASSWORD=tsss!_value_here
```
