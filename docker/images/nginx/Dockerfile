ARG BASE_IMAGE=drupalwxt/site-wxt:latest
FROM $BASE_IMAGE as src

FROM nginx:alpine

COPY --from=src /var/www/html /var/www/html

# Configure nginx
COPY docker/conf/nginx.conf /etc/nginx/nginx.conf
# Remove default server definition
RUN rm /etc/nginx/conf.d/default.conf
# Make sure files/folders needed by the processes are accessable when they run under the nobody user
RUN chown -R nobody.nobody /run && \
  chown -R nobody.nobody /var/lib/nginx && \
  chown -R nobody.nobody /var/tmp/nginx && \
  chown -R nobody.nobody /var/log/nginx
