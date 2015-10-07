# docker-compose docker image

This image allows you to run `docker-compose` inside of `docker` container
instead of installing it on your docker host.

## Tags

- `brainly/docker-compose:1.4`
- `brainly/docker-compose:latest` - latest released version of `docker-compose`
- `brainly/docker-compose:edge` - latest built version from `master` branch of
  https://github.com/docker/compose/

## Development

After cloning the repo, to build an image, you can use:

```bash
./scripts/build <tag>
```

Where `<tag>` is one of available versions.

Versions are represented as directories in `/versions/<tag>`. Each directory
contains its own `Dockerfile`.

## Contributing

1. Fork it ( https://github.com/waterlink/active_record.cr/fork )
1. Create your feature branch (git checkout -b my-new-feature)
1. Commit your changes (git commit -am 'Add some feature')
1. Push to the branch (git push origin my-new-feature)
1. Create a new Pull Request

## Contributors

- [alex-fedorov](https://github.com/alex-fedorov) (or
  [waterlink](https://github.com/waterlink)) Oleksii Fedorov - creator,
  maintainer
