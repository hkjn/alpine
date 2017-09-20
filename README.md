# alpine

Repo alpine holds some alpine images.

## Image manifests

The image manifests which allows the Docker registry 2.2+ to support multiple
CPU architectures for `hkjn/alpine` currently needs to be built and pushed
using the standalone [`manifest-tool`](https://github.com/estesp/manifest-tool):

```
$ manifest-tool push from-args --platforms linux/amd64,linux/arm,linux/arm64 --template hkjn/alpine:ARCH --target hkjn/alpine
```
