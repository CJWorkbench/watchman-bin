Prebuilt [Watchman](https://facebook.github.io/watchman/docs/install.html)
binary.

# Usage

In a Dockerfile that should have a watchman binary:

```Dockerfile
FROM workbenchdata/watchman:v0.0.1-buster-slim as watchman

FROM debian:buster-slim AS my-image

COPY --from=watchman /usr/bin/watchman /usr/bin/watchman
COPY --from=watchman /usr/var/run/watchman /usr/var/run/watchman
```
