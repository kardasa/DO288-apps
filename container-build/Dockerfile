# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL 	io.k8s.descrition="A basic Apache HTTP Server child image, usese ONBUILD" \
	io.k8s.dsiplay-name="Apache HTTP Server" \
	io.openshift.tags="httpd, apache" \
	io.openshift.expose-services="8000:http"


RUN sed -i "/s/Listen 80/Listen 8000/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001

EXPOSE 8000
