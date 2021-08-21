FROM ubuntu:20.10

EXPOSE 8080

WORKDIR /go

COPY example-backend .

RUN apt update && apt install -y golang-go ca-certificates

RUN go build

CMD ./server