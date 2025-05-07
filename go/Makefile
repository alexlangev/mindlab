.DEFAULT_GOAL := build

.PHONY:fmt vet build
fmt:
	go fmt ./...

vet: fmt
	go vet ./...

build: vet
	go build -o # binary file name

clean:
	go clean # filepath for binary
	# rm -f stuff

test:
	go test -v ./... # run all tests
