# fly-buildkit

Run buildkit on Fly.io

This Fly app configuration runs the [`moby/buildkit`](https://github.com/moby/buildkit) image with configuration
suitable for building images on Fly.io.

## Getting started

Launch a builder based on this repo, then use it to build another app:

```sh
# in a builder directory:
BUILDER=my-builder
fly launch --from https://github.com/wjordan/fly-buildkit --flycast --name $BUILDER

# in your app directory:
fly deploy --buildkit-addr $BUILDER.flycast:1234
```
