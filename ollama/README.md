# Ollama

Ollama experiments and notes

# Local Configuration

Add this configuration in /etc/hosts

```
echo "127.0.0.1 ollama.localhost" > /etc/hosts
``` 


# Kubernetes

Create namespace

```
kubectl create namespace ollama

```

Add [Ollama Helm repo](https://artifacthub.io/packages/helm/ollama-helm/ollama) 


```
helm repo add ollama-helm https://otwld.github.io/ollama-helm/
helm repo update
helm install -f values.yaml ollama ollama-helm/ollama --namespace ollama
```

