# Multi-arch Minio docker container

This image allows multi architecture docker container for Minio based on the [official project](https://github.com/minio/minio)

## Building the image

Multi architecture image build with Docker buildx:

```shell
chmod +x docker-entrypoint.sh
docker buildx build --platform linux/amd64,linux/arm64,linux/arm/v7 -t pablogarciaarevalo/minio:latest --push .
```

## Running the container

```shell
docker pull pablogarciaarevalo/minio
docker run -p 9000:9000 pablogarciaarevalo/minio server /data
docker
```


