Dockerfile
----------
 FROM ubuntu:20.04
 ENV DEBIAN_FRONTEND=noninteractive
 RUN apt-get update && \
       apt-get install -y apache2 \
       && apt-get clean \
       && rm -rf /var/lib/apt/lists/*
COPY ./html/ /var/www/html/
RUN chown -R www-data:www-data /var/www/html
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]
