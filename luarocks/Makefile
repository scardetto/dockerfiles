
build:
	docker rmi -f luarocks || true
	docker build -t luarocks .

release:
	docker tag luarocks scardetto/luarocks
	docker push scardetto/luarocks
