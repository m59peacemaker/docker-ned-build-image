# pmkr/ned-build-image

Docker image that builds a docker image for running a node application developed with [ned](https://www.npmjs.com/package/ned).

See [ned-build-image](https://www.npmjs.com/package/ned-build-image) documentation.

### development

```sh
# build image for development
docker run -it \
-v /var/run/docker.sock:/var/run/docker.sock \
-v $PWD:/app \
pmkr/ned-build-image dev
```

```sh
# run development image
docker run -it --rm \
-v $PWD:/app \
--user $(id -u) \
ned-app-dev
```

### production

```sh
# build image for production
docker run -it \
-v /var/run/docker.sock:/var/run/docker.sock \
-v $PWD:/app \
pmkr/ned-build-image prod
```

```sh
# run production image
docker run -it ned-app-prod
```
