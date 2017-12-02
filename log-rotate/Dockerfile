FROM alpine:3.7

RUN apk update && \
  apk add logrotate && \
  rm -rf /tmp/* /var/cache/apk/*

COPY logrotate.txt /etc/logrotate.conf

# execute logrotate every 12 hours
CMD ["watch", "-n", "43200", "logrotate", "-v", "/etc/logrotate.conf"]