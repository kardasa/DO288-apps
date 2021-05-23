# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.openshift.expose-services="http:8080" \
      io.k8s.display-name="Apache httpd Server" \
      io.k8s.description="Basic WWW server" \
      io.openshit.tags="apache, httpd, www"

EXPOSE 8080

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chown u=g /var/log/httpd /var/run/httpd

USER 1001

