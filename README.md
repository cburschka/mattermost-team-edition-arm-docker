# mattermost-team-edition-arm Docker image

[ngrie/mattermost-team-edition-arm on Docker Hub](https://hub.docker.com/r/ngrie/mattermost-team-edition-arm)

(Forked on [cburschka/mattermost-arm])(https://hub.docker.com/r/cburschka/mattermost-arm)

Like the official Mattermost Team Edition Docker image but built for arm64.

See https://hub.docker.com/r/mattermost/mattermost-team-edition or https://docs.mattermost.com/install/install-docker.html#deploy-mattermost-on-docker-for-production-use for usage instructions, but use `ngrie/mattermost-team-edition-arm` as image name instead. For instance, in a `compose.yml`/`docker-compose.yml`, use:
```yaml
services:
  mattermost:
    image: cburschka/mattermost-arm:latest
```

This image is based on the original Dockerfile with as few adjustments as necessary (see [create-dockerfile.sh](./create-dockerfile.sh)).
