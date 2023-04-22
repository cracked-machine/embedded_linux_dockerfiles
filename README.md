# yocto_docker

|Name|Image|Build|Run|Push|
|:-|:-|:-|:-|:-|
|Core Yocto Image|yocto_docker|DOCKER_BUILDKIT=1 docker build -f dockerfiles/yocto_docker/Dockerfile -t ghcr.io/cracked-machine/yocto_docker:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/yocto_docker:ubuntu2204|docker push ghcr.io/cracked-machine/yocto_docker:ubuntu2204|
|Open ST Linux Docker Image|openstlinux_docker|DOCKER_BUILDKIT=1 docker build -f dockerfiles/openstlinux_docker/Dockerfile -t ghcr.io/cracked-machine/openstlinux_docker:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/openstlinux_docker:ubuntu2204|docker push ghcr.io/cracked-machine/openstlinux_docker:ubuntu2204|

You must setup a [personal access token](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry) to push/pull this with the github docker registry used in the commands above.

A [devcontainer.json](example/devcontainer.json) example file is provided for use with vscode extension.