PHP5.6.40-fpm by alpine-3.11
  docker images  https://hub.docker.com/repository/docker/tzwken/php-fpm5/general
  基于官方php-5.6.40编译，支持pcre-jit。其它拓展可使用pecl进行安装。
  注：
     使用到ssl的模块需要手动编译,切换到模块所在目录执行如下命令
     phpize
     export PKG_CONFIG_PATH=/usr/local/ssl/lib/pkgconfig
     pkg-config --cflags --libs libssl
     ./configure --with-php-config=/usr/local/bin/php-config --with-openssl-dir=/usr/local/ssl
     make && make install
