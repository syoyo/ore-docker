FROM syoyo/ubuntu-gcc48
MAINTAINER Syoyo Fujita "syoyo@lighttransport.com"

RUN apt-get -y install wget
RUN apt-get -y install libpcre3-dev
RUN apt-get -y install libssl-dev

RUN wget http://nginx.org/download/nginx-1.4.6.tar.gz
RUN tar -zxvf nginx-1.4.6.tar.gz
RUN (cd nginx-1.4.6; ./configure --with-http_ssl_module && make && make install)
RUN echo "daemon off;" >> /usr/local/nginx/conf/nginx.conf

EXPOSE 80

CMD ["/usr/local/nginx/sbin/nginx"]
