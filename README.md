# Docker image for robot framework

This repo holds a Dockerfile as base layer for [Robot framework][robot] test suite.

The Docker image is built at any push or pull request.  
It is pushed on [DockerHub][docker] at any tag of the code.  
The Docker image name is `indigoiam/robot-framework`;  
the available tags for the image are `<sha>`, `<tag>` and `latest`.

The Docker image is currently used by

* [WLCG JWT compliance test suite][wlcg-jwt-compliance-tests]
* [ESCAPE authN/Z test suite][escape-auth-tests]

[robot]: https://robotframework.org/
[docker]: https://hub.docker.com/r/indigoiam/robot-framework
[wlcg-jwt-compliance-tests]: https://github.com/indigo-iam/wlcg-jwt-compliance-tests
[escape-auth-tests]: https://github.com/indigo-iam/escape-auth-tests