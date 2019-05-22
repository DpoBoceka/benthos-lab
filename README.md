Benthos Lab
===========

[![Build Status](https://cloud.drone.io/api/badges/benthosdev/benthos-lab/status.svg)](https://cloud.drone.io/benthosdev/benthos-lab)

This is an experimental site using a WASM build of Benthos for testing pipelines
in the browser.

This repo is subject to stagnation, modification beyond recognition, outright
deletion. I'm basically just messing about for fun, please don't get mad.

### Install

Pull a docker image with:

``` sh
docker pull jeffail/benthos-lab
```

### Build

``` sh
# Build client
GOOS=js GOARCH=wasm go build -o ./client/wasm/benthos-lab.wasm ./client/wasm/benthos-lab.go

# Install server
go install ./server/benthos-lab
```

Docker:

``` sh
docker build . -t benthosdev/benthos-lab
```

### Run

``` sh
cd ./client && benthos-lab
```

Docker:

``` sh
docker run --rm -p 8080:8080 benthosdev/benthos-lab
```

Then open your browser at `http://localhost:8080`.
