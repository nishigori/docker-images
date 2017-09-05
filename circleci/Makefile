DOCKER_IMAGE := nishigori/circleci
DOCKER_TAGS   = $(subst Dockerfile.,,$(wildcard Dockerfile.*))
DOCKER_TAG   :=

BUILD_AND_PUSH := true


.PHONY: help docker/* $(DOCKER_TAGS)
.DEFAULT_GOAL: help

help:
	@echo "U can exec: $$ make [ $(DOCKER_TAGS) ]"

docker/pull:
	$(@D) $(@F) $(DOCKER_IMAGE) --all-tags

docker/push:
ifeq (,$(findstring $(DOCKER_TAG),$(DOCKER_TAGS)))
	$(error "Dockerfile.$(DOCKER_TAG) is not found")
endif
	$(@D) login
	$(@D) $(@F) $(DOCKER_IMAGE):$(DOCKER_TAG)

$(DOCKER_TAGS): docker/pull
	docker build -f Dockerfile.$@ -t $(DOCKER_IMAGE):$@ .
ifeq (true,$(BUILD_AND_PUSH))
	@$(MAKE) docker/push DOCKER_TAG=$@
endif
