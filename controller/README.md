For debugging:

```
kubectl proxy --port=8080
KUBERNETES_SERVICE_PROTOCOL=http KUBERNETES_SERVICE_HOST=localhost KUBERNETES_SERVICE_PORT=8080 ./tensorset-controller.sh
```
