# RUN
FROM alpine

WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip

WORKDIR /apps/static
RUN /bin/sh -c 'ls /apps'
RUN /bin/sh -c 'ls /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0'
RUN /bin/sh -c 'cp /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/static /apps/static'

RUN chmod +x /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/web
EXPOSE 80
CMD ["/apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/web"]
