# README

https://github.com/grpc-ecosystem/grpc-gateway

## The grpc

protoc -I . \
    --go_out ./gen/go/ --go_opt paths=source_relative \
    --go-grpc_out ./gen/go/ --go-grpc_opt paths=source_relative \
    your/service/v1/your_service.proto

## Just the gateway stubs

protoc -I . --grpc-gateway_out ./gen/go \
    --grpc-gateway_opt logtostderr=true \
    --grpc-gateway_opt paths=source_relative \
    --grpc-gateway_opt generate_unbound_methods=true \
    your/service/v1/your_service.proto

buf mod update

## Annotations

https://github.com/grpc-ecosystem/grpc-gateway/blob/master/examples/internal/proto/examplepb/a_bit_of_everything.proto
