.DEFAULT_GOAL := compile 

compile:
	# Simple easy compile, completely docker driven.
	# Copy everything into an idiomatic gopath for easy debugging.  Build and copy to a build/perceptor binary.
	docker run -t -i --rm -v $(shell pwd):/go/src/github.com/blackducksoftware/perceptor/ -w /go/src/github.com/blackducksoftware/perceptor -e CGO_ENABLED=0 -e GOOS=linux -e GOARCH=amd64 golang:1.9 go build -o build/perceptor ./cmd/perceptor

# Hydra is the name of the secret WW2 people in captain america.
hydra:
	docker run -t -i --rm -v $(shell pwd):/go/src/github.com/blackducksoftware/perceptor/ -w /go/src/github.com/blackducksoftware/perceptor -e CGO_ENABLED=0 -e GOOS=linux -e GOARCH=amd64 golang:1.9 go build -o build/hydra ./contrib/cmd/hydra_install/

test:
	go test ./pkg/...
