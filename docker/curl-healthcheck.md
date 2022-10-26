# Running a curl HEALTHCHECK on an Alpine Based Image

I often use something like `curl http://localhost:8080` or something similar to check if an app is up an running locally on the exposed port. I started using alpine based images recently and they do not have curl installed by default. 

To install curl add the following to your Dockerfile:

```Dockerfile
RUN apk --no-cache add curl
```

You can then use HEALTHCHECK as follows:

```Dockerfile
HEALTHCHECK --interval=30s --timeout=30s --start-period=10s --retries=3 \
    CMD curl http://localhost:8080 || exit 1
```

or something similar...
