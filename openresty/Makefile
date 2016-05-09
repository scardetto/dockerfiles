
build:
	docker rmi -f openresty || true
	docker build -t openresty .

release:
	docker tag openresty scardetto/openresty
	docker push scardetto/openresty
