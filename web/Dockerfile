# RUN
FROM alpine

WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip

WORKDIR /apps/static/
RUN ["ls /apps/"]
RUN ["ls /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0"]
RUN ["cp github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/static/ /apps/static/"]

RUN chmod +x /apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/web
EXPOSE 80
CMD ["/apps/github.com/yixuanloh/k8s-wordsmith-demo/web@v1.2.0/web"]
