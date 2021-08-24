### Useful commands for working with Azure Bash CLI

**Create Service User account**
```
  az ad sp create-for-rbac --name ServicePrincipalName
```

**Get Credentials for Kubernetes cluster**
```
az aks get-credentials --resource-group <resource_group_name> --name <cluster_name>
```

**Build&push image to the Azure  registry**
```
az acr build --image <image_name> --registry <registry_name> --file Dockerfile .
```

** Attach container registry to AKS**
```
az aks update -n <aks_cluster> -g <group_name> --attach-acr <registry_name>
```
