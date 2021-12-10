# Robot framework Docker image

This repo provides a Docker image for [Robot framework][robot]-based test suites. 

The image, besides a recent, python3 based Robot framework environment, provides tools commonly used in WLCG data management:

- jq
- oidc-agent
- voms clients
- gfal
- curl (compiled against OpenSSL)

More details in the [Dockerfile](./docker/Dockerfile).

The image is currently used by:

- The [WLCG JWT compliance test suite][wlcg-jwt-compliance-tests]
- The [ESCAPE authN/Z test suite][escape-auth-tests]

The image is built in CI on every commit or pull request submitted to this repo. It is pushed on [DockerHub][dockerhub-repo] when the code is tagged.

The Docker image name is `indigoiam/robot-framework`. To see the list of tags available, check the [DockerHub repo][dockerhub-repo].

[robot]: https://robotframework.org/
[wlcg-jwt-compliance-tests]: https://github.com/indigo-iam/wlcg-jwt-compliance-tests
[escape-auth-tests]: https://github.com/indigo-iam/escape-auth-tests
[dockerhub-repo]: https://hub.docker.com/r/indigoiam/robot-framework
