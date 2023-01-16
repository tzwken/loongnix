PHP5.6.40-fpm by alpine-3.11
  1. https://hub.docker.com/repository/docker/tzwken/php-fpm5/general
  2. 基于官方php-5.6.40编译，支持pcre-jit(源码有修改增加对loongarch64的实别)。其它拓展可使用pecl进行安装。
  3. 使用到ssl的模块需要手动编译，切换到模块所在目录执行如下命令
  
     phpize
  
     export PKG_CONFIG_PATH=/usr/local/ssl/lib/pkgconfig
     
     pkg-config --cflags --libs libssl
     
     ./configure --with-php-config=/usr/local/bin/php-config --with-openssl-dir=/usr/local/ssl
     
     make && make install

   4. FIX intl拓展编译报错误问题处理。新镜像已集成此模块。
