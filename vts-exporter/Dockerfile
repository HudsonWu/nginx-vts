FROM sophos/nginx-vts-exporter


ENV NGINX_HOST "http://nginx"
ENV NGINX_STATUS "http://nginx/status/format/json"
ENV METRICS_ENDPOINT "/metrics"
ENV METRICS_ADDR ":9913"
ENV DEFAULT_METRICS_NS "nginx"

ENTRYPOINT ["docker-entrypoint.sh"]

EXPOSE 9913
