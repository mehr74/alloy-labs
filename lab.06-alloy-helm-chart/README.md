# Alloy Helm Chart installation

```bash
# start a new kind cluster
kind create cluster --name alloy-helm-chart

# add Grafana helm repo
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update

# get values for alloy helm chart
helm show values grafana/alloy > alloy.values.yaml

# install alloy helm chart
helm upgrade --install alloy grafana/alloy -f alloy.values.overwrite.yaml

# port forward to access alloy
kubectl port-forward service/alloy 12345:12345
```

At the end, you can remove the kind cluster.
```bash
kind delete cluster --name alloy-helm-chart
```