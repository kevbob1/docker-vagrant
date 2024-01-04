# how to build and push to docker hub


## setup buildx (do once)
docker buildx create --name container --driver=docker-container

## run multi-arch build for arm and x86
docker buildx build --builder=container --platform=linux/amd64,linux/arm64 -t <repo>:<tag> .

