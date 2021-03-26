[![docker-publish-to-dh 1.19-alpine](https://github.com/swaglive/docker-nginx/actions/workflows/docker-publish-to-dh.yaml/badge.svg)](https://github.com/swaglive/docker-nginx/actions/workflows/docker-publish-to-dh-1.19-alpine.yaml)

## Get latest `Dockerfile` template
```bash
curl -o Dockerfile https://raw.githubusercontent.com/nginxinc/docker-nginx/master/modules/Dockerfile.alpine
```

## Add a module (if it's not on pkg-oss[1])
```bash
mkdir -p modules/echo
echo "https://github.com/openresty/echo-nginx-module/archive/v0.62.tar.gz" > docker/echo/source
```

Build image
```bash
docker-compose up --build
```

## Other Info
[1] Packaged modules `Makefile.module-*`: https://hg.nginx.org/pkg-oss/file/tip/alpine
[2] DockerHub - nginx: https://hub.docker.com/_/nginx
