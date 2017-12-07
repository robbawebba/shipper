proto:
	 protoc -I. --go_out=plugins=grpc:$(GOPATH)/src/github.com/robbawebba/shipper/consignment-service proto/consignment/consignment.proto
build:
	GOOS=linux GOARCH=amd64 go build github.com/robbawebba/shipper/consignment-service
	docker build -t consignment-service $(GOPATH)/src/github.com/robbawebba/shipper/consignment-service

run:
	docker run -p 4000:50051 consignment-service
