# Weaviate Kubernetes

Instructions taken from https://weaviate.io/developers/weaviate/current/getting-started/installation.html

```bash
# Set the Weaviate chart version
export CHART_VERSION="v14.2.0"
# Download the Weaviate Helm chart
wget https://github.com/semi-technologies/weaviate-helm/releases/download/$CHART_VERSION/weaviate.tgz
# Download an example values.yml (with the default configuration)
wget https://raw.githubusercontent.com/semi-technologies/weaviate-helm/$CHART_VERSION/weaviate/values.yaml
# Create a Weaviate namespace
kubectl create namespace weaviate
# Deploy
helm upgrade \
  "weaviate" \
  weaviate.tgz \
  --install \
  --namespace "weaviate" \
  --values ./values.yaml
```
