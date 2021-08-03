FROM golang:alpine as builder
WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip
RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/dispatcher.go .'
RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/static .'
RUN go build /apps/dispatcher.go
RUN /bin/sh -c 'ls /apps'


FROM alpine
EXPOSE 80
CMD ["/apps/dispatcher"]

RUN /bin/sh -c 'ls /apps'
RUN /bin/sh -c 'ls /'
