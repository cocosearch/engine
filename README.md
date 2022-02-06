# server

[![Build Status](https://github.com/cocosearch/server/workflows/CI/badge.svg?branch=main&event=push)](https://github.com/cocosearch/server/actions?query=workflow%3ACI)
[![codecov](https://codecov.io/gh/cocosearch/server/branch/main/graph/badge.svg?token=FM4NOMPT7Q)](https://codecov.io/gh/cocosearch/server)
[![License](https://img.shields.io/github/license/cocosearch/server.svg)](https://github.com/cocosearch/server/blob/main/LICENSE)
[![Tag](https://img.shields.io/github/tag/cocosearch/server.svg)](https://github.com/cocosearch/server/tags)
[![Gitter chat](https://badges.gitter.im/craftslab/cocosearch.png)](https://gitter.im/craftslab/cocosearch)



## Introduction

*server* is the distributed ninja of [cocosearch](https://github.com/cocosearch) written in Rust.



## Prerequisites

- Rust >= 1.57.0



## Run

```bash
git clone https://github.com/cocosearch/server.git

cd server
make build
./target/release/server --config-file="$PWD/src/config/config.yml"
```



## Docker

```bash
git clone https://github.com/cocosearch/server.git

cd server
make docker
docker run -v "$PWD"/src/config:/tmp ghcr.io/cocosearch/server:latest --config-file="/tmp/config.yml"
```



## Usage

```
USAGE:
    server --config-file <NAME>

OPTIONS:
    -c, --config-file <NAME>    Config file (.yml)
    -h, --help                  Print help information
    -V, --version               Print version information
```



## Settings

*server* parameters can be set in the directory [config](https://github.com/cocosearch/server/blob/main/src/config).

An example of configuration in [config.yml](https://github.com/cocosearch/server/blob/main/src/config/config.yml):

```yaml
apiVersion: v1
kind: server
metadata:
  name: server
spec:
  foo: foo
```



## License

Project License can be found [here](LICENSE).



## Reference

- [rocket](https://rocket.rs/)
- [rocket-examples](https://github.com/SergioBenitez/Rocket/tree/master/examples)
