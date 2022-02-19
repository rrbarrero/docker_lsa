FROM nginx:1.21.6

RUN mkdir -p /app/ssl/ && \
  openssl req -x509 -nodes -days 3650 -newkey rsa:2048 \
  -subj /CN=comunidadlsa.es \
  -keyout /app/ssl/nginx.key -out /app/ssl/nginx.crt

COPY nginx.conf /etc/nginx/conf.d/default.conf
