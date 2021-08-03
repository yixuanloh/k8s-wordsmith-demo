FROM golang:alpine as builder
WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip
RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/dispatcher.go .'
RUN go build /apps/dispatcher.go

FROM alpine

RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/static .'

EXPOSE 80
CMD ["/apps/dispatcher"]
COPY --from=builder /go/dispatcher .
RUN chmod +x /apps/dispatcher

RUN /bin/sh -c 'ls /apps'
RUN /bin/sh -c 'ls /'
