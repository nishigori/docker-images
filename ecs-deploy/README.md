# Docker ecs-deploy image

Build to Docker Image
With [ecs-deploy](https://github.com/fabfuel/ecs-deploy)

## Usage

```
$ docker run --rm -it -v ~/.aws:/root/.aws:ro nishigori/ecs-deploy my-cluster my-service
```

---

## Development

### Requirements

* docker

```
$ docker build -t {APP_NAME} .
```
