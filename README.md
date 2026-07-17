# mattermost-team-edition-arm Docker image

Forked on [cburschka/mattermost-arm](https://hub.docker.com/r/cburschka/mattermost-arm)

Like the official Mattermost Team Edition Docker image but built for arm64.

See https://hub.docker.com/r/mattermost/mattermost-team-edition or https://docs.mattermost.com/install/install-docker.html#deploy-mattermost-on-docker-for-production-use for usage instructions, but use `ngrie/mattermost-team-edition-arm` as image name instead. For instance, in a `compose.yml`/`docker-compose.yml`, use:
```yaml
services:
  mattermost:
    image: cburschka/mattermost-arm:latest
```

This image is based on the original Dockerfile with as few adjustments as necessary (see [create-dockerfile.sh](./create-dockerfile.sh)).

# MAINTENANCE

I'll probably keep this up to date with ESR versions for as long as I'm using Mattermost.

If you need a version that isn't here, the steps to build it yourself are:

1. Fork this repository on GitHub.
2. Create a repository on https://hub.docker.com/ named something like `<yourname>/<repo>`
3. Generate an access token, and add it to the secrets of your fork (under `DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`).
4. Edit [.github/workflows/docker.yml](./.github/workflows/docker.yml) to change the repository to `<yourname>/<repo>`.
5. Make sure that GitHub actions are enabled, as they get disabled by default when forking a repository.
6. Tag the release you want to build. This must be of the form `v*.*.*` and correspond to one of the tagged [Mattermost releases](https://github.com/mattermost/mattermost/releases).
7. Push the tag.
