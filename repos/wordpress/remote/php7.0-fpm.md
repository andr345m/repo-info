## `wordpress:php7.0-fpm`

```console
$ docker pull wordpress@sha256:8cd90561f7aad89a04a618e8679da00864a894f26f8f967ecc43a53e48fc1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `wordpress:php7.0-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:4843af48c4d54d33c582edd8a6ea19a8177cb76af62274acbef5ef6e27429a54
```

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170003900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a1be6c517610c45804b5b73e3c01ddb8e1e191db29ff23d9a0613cbdf230b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 07 Sep 2017 23:04:40 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Thu, 07 Sep 2017 23:04:41 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 02:37:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2017 02:38:08 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 02:38:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2017 02:38:10 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 08 Sep 2017 03:00:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 08 Sep 2017 03:00:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 03:00:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 03:00:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 08 Sep 2017 03:56:40 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 08 Sep 2017 03:56:40 GMT
ENV PHP_VERSION=7.0.23
# Fri, 08 Sep 2017 03:56:40 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Fri, 08 Sep 2017 03:56:41 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Fri, 08 Sep 2017 03:57:04 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 08 Sep 2017 03:57:04 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 08 Sep 2017 04:01:00 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 08 Sep 2017 04:07:09 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 08 Sep 2017 04:07:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2017 04:07:10 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2017 04:07:11 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 08 Sep 2017 04:07:12 GMT
EXPOSE 9000/tcp
# Fri, 08 Sep 2017 04:07:12 GMT
CMD ["php-fpm"]
# Fri, 08 Sep 2017 11:30:54 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 08 Sep 2017 11:30:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Sep 2017 11:30:55 GMT
VOLUME [/var/www/html]
# Fri, 08 Sep 2017 11:30:56 GMT
ENV WORDPRESS_VERSION=4.8.1
# Fri, 08 Sep 2017 11:30:56 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Fri, 08 Sep 2017 11:30:58 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 08 Sep 2017 11:30:58 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Fri, 08 Sep 2017 11:30:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 11:30:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a924c2479bb6777905f96cfb605b402d9a8021e3176dc0891fed25027369f86`  
		Last Modified: Fri, 08 Sep 2017 05:05:06 GMT  
		Size: 82.5 MB (82494887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e34513d1c6fa28a895a9038631ce0f01eac1112e553e52ec255d08c29ab8586`  
		Last Modified: Fri, 08 Sep 2017 05:04:39 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a257473dde3882fb8eb6dd48b656ae27b7a57a331c9d9c916c134a46ecbb68`  
		Last Modified: Fri, 08 Sep 2017 05:36:10 GMT  
		Size: 12.1 MB (12063053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852e96b9bc24d8b36495602e3126981a84f7ae8d95f523a29b8e8e4b13782345`  
		Last Modified: Fri, 08 Sep 2017 05:36:08 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327f063a45d927da030c82f179bb09560cd134d15f990f1d108d2c04e3f30a19`  
		Last Modified: Fri, 08 Sep 2017 05:36:14 GMT  
		Size: 12.7 MB (12679945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c753a295ae70651aac01c048a3063e6b383b842a741b45f25fe357c60859a2`  
		Last Modified: Fri, 08 Sep 2017 05:36:08 GMT  
		Size: 2.1 KB (2120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21319e8b1742ad3d22ef2036b4ec2cc41bef72d98cf56403bee1d7b56973a662`  
		Last Modified: Fri, 08 Sep 2017 05:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c358ee6112218bc3b06a889df516e2f4b21e561774078f82fd3d9b61c03c484a`  
		Last Modified: Fri, 08 Sep 2017 05:36:08 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc442e1af151537acd32bb20b650c5e67fa31f5304777a543050a58a7e6dea8`  
		Last Modified: Mon, 11 Sep 2017 16:47:48 GMT  
		Size: 2.1 MB (2146797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50278762c764a5493cda367d66a798cc547ad4a77cc0b0cdd80b0e16aa5c2be4`  
		Last Modified: Mon, 11 Sep 2017 16:47:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad03e4c529e042189b07f3d23ea0945b96a4e7262f7cf950601a28b56908b32`  
		Last Modified: Mon, 11 Sep 2017 16:47:52 GMT  
		Size: 8.0 MB (8009543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d68b1422a6abc1ed34fa7a7b2e63f3bf0879669e4f92f11a35289f1942fc16`  
		Last Modified: Mon, 11 Sep 2017 16:47:47 GMT  
		Size: 3.2 KB (3206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.0-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:97319a5bdc46e59dda5bd9778c16953bf041f5d9feabd59a0bb33618c109472c
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147317542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dc5adef37d9e2c5caacd1d45c077c56579c49d255be849884119d96dc92862`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 25 Jul 2017 12:47:49 GMT
ADD file:0448b2cd9da7d0c40fa8f3ee9ac6db219379c4631011ee1495ec8ad66be4f52e in / 
# Tue, 25 Jul 2017 12:47:52 GMT
CMD ["bash"]
# Wed, 26 Jul 2017 01:27:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Wed, 26 Jul 2017 01:34:08 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Wed, 26 Jul 2017 01:34:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Jul 2017 01:34:13 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 29 Jul 2017 12:41:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 29 Jul 2017 12:41:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 29 Jul 2017 12:41:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 29 Jul 2017 12:41:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 29 Jul 2017 14:29:13 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 01 Sep 2017 15:08:40 GMT
ENV PHP_VERSION=7.0.23
# Fri, 01 Sep 2017 15:08:41 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Fri, 01 Sep 2017 15:08:42 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Fri, 01 Sep 2017 15:10:43 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 01 Sep 2017 15:10:44 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 01 Sep 2017 15:36:50 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 01 Sep 2017 15:36:51 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 01 Sep 2017 15:36:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Sep 2017 15:36:53 GMT
WORKDIR /var/www/html
# Fri, 01 Sep 2017 15:36:55 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 01 Sep 2017 15:36:56 GMT
EXPOSE 9000/tcp
# Fri, 01 Sep 2017 15:36:56 GMT
CMD ["php-fpm"]
# Thu, 07 Sep 2017 20:12:13 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Thu, 07 Sep 2017 20:12:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 07 Sep 2017 20:12:16 GMT
VOLUME [/var/www/html]
# Thu, 07 Sep 2017 20:12:17 GMT
ENV WORDPRESS_VERSION=4.8.1
# Thu, 07 Sep 2017 20:12:18 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Thu, 07 Sep 2017 20:12:39 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Thu, 07 Sep 2017 20:12:41 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Thu, 07 Sep 2017 20:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2017 20:12:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5e32d580a9d26e16dd26eaf656c25de16f6fc4a5e2cf51e5d73de3d0b5a0966c`  
		Last Modified: Tue, 25 Jul 2017 13:05:41 GMT  
		Size: 48.7 MB (48691924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff8ce68cf6c0fb7a0df99490754415d5e1e4c666008bf8c720adeb72bb540f8`  
		Last Modified: Sat, 29 Jul 2017 17:09:55 GMT  
		Size: 63.8 MB (63791145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6211db034033589ffed338d2fa542f9cb83e59e8034dfcc1830a2196af0001c`  
		Last Modified: Sat, 29 Jul 2017 17:09:03 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b92a1210b950b0ea57354219d59f93d65de6e42a3f3a7cab6a9cfd05ecbb12`  
		Last Modified: Fri, 01 Sep 2017 16:11:01 GMT  
		Size: 12.3 MB (12288681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d387590a81d76d1124fb6902f4b1a9aa5c9d60166a3a90129e20757109218d2`  
		Last Modified: Fri, 01 Sep 2017 16:10:54 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c8bba1b25b132be761bd1ea0e275833f58212f642c55e49dfdbc2b7b8158d1`  
		Last Modified: Fri, 01 Sep 2017 16:10:57 GMT  
		Size: 12.4 MB (12389891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478b3fc461207690e57b76abb75296a4115e7cbfb30a38a3c1657301ff25386b`  
		Last Modified: Fri, 01 Sep 2017 16:10:51 GMT  
		Size: 2.1 KB (2127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45aaa21224ddee8c1a8abdc2e3902bea9842fa45b0985677835c0180071c501d`  
		Last Modified: Fri, 01 Sep 2017 16:10:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750d0151c188f3421fbd8a6c32f58846c8250371585347c8eb6f902a0649170a`  
		Last Modified: Fri, 01 Sep 2017 16:10:53 GMT  
		Size: 7.7 KB (7680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916cd0cbe0fe7815c3ee93a825d1e611d08fa1a13c15c8a8b8ec93299b7c8d4`  
		Last Modified: Thu, 07 Sep 2017 20:28:07 GMT  
		Size: 2.1 MB (2132076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca754c2f2107b900b9accfc658535b2c0c197c5642f378c4d4fadfc5518917b`  
		Last Modified: Thu, 07 Sep 2017 20:28:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7d875d68292d73847b25a464109f1f97b22241cb6ad2cf5c0068f3200d4fdc`  
		Last Modified: Thu, 07 Sep 2017 20:28:09 GMT  
		Size: 8.0 MB (8009621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156b0f85fbfed21d46ac0d36e705b620c309ba84afc88ff28f43ae47ce9c7a0`  
		Last Modified: Thu, 07 Sep 2017 20:28:04 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.0-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0dd133baeddd185129d2f8d030cdce3713bcdf73ee0de8ed91fff5daea9fa734
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149213074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6dcea395e48e5a8ce859dc38e163a51a54e18466ddb9c1ba2beb4e8c111b4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 23:36:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2017 23:39:13 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 23:39:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2017 23:39:17 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 08 Sep 2017 23:58:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 08 Sep 2017 23:58:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 23:58:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 23:58:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 09 Sep 2017 00:31:07 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Sat, 09 Sep 2017 00:31:09 GMT
ENV PHP_VERSION=7.0.23
# Sat, 09 Sep 2017 00:31:10 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Sat, 09 Sep 2017 00:31:12 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Sat, 09 Sep 2017 00:31:57 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Sat, 09 Sep 2017 00:31:59 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Sat, 09 Sep 2017 00:38:57 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Sat, 09 Sep 2017 00:38:59 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Sat, 09 Sep 2017 00:38:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 09 Sep 2017 00:39:00 GMT
WORKDIR /var/www/html
# Sat, 09 Sep 2017 00:39:02 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 09 Sep 2017 00:39:03 GMT
EXPOSE 9000/tcp
# Sat, 09 Sep 2017 00:39:03 GMT
CMD ["php-fpm"]
# Sat, 09 Sep 2017 04:00:19 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Sat, 09 Sep 2017 04:00:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 09 Sep 2017 04:00:22 GMT
VOLUME [/var/www/html]
# Sat, 09 Sep 2017 04:00:23 GMT
ENV WORDPRESS_VERSION=4.8.1
# Sat, 09 Sep 2017 04:00:24 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Sat, 09 Sep 2017 04:00:31 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sat, 09 Sep 2017 04:00:32 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Sat, 09 Sep 2017 04:00:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Sep 2017 04:00:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ce2ee409521cc41fb7b4a0f2b1afb85e1f4e0866aa17193d1c6fe2f05b84a3`  
		Last Modified: Sat, 09 Sep 2017 01:20:46 GMT  
		Size: 64.6 MB (64611190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8673d63cbfe1fbf0b951a59b088c845b7d04f9084298af89c958da9faf363396`  
		Last Modified: Sat, 09 Sep 2017 01:20:21 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871a3f11655445c2dbdfbf4d29711143a1a4b415c21e1b4c5ac40981dba89b42`  
		Last Modified: Sat, 09 Sep 2017 01:25:01 GMT  
		Size: 12.3 MB (12288198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5893f85baa34f0ec83fe05a3918bf099ce851800f489734d5f90bae8a7dae5af`  
		Last Modified: Sat, 09 Sep 2017 01:24:57 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da84f41daecc14b895664df69ce3e63e17aa22175f4be7619bc89f2943a87fd`  
		Last Modified: Sat, 09 Sep 2017 01:25:02 GMT  
		Size: 12.1 MB (12052365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef2d152f18b5ee6d0c2f07aa4b4adee511391801c2be73fd520e6585ec36410`  
		Last Modified: Sat, 09 Sep 2017 01:24:57 GMT  
		Size: 2.1 KB (2124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44107d6d49199ac3b38c093dd3c174f66d2be834b74996f1273a0945f3cc5afc`  
		Last Modified: Sat, 09 Sep 2017 01:24:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03dd8fad18464b512d6dee16f34a99724a3c8cb2af89885c23678c964b8be782`  
		Last Modified: Sat, 09 Sep 2017 01:24:56 GMT  
		Size: 7.7 KB (7673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f46a4cac8f6d3d334f119489b7626236d07615bc651d408e973e1e5055751dd`  
		Last Modified: Sat, 09 Sep 2017 04:11:01 GMT  
		Size: 2.3 MB (2308064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9418a36a6260c254d90346fbfeaf9ac9da749b9b4d61992b46986dc935779844`  
		Last Modified: Sat, 09 Sep 2017 04:11:00 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621012c343a607c443f943a1f3b753ca3526818b2f39374400f7dc8ce5ef6fd0`  
		Last Modified: Sat, 09 Sep 2017 04:11:03 GMT  
		Size: 8.0 MB (8009624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1407748b5cb0e50d631dad7cc1ca81053eda54de5bed4e429873eee563ca25e3`  
		Last Modified: Sat, 09 Sep 2017 04:10:59 GMT  
		Size: 3.2 KB (3221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.0-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:37a976837d13c48c7ccdf1274ff26b9c753e9f6bea4047d31a858145ebd4af8d
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172576853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e844c362164112c36c66a8085f81bb04ac8030232ae1e3b8e250c51d0c7d019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Sep 2017 13:17:52 GMT
ADD file:e02edf114d3ee3a58b6c6729d41261abc361f69333d3b08c7c730572fd6c1874 in / 
# Fri, 08 Sep 2017 13:17:52 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:42:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2017 15:43:33 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:43:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2017 15:43:34 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 08 Sep 2017 15:58:56 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 08 Sep 2017 15:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 15:58:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 15:58:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 08 Sep 2017 16:27:10 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 08 Sep 2017 16:27:10 GMT
ENV PHP_VERSION=7.0.23
# Fri, 08 Sep 2017 16:27:11 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Fri, 08 Sep 2017 16:27:11 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Fri, 08 Sep 2017 16:28:04 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 08 Sep 2017 16:28:04 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 08 Sep 2017 16:34:37 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 08 Sep 2017 16:35:02 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 08 Sep 2017 16:35:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2017 16:35:03 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2017 16:35:03 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 08 Sep 2017 16:35:04 GMT
EXPOSE 9000/tcp
# Fri, 08 Sep 2017 16:35:04 GMT
CMD ["php-fpm"]
# Fri, 08 Sep 2017 17:57:27 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 08 Sep 2017 17:57:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Sep 2017 17:57:29 GMT
VOLUME [/var/www/html]
# Fri, 08 Sep 2017 17:57:29 GMT
ENV WORDPRESS_VERSION=4.8.1
# Fri, 08 Sep 2017 17:57:29 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Fri, 08 Sep 2017 17:57:32 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 08 Sep 2017 17:57:32 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Fri, 08 Sep 2017 17:57:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 17:57:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f611f84acffe6a66fad3356eb9101ed9fff54e980701079bbce3ee4826ccd3ae`  
		Last Modified: Fri, 08 Sep 2017 13:22:33 GMT  
		Size: 52.8 MB (52773126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79b0c6e6c0af331a9399924d3d78ed076049dca893469ce8512cd3d173708f6`  
		Last Modified: Fri, 08 Sep 2017 17:16:02 GMT  
		Size: 83.9 MB (83883283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7374d46215ae1d83309d33a1f57a658d05346f2983de18430fe1d3cca2f3bfb7`  
		Last Modified: Fri, 08 Sep 2017 17:15:31 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34ebc4d28eda624bb65e3eef0bb6dffbcb3ed06957ba23d779457bf440621e8`  
		Last Modified: Fri, 08 Sep 2017 17:19:24 GMT  
		Size: 12.3 MB (12289447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c889a3bdc95ceaae0f1672c415425634cd788a24acedb649a607c65265d2e993`  
		Last Modified: Fri, 08 Sep 2017 17:19:23 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be364b4f8d1108f01e9bd56e2457dc3e7ed8e4c5f1e8fa5930fc402c52749a7a`  
		Last Modified: Fri, 08 Sep 2017 17:19:27 GMT  
		Size: 13.3 MB (13311600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931353aaaca9e2b77a57df2f7b3bdfeed78cf40a57470d263e3c96ae3bc11b2b`  
		Last Modified: Fri, 08 Sep 2017 17:19:23 GMT  
		Size: 2.1 KB (2124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bc6dd8dae352533530932cbfb4b64c39e73b40c048f876bb3d833c4edb3f6a`  
		Last Modified: Fri, 08 Sep 2017 17:19:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0342a14bbcb8431af61c9edee006e01f9115e81e2f6c38eca8bdce925d0a263e`  
		Last Modified: Fri, 08 Sep 2017 17:19:23 GMT  
		Size: 7.7 KB (7676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5397d6c9dbae3eefbe263098c458536c77687cf86d54ac62b1dbd8f3daee9e`  
		Last Modified: Fri, 08 Sep 2017 18:05:38 GMT  
		Size: 2.3 MB (2295665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb1c662c0547e798d7b81529905dd7ab766aacc437510a3391c58bb308e631`  
		Last Modified: Fri, 08 Sep 2017 18:05:38 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca4d795ca0aba4eaaa4b2c8bf784ef23fd71bb5af6f30d4d398e1bee86f5a1`  
		Last Modified: Fri, 08 Sep 2017 18:05:40 GMT  
		Size: 8.0 MB (8009546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cb6bd1fa4095cd3fa8f94c5143be1a285a6f4fe2983944bd3dd88b393fdff7`  
		Last Modified: Fri, 08 Sep 2017 18:05:38 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.0-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:8a668ee9d0ffe067f33c9fbeca52147860f46120e34424ee8ba42f7784645895
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157287667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639a9908c13072c443340616a4d0cc52bb2f55b69c8a1a8f34b113991c666bca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:48:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2017 01:49:18 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:49:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2017 01:49:19 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 08 Sep 2017 01:56:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 08 Sep 2017 01:56:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 01:56:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 01:56:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 08 Sep 2017 02:12:15 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 08 Sep 2017 02:12:15 GMT
ENV PHP_VERSION=7.0.23
# Fri, 08 Sep 2017 02:12:15 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Fri, 08 Sep 2017 02:12:15 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Fri, 08 Sep 2017 02:12:37 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 08 Sep 2017 02:12:37 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 08 Sep 2017 02:15:24 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 08 Sep 2017 02:15:24 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 08 Sep 2017 02:15:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2017 02:15:25 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2017 02:15:25 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 08 Sep 2017 02:15:26 GMT
EXPOSE 9000/tcp
# Fri, 08 Sep 2017 02:15:26 GMT
CMD ["php-fpm"]
# Fri, 08 Sep 2017 03:12:29 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 08 Sep 2017 03:12:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Sep 2017 03:12:30 GMT
VOLUME [/var/www/html]
# Fri, 08 Sep 2017 03:12:30 GMT
ENV WORDPRESS_VERSION=4.8.1
# Fri, 08 Sep 2017 03:12:30 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Fri, 08 Sep 2017 03:12:34 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 08 Sep 2017 03:12:34 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Fri, 08 Sep 2017 03:12:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 03:12:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dcfe91b8601953aafd744d3b843930c543043e6685df075ee8e09cea485fcb`  
		Last Modified: Fri, 08 Sep 2017 02:35:19 GMT  
		Size: 70.0 MB (69977302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f39d9a27644155d78cc51a93b3a444e99fce2906b6659cff0fb8b86cc4bcb1`  
		Last Modified: Fri, 08 Sep 2017 02:34:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac172de2c9af029b49c148a1d3414b0e6f5aad1e7e446ffbe891f0fcf9f5435b`  
		Last Modified: Fri, 08 Sep 2017 02:38:49 GMT  
		Size: 12.3 MB (12287771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad21f81bcae9e4fc66bda3dc1e96246d0e6aac2608dba9609c7bea341895fcf`  
		Last Modified: Fri, 08 Sep 2017 02:38:45 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4412fae3c7b860cabf45d4506cd8c9951d7343fd74e6fb8072e01117782e2ea7`  
		Last Modified: Fri, 08 Sep 2017 02:38:49 GMT  
		Size: 12.8 MB (12804696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939e39a0bebdbbb04c5f75e3fc71b26045b20ae126afee32b662a2dff849b483`  
		Last Modified: Fri, 08 Sep 2017 02:38:45 GMT  
		Size: 2.1 KB (2124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c6a267fab9b01ac9229fa7e54a56bc1a2b71faeaa245f76eeba74504647f88`  
		Last Modified: Fri, 08 Sep 2017 02:38:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c79071ee209ea84bca158a9018cc937b1f23015b7319acc94b1bd4782cf1a7`  
		Last Modified: Fri, 08 Sep 2017 02:38:45 GMT  
		Size: 7.7 KB (7678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2dd7e1539b3425aada1ffbe01dcec0eedd81a058fe5503e63dcdad900a81ab`  
		Last Modified: Fri, 08 Sep 2017 03:19:11 GMT  
		Size: 2.4 MB (2384415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f31a31ee5a3c380b096fa212e4aea5c31fee2e1fe5ad255c2c3a603157f0226`  
		Last Modified: Fri, 08 Sep 2017 03:19:10 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b930a935872b71f4a548c3c84701cc79659ceed8430673b02c3f860957cf0a5`  
		Last Modified: Fri, 08 Sep 2017 03:19:12 GMT  
		Size: 8.0 MB (8009670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4128df1b3d62e36f1895e592ca22ed724044f30d0debbd4a4885f6bef717a0`  
		Last Modified: Fri, 08 Sep 2017 03:19:10 GMT  
		Size: 3.2 KB (3221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.0-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:4ba960b8725f199d95f049b31d5034783957e2cce7baa68453a5a17ef07f4b00
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153141238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482413a4955a67a997da13ed058b2e3c4999683cd4bf20469c7c78fd3ea4a989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:18:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		libpcre3-dev 		make 		pkg-config 		re2c
# Fri, 08 Sep 2017 06:19:14 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 06:19:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Sep 2017 06:19:15 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Fri, 08 Sep 2017 06:25:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Fri, 08 Sep 2017 06:25:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 06:25:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 06:25:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 08 Sep 2017 06:38:38 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 08 Sep 2017 06:38:39 GMT
ENV PHP_VERSION=7.0.23
# Fri, 08 Sep 2017 06:38:39 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.23.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.23.tar.xz.asc/from/this/mirror
# Fri, 08 Sep 2017 06:38:39 GMT
ENV PHP_SHA256=8e526e3551a58e00c8055fa4a72804aa1bd3ee1c0411b25bf1504cc4992609df PHP_MD5=
# Fri, 08 Sep 2017 06:38:55 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 08 Sep 2017 06:38:55 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 08 Sep 2017 06:41:57 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 08 Sep 2017 06:41:58 GMT
COPY multi:1401feee8064a06ad514519ec870939c946ecfdf381c82a90cb2035486938ee9 in /usr/local/bin/ 
# Fri, 08 Sep 2017 06:41:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2017 06:41:58 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2017 06:41:59 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 08 Sep 2017 06:41:59 GMT
EXPOSE 9000/tcp
# Fri, 08 Sep 2017 06:41:59 GMT
CMD ["php-fpm"]
# Fri, 08 Sep 2017 07:32:07 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 08 Sep 2017 07:32:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 08 Sep 2017 07:32:08 GMT
VOLUME [/var/www/html]
# Fri, 08 Sep 2017 07:32:08 GMT
ENV WORDPRESS_VERSION=4.8.1
# Fri, 08 Sep 2017 07:32:08 GMT
ENV WORDPRESS_SHA1=5376cf41403ae26d51ca55c32666ef68b10e35a4
# Fri, 08 Sep 2017 07:32:10 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 08 Sep 2017 07:32:11 GMT
COPY file:db1f48c4963a4352b4c31c18f102b71fcc06a1266db6edd17f8f52458fe13130 in /usr/local/bin/ 
# Fri, 08 Sep 2017 07:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 07:32:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701b1d6891093c664aafb5ddded8b897bab2678b49b4c39ed152c86139e3b472`  
		Last Modified: Fri, 08 Sep 2017 06:58:03 GMT  
		Size: 64.0 MB (63977876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477fee1ce9a2412b1abf6eb058badc7a59941c997bf3c5764c47e9f3d51e2f0`  
		Last Modified: Fri, 08 Sep 2017 06:57:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fd194ae6008f443d18934e2518b60e87567aba08d9fdad7d2b88c47565f09c`  
		Last Modified: Fri, 08 Sep 2017 06:59:29 GMT  
		Size: 12.3 MB (12287657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e1231b6efc5b64c34073f2ed51d14e2451fa7a82b091263d2e8790f1b299fd`  
		Last Modified: Fri, 08 Sep 2017 06:59:27 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650a5d109ab2827529245231b29aa89f0a1b350e736fee6652337e73a334356d`  
		Last Modified: Fri, 08 Sep 2017 06:59:30 GMT  
		Size: 13.4 MB (13405756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e78101cc7efd0c06f45eb9d741678d19b61374e20ba3802628de984298c9b44`  
		Last Modified: Fri, 08 Sep 2017 06:59:27 GMT  
		Size: 2.1 KB (2123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a40b9d093a7381e2a73206bf9955bc64f5d902e5c4b018776f93a5e04a56ed2`  
		Last Modified: Fri, 08 Sep 2017 06:59:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b3df382f651f1dca0a0d77e02392894fb2d4af0e742e230cdebf8444b18f1e`  
		Last Modified: Fri, 08 Sep 2017 06:59:27 GMT  
		Size: 7.7 KB (7676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e824edbe5f21e7d6974b7b480481116187efbb6b025cfb1f7381dcd2ed683347`  
		Last Modified: Fri, 08 Sep 2017 07:35:39 GMT  
		Size: 2.7 MB (2657342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cd52e3ae2323f6a92efe1769015dd44d690b234dde4e71640e357c1cd184ac`  
		Last Modified: Fri, 08 Sep 2017 07:35:38 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193811bbfbbc5cc6eed50a70c04aba2358a47c9208c778edc15fbb6a872c188`  
		Last Modified: Fri, 08 Sep 2017 07:35:41 GMT  
		Size: 8.0 MB (8009624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ef8aa050d5ff71316af17cabeba72227f80cd2ae0154e1a4155be4d4a210e9`  
		Last Modified: Fri, 08 Sep 2017 07:35:38 GMT  
		Size: 3.2 KB (3221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
