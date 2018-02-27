IMAGE_NAME=fpm-wordpress

build:
	docker rmi -f $(IMAGE_NAME) || true
	docker build -t $(IMAGE_NAME) .

release:
	docker tag $(IMAGE_NAME) scardetto/$(IMAGE_NAME)
	docker push scardetto/$(IMAGE_NAME)
