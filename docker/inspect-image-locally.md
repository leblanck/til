# Inspecting a Docker Image Locally Before Building

Sometimes helpful to get a terminal into an image to creep around and see what it needs to fit your image goals. What tools need to be installed vs. what is already installed etc. 

```bash
docker run -it --name ubuntu ubuntu:20.04 /bin/bash
```

You do need to have this image pulled down locally from whatever container registry you are using. 