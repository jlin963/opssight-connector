FROM scratch

MAINTAINER Black Duck OpsSight Team

ARG LASTCOMMIT
ARG BUILDTIME
ARG VERSION

# Container catalog requirements
COPY ./LICENSE /licenses/
COPY ./deployer-help.1 /help.1

COPY ./protoform ./protoform

LABEL name="Black Duck OpsSight Deployer" \
      vendor="Black Duck Software" \
      release.version="$VERSION" \
      summary="Black Duck OpsSight Deployer" \
      description="This container is used to deploy the Black Duck OpsSight Connector." \
      lastcommit="$LASTCOMMIT" \
      buildtime="$BUILDTIME"

CMD ["./protoform"]
