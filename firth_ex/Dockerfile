ARG Secret
FROM golang:1.19-alpine AS builder
WORKDIR /app
COPY main.go .
ENV GO111MODULE auto
RUN  go mod init main && \
     go mod tidy && \
     go build 
RUN cd /home/user/gocalc/ && \
     echo "@Secret" >> file
      
FROM alpine:3.10.3
RUN apk --no-cache add ca-certificates
WORKDIR /root/
COPY --from=0 /app/  ./
CMD ["./app"]
