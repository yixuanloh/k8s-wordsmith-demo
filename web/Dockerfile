# RUN
FROM alpine

EXPOSE 80
CMD ["/web"]

WORKDIR /apps
COPY web/github.com/yixuanloh/k8s-wordsmith-demo/web/@v/v1.2.0.zip .
RUN unzip /apps/v1.2.0.zip

