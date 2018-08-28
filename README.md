Restarting a Service
---

If a service appears to be down you can restart it by issuing:

```
kubectl delete pod -l app=hail-ci
```

replacing `hail-ci` with `batch` to restart the `batch` service.

Before doing this, please save the logs for *both* services and create an issue in the appropriate repository.

```
kubectl logs -l app=hail-ci > hail-ci.log
kubectl logs -l app=batch > batch.log
```
