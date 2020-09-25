FROM php:7.4-fpm

# 工作目录
VOLUME ["/var/www"]

# 删除apt相关缓存
RUN rm -rf /var/lib/apt/list/*

# 安装相关依赖
## apt-get
## docker-php-ext-install
## pecl
RUN apt-get update -y

# php配置
RUN ln -s /var/www/${WORKSPACES}/docker_conf/php/php.ini /usr/local/etc/php \
    && rm -rf /usr/local/lib/php/extensions/no-debug-non-zts-20160303 \
    && ln -s /var/www/${PROJECT_NAME}/${WORKSPACES}/php/no-debug-non-zts-20160303 /usr/local/lib/php/extensions/
