# Entorno local de Kubernetes

Anteriormente este repositorio usaba Vagrant, pero se ha modernizado para usar [kind (Kubernetes in Docker)](https://kind.sigs.k8s.io/).

## Uso

1. Instala [Docker](https://docs.docker.com/get-docker/) y [kind](https://kind.sigs.k8s.io/docs/user/quick-start/#installation).
2. Crea el cluster local:
   ```bash
   kind create cluster --name k8s-local
   ```
3. Interactúa con tu cluster usando `kubectl`:
   ```bash
   kubectl get nodes
   ```
4. Para eliminar el cluster:
   ```bash
   kind delete cluster --name k8s-local
   ```
