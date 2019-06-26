FROM httpd:2.4.37-alpine
# RUN apk update; \
#    apk upgrade; 

# Copy apache vhost file to proxy php requests to php-fpm container

COPY demo.apache.conf /usr/local/apache2/conf/demo.apache.conf
RUN echo "Include /usr/local/apache2/conf/demo.apache.conf" \
	>> /usr/local/apache2/conf/httpd.conf

# Comment if you want to download and install wordpress
# CONTINUE HERE
# ADD ${WORDPRESS_FILE} ${WEB_DESTINATION_PATH} 
# RUN tar -xzvf ${WEB_DESTINATION_PATH}/latest.tar.gz 
# RUN mv /var/www/html/wordpress/* /var/www/html/
# RUN rm -r /var/www/html/wordpress 
# RUN rm /var/www/html/latest.tar.gz 

COPY wp-config-sample.php /var/www/html/wp-config.php

# RUN cd ${WEB_DESTINATION_PATH} 
# RUN sed "s/database_name_here/${DB_NAME}/g" wp-config.php 
# RUN sed "s/username_here/${DB_USERNAME}/g" wp-config.php 
# RUN sed "s/password_here/${DB_PASSWORD}/g" wp-config.php 
# RUN sed "s/localhost/${DB_HOST}/g" wp-config.php 
