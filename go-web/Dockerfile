FROM golang:1.13-alpine3.10 as builder

COPY *.go /app/

RUN cd /app && go build -o hellogo .


FROM alpine:3.10

RUN apk update && \
    apk --no-cache add tzdata ca-certificates && \
    cp -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    rm -rf /var/cache/apk/*

COPY --from=builder /app/hellogo /hellogo

CMD ["/hellogo"] 