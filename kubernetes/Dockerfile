FROM golang:1-alpine as build

WORKDIR /app
COPY hello.go hello.go
RUN go build hello.go

FROM alpine:latest

WORKDIR /app
COPY --from=build /app/hello /app/hello

EXPOSE 8180
ENTRYPOINT ["./hello"]
