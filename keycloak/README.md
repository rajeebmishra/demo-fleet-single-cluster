# Keycloak

# How to deploy

```
For now this repo can deploy for 2 environments. First on simple default base deployment by executing
kustomize  build base/. --enable-helm  | kubectl apply -f

For environment specific deployment for e.g. to deploy in dev environment with dev environment specific configuration:
kustomize  build environments/dev/. --enable-helm  | kubectl apply -f

```


# How to acces the UI

Since the keycloak is deployed as ClusterIP, you can use port-forward to access the UI

```
kubectl port-forward svc/keycloak-http -n keycloak 3000:80
```

# Sample Client UI

http://localhost:3000
