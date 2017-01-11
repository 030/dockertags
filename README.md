# dockertags

[![Docker Repository on Quay](https://quay.io/repository/wantedly/dockertags/status "Docker Repository on Quay")](https://quay.io/repository/wantedly/dockertags)

`dockertags` retrieves and print available Docker image tag list from image repository.

## How to build and install

```bash
$ go get -d github.com/wantedly/dockertags
$ cd $GOPATH/src/github.com/wantedly/dockertags
$ make
$ make install
```

## Usage

```bash
$ dockertags
Usage:
  dockertags IMAGENAME
```

Provide Docker image name, then available tags of given image will be shown.

```bash
$ dockertags quay.io/wantedly/dockertags
latest
master

$ dockertags mysql/mysql-server
latest
8.0
8.0.0
5.7
5.7.9
...
5.5.42
```

## Supported image registry

- [Quay.io](https://quay.io)
  - To retrieve tags of private image, pass [API access token](http://docs.quay.io/api/) to `QUAYIO_TOKEN` environement variable.
- [Docker Hub](https://hub.docker.com)

## License
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
