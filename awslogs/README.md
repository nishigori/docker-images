# Docker awslogs image

Build to Docker Image
With [awslogs](https://github.com/jorgebastida/awslogs/tree/0.10)

## Usage

```
$ docker run --rm -it -v ~/.aws:/root/.aws:ro nishigori/awslogs get $GROUP [STREAM_EXPRESSION]
```

---

## Development

### Requirements

* docker

```
$ docker build -t {APP_NAME} .
```
