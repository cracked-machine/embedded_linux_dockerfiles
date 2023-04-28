# Embedded Linux Dockerfiles

|Name|Image|Build|Run|Push|
|:-|:-|:-|:-|:-|
|Core Yocto Image|yocto_core|DOCKER_BUILDKIT=1 docker build -f dockerfiles/yocto_core/Dockerfile -t ghcr.io/cracked-machine/yocto_core:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/yocto_core:ubuntu2204|docker push ghcr.io/cracked-machine/yocto_core:ubuntu2204|
|Xilinx Yocto Image|yocto_xlnx|DOCKER_BUILDKIT=1 docker build -f dockerfiles/yocto_xlnx/Dockerfile -t ghcr.io/cracked-machine/yocto_xlnx:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/yocto_xlnx:ubuntu2204|docker push ghcr.io/cracked-machine/yocto_xlnx:ubuntu2204|
|Open ST Linux Docker Image|yocto_openstlinux|DOCKER_BUILDKIT=1 docker build -f dockerfiles/yocto_openstlinux/Dockerfile -t ghcr.io/cracked-machine/yocto_openstlinux:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/yocto_openstlinux:ubuntu2204|docker push ghcr.io/cracked-machine/yocto_openstlinux:ubuntu2204|
|Buildroot Image|buildroot|DOCKER_BUILDKIT=1 docker build -f dockerfiles/buildroot/Dockerfile -t ghcr.io/cracked-machine/buildroot:ubuntu2204 .|docker run -it --rm ghcr.io/cracked-machine/buildroot:ubuntu2204|docker push ghcr.io/cracked-machine/buildroot:ubuntu2204|

You must setup a [personal access token](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry) to push/pull this with the github docker registry used in the commands above.

A [devcontainer.json](example/devcontainer.json) example file is provided for use with vscode extension.