# fly-buildkit

Run buildkit on Fly.io

This Fly app configuration runs the [`moby/buildkit`](https://github.com/moby/buildkit) image with configuration
suitable for building images on Fly.io.

## Getting started

Launch a builder, then use it to build itself:

```sh
APP=my-builder
fly launch --from https://github.com/wjordan/fly-buildkit --flycast --name $APP
fly deploy --buildkit-addr $APP.flycast:1234
```
