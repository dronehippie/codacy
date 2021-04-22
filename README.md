# codacy

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/codacy?sort=semver)](https://github.com/dronehippie/codacy) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/codacy/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/codacy) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/codacy/latest)](https://hub.docker.com/r/dronehippie/codacy) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/codacy)](https://hub.docker.com/r/dronehippie/codacy) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/codacy.svg)](https://pkg.go.dev/github.com/dronehippie/codacy) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/codacy)](https://goreportcard.com/report/github.com/dronehippie/codacy) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/c3ec547734f746a583a35c91a28e1f6b)](https://www.codacy.com/gh/dronehippie/codacy/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/codacy&amp;utm_campaign=Badge_Grade)

Drone plugin to upload coverage reports to Codacy. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/codacy/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/codacy \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/codacy .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/codacy
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```
