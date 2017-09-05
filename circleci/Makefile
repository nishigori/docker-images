DOCKER_IMAGE := nishigori/circleci
DOCKER_TAGS   = $(subst Dockerfile.,,$(wildcard Dockerfile.*))

BUILD_AND_PUSH := true


.PHONY: help docker/* $(DOCKER_TAGS)
.DEFAULT_GOAL: help

help:
	@echo "U can exec: $$ make [ $(DOCKER_TAGS) ]"

docker/login:
	$(@D) $(@F)

docker/pull:
	$(@D) $(@F) $(DOCKER_IMAGE) --all-tags

$(DOCKER_TAGS): docker/pull
	docker build -f Dockerfile.$@ -t $(DOCKER_IMAGE):$@ .
ifeq (true,$(BUILD_AND_PUSH))
	@$(MAKE) docker/login
	docker push $(DOCKER_IMAGE):$@
endif
