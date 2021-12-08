# Docker image for Robot framework

This repo holds a Dockerfile as base layer for [Robot framework][robot] test suites. It currently used by

* [WLCG JWT compliance test suite][wlcg-jwt-compliance-tests]
* [ESCAPE authN/Z test suite][escape-auth-tests]

The Docker image is built at any push or pull request. It is pushed on [DockerHub][docker] at any tag of the code.

The Docker image name is `indigoiam/robot-framework`; the available tags for the image are `<sha>`, `<tag>` and `latest`.

[robot]: https://robotframework.org/
[wlcg-jwt-compliance-tests]: https://github.com/indigo-iam/wlcg-jwt-compliance-tests
[escape-auth-tests]: https://github.com/indigo-iam/escape-auth-tests
[docker]: https://hub.docker.com/r/indigoiam/robot-framework
