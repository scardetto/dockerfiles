OWNER=scardetto
IMAGE_NAME=teamcity-agent
IMAGE_TAG=2018-05-17-04

build:
	docker rmi --force $(IMAGE_NAME) || true
	docker build --tag $(IMAGE_NAME) .
	docker tag $(IMAGE_NAME) $(OWNER)/$(IMAGE_NAME)

release:
	docker tag $(IMAGE_NAME) $(OWNER)/$(IMAGE_NAME):$(IMAGE_TAG)
	docker push scardetto/$(IMAGE_NAME):$(IMAGE_TAG)
