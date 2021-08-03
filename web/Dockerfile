FROM alpine

WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip

RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/dispatcher.go .'
RUN /bin/sh -c 'cp -r /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/static .'
RUN chmod +x /apps/web

RUN /bin/sh -c 'go build /apps/dispatcher.go'

EXPOSE 80
CMD ["/apps/dispatcher"]
