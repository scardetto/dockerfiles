IMAGE_NAME=capybara-headless-chrome
CHROME_VERSION=68

build:
	docker rmi --force $(IMAGE_NAME) || true
	docker build --no-cache --tag $(IMAGE_NAME) .
	docker tag $(IMAGE_NAME) scardetto/$(IMAGE_NAME)

release:
	docker tag $(IMAGE_NAME) scardetto/$(IMAGE_NAME):chrome-$(CHROME_VERSION)
	docker push scardetto/$(IMAGE_NAME):chrome-$(CHROME_VERSION)
