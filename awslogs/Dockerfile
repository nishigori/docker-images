FROM python:3-alpine

# https://pypi.python.org/pypi/awslogs/
ENV AWSLOGS_VER 0.10.0

RUN set -x \
  && apk upgrade --no-cache \
  && pip install --no-cache-dir awslogs==$AWSLOGS_VER

ENTRYPOINT ["awslogs"]
CMD []
