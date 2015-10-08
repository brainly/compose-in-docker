# docker-compose docker image

This image allows you to run `docker-compose` inside of `docker` container
instead of installing it on your docker host.

## Tags

- `brainly/compose-in-docker:1.4`
- `brainly/compose-in-docker:latest` - latest released version of `docker-compose`
- `brainly/compose-in-docker:edge` - latest built version from `master` branch of
  https://github.com/docker/compose/

## Usage

With `docker-machine`:

```bash
docker run \
  -v $DOCKER_CERT_PATH:/certs \
  -e DOCKER_TLS_VERIFY="$DOCKER_TLS_VERIFY" \
  -e DOCKER_HOST="$DOCKER_HOST" \
  -e DOCKER_CERT_PATH="/certs" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  brainly/compose-in-docker \
  docker-compose -p yourprojectname up
```

With just `docker`:

```bash
docker run \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  brainly/compose-in-docker \
  docker-compose -p yourprojectname up
```

## Development

After cloning the repo, to build an image, you can use:

```bash
./scripts/build <tag>
```

Where `<tag>` is one of available versions.

Versions are represented as directories in `/versions/<tag>`. Each directory
contains its own `Dockerfile`.

## Contributing

1. Fork it ( https://github.com/brainly/compose-in-docker/fork )
1. Create your feature branch (git checkout -b my-new-feature)
1. Commit your changes (git commit -am 'Add some feature')
1. Push to the branch (git push origin my-new-feature)
1. Create a new Pull Request

## Contributors

- [alex-fedorov](https://github.com/alex-fedorov) (or
  [waterlink](https://github.com/waterlink)) Oleksii Fedorov - creator,
  maintainer
