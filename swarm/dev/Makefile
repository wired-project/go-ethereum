.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/wired-project/go-wired/cmd/swarm
	go build -o bin/geth     github.com/wired-project/go-wired/cmd/geth
	go build -o bin/bootnode github.com/wired-project/go-wired/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/wired-project/go-wired/swarm/...
