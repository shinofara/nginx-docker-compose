FROM wordpress:4.5.2-fpm

ENV WORDPRESS_TAR_FILE wordpress-4.5.2-ja.tar.gz
ENV WORDPRESS_SHA1 bab94003a5d2285f6ae76407e7b1bbb75382c36e

RUN rm -fr /usr/src/wordpress \
&& curl -o ${WORDPRESS_TAR_FILE} -SL https://ja.wordpress.org/${WORDPRESS_TAR_FILE} \
&& echo "0ca6bba086c6a7efc025f12d49c729de ${WORDPRESS_TAR_FILE}" | md5sum -c \
&& tar -xzf ${WORDPRESS_TAR_FILE} -C /usr/src/ \
&& rm ${WORDPRESS_TAR_FILE} \
&& chown -R www-data:www-data /usr/src/wordpress

VOLUME /var/www/html
