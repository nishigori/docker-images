# Docker rpmbuild image

Build to Docker Image
OS selected [CentOS](https://registry.hub.docker.com/_/centos/)
With rpmbuild

## Usage

```
$ docker pull nishigori/rpmbuild
```

---

## Development

### Requirements

* docker ~> 1.0.0
* boot2docker ~> 1.0.0 (only Mac OS)

```
$ docker build -t {APP_NAME} .
```
