
build:
	docker rmi -f php-apache || true
	docker build -t php-apache .

release:
	docker tag php-apache scardetto/php-apache
	docker push scardetto/php-apache
