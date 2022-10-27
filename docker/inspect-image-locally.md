# Inspecting a Docker Image Locally Before Building

Sometimes helpful to get a terminal into an image to creep around and see what it needs to fit your image goals. What tools need to be installed vs. what is already installed etc. 

```bash
docker run -it --rm --name ubuntu ubuntu:20.04 /bin/bash
```

`--rm` will remove this container/clean up after itself once we are finished.