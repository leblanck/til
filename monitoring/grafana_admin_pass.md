# Changing Local Grafana Admin Password

Recently lost my local admin password for my self-hosted Grafana instance. Not sure what happened to the 1Password entry I had...

Anyway, to reset this password run the following:

```
grafana-cli admin reset-admin-password <new password>
```

I had to do this within the docker container that Grafana was running in. 


*source:* [grafana](https://grafana.com/docs/grafana/v9.0/cli/#reset-admin-password)
