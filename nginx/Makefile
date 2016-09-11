.PHONY: release tag_latest build

NAME = taaviteska/nginx
VERSION = 1.11.2

build:
	docker build -t $(NAME):$(VERSION) --rm .

build-fast:
	docker build -t $(NAME):$(VERSION) .

tag_latest:
	docker tag $(NAME):$(VERSION) $(NAME):latest

push:
	@if ! docker images $(NAME) | awk '{ print $$2 }' | grep -q -F $(VERSION); then echo "$(NAME) version $(VERSION) is not yet built. Please run 'make build'"; false; fi
	docker push $(NAME)

release: build tag_latest push
release-fast: build-fast tag_latest push
