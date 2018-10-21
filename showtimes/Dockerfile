# golang image where workspace (GOPATH) configured at /go.
FROM golang:1.10

# Install dependencies
RUN go get gopkg.in/mgo.v2
RUN go get github.com/gorilla/mux

# Setting up working directory
COPY . /go/src/github.com/soeunj/microservices-example/showtimes/

# Build the showtimes command inside the container.
RUN go install github.com/soeunj/microservices-example/showtimes/

# Run the showtimes microservice when the container starts.
ENTRYPOINT microservices-example

# Service listens on port 8080.
ENV PORT 8080
EXPOSE 8080
