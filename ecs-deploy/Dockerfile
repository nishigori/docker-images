FROM python:3.5-alpine

# https://pypi.python.org/pypi/ecs-deploy/
ENV ECS_DEPLOY_VER 1.3.1

RUN set -x \
  && apk upgrade --no-cache \
  && pip install --no-cache-dir ecs-deploy==$ECS_DEPLOY_VER

ENTRYPOINT ["ecs", "deploy"]
CMD ["--help"]
