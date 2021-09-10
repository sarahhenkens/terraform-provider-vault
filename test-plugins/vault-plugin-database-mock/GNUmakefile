GOARCH = amd64
GOOS = linux

.DEFAULT_GOAL := all

all: fmt build

build:
	GOOS=$(GOOS) GOARCH="$(GOARCH)" go build -o ../bin/vault-plugin-database-mock cmd/vault-plugin-database-mock/main.go

clean:
	rm -f ../bin/vault-plugin-database-mock

fmt:
	go fmt $$(go list ./...)

.PHONY: build clean fmt
