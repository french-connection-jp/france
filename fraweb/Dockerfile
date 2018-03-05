FROM nginx
MAINTAINER ngzm<nk.ngzm@gmail.com>
RUN cd /etc/nginx/conf.d && cp -p default.conf default.conf.org
ADD default.conf /etc/nginx/conf.d/
ADD ssl.conf /etc/nginx/conf.d/
RUN mkdir /etc/nginx/ssl
ADD dhparam.pem /etc/nginx/ssl/
ADD index.html 50x.html 404.html /usr/share/nginx/html/
#
# Add application's conf file
#
ADD hamcco.conf /etc/nginx/conf.d/
ADD uploader.conf /etc/nginx/conf.d/
ADD glink.conf /etc/nginx/conf.d/
