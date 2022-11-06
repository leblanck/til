# Creating a ConfigMap using kubectl

I recently struggeled with getting a multiline entry for the `data:` key formatted correctly and it was causing a `CrashLoopBackOff` error. I remedied this by just using `kubectl` to create the ConfigMap for me.

```
kubectl create configmap nginx-config --from-file=/etc/nginx/default.conf
```

This does not create a YAML file but it will create the ConfigMap in place. You can then have your pod call that ConfigMap.

[Source](https://unofficial-kubernetes.readthedocs.io/en/latest/tasks/configure-pod-container/configmap/)

