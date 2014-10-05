FROM debian:jessie
COPY . /app
RUN apt-get update && apt-get install golang git mercurial -y && export GOPATH=/app && cd /app && go get . ; go build . && mv /app/app /app/controller
EXPOSE 8080
ENTRYPOINT ["/app/controller"]
