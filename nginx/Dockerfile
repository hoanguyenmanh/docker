FROM ubuntu
MAINTAINER Hoa Nguyen <mozose@gmail.com>

# Install Nginx
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:nginx/stable
RUN apt-get update && apt-get install -y \
    vim \
    wget \
    dialog \
    net-tools \
    nginx \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir -p /data
VOLUME /data
EXPOSE 80
EXPOSE 443

RUN echo "daemon off;" >> /etc/nginx/nginx.conf
CMD service nginx start