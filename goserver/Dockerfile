FROM golang:1.16-alpine as base

FROM base as dev

WORKDIR /app

COPY go.mod ./
COPY go.sum ./
# RUN go mod download

COPY *.go ./

RUN go build -o /goserv

EXPOSE 8080

CMD [ "/goserv" ]