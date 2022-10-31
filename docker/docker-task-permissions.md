# Resolving Docker Task Permission Denied in Bamboo CI

Recently had a failing pipeline when trying to build docker images on a local agent runner. 

```bash
31-Oct-2022 09:56:33 	Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post "http://...": dial unix /var/run/docker.sock: connect: permission denied
```

Resolving this makes sense in hindsight, make sure you have the user running your bamboo service added to your docker group:

`sudo usermod -a -G docker $USER`

Restart the whole box, or restart the bamboo service _and_ the docker service. 

source: [atlassian](https://confluence.atlassian.com/bamkb/docker-task-permission-denied-887749337.html)
