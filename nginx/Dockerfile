FROM xcgd/nginx-vts

COPY nginx.conf /etc/nginx/

# 更换源，从dl-cdn.alpinelinux.org更换到aliyun source
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/' /etc/apk/repositories

RUN apk update && apk add curl bash tree tzdata && \
    cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash \
    && adduser -D -H -u 1000 -s /bin/bash www-data


EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
