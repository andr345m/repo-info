## `joomla:apache`

```console
$ docker pull joomla@sha256:2e6d8f474a4be21634df26a5e8ea2ae8a3ba85b7506bb3d9a23cb625bf43458a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `joomla:apache` - linux; amd64

```console
$ docker pull joomla@sha256:51c0e52e3ed2f795162cb7fa373c0c4bea687c4f814cb332cc55908f9774aae2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171889012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a743beef6fd1a76ee8622541951ddd2bc48090eebc6021a6d7b49bfaa95b11b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Fri, 08 Sep 2017 02:50:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		apache2 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 02:51:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Sep 2017 02:51:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Sep 2017 02:51:31 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Fri, 08 Sep 2017 02:51:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 08 Sep 2017 02:51:34 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Fri, 08 Sep 2017 02:51:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 08 Sep 2017 02:51:35 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 08 Sep 2017 02:51:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Fri, 08 Sep 2017 02:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 02:51:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Fri, 08 Sep 2017 02:51:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Fri, 08 Sep 2017 04:19:30 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Fri, 08 Sep 2017 04:19:31 GMT
ENV PHP_VERSION=5.6.31
# Fri, 08 Sep 2017 04:19:31 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.31.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.31.tar.xz.asc/from/this/mirror
# Fri, 08 Sep 2017 04:19:32 GMT
ENV PHP_SHA256=c464af61240a9b7729fabe0314cdbdd5a000a4f0c9bd201f89f8628732fe4ae4 PHP_MD5=
# Fri, 08 Sep 2017 04:20:01 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg2 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Fri, 08 Sep 2017 04:20:02 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Fri, 08 Sep 2017 04:24:42 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)" 	&& if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi 	&& ./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pcre-regex=/usr 		--with-libdir="lib/$debMultiarch" 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& cd / 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps 		&& pecl update-channels 	&& rm -rf /tmp/pear ~/.pearrc
# Fri, 08 Sep 2017 04:24:43 GMT
COPY multi:3775aa35856908376b7ea71c79fad1e546e92e4ef56dcfc5821b2cc6e2ed6cdc in /usr/local/bin/ 
# Fri, 08 Sep 2017 04:24:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Sep 2017 04:24:44 GMT
COPY file:24613ecbb1ce6a09f683b0753da9c26a1af07547326e8a02f6eec80ad6f2774a in /usr/local/bin/ 
# Fri, 08 Sep 2017 04:24:44 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2017 04:24:45 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 04:24:45 GMT
CMD ["apache2-foreground"]
# Wed, 13 Sep 2017 01:19:02 GMT
MAINTAINER Michael Babker <michael.babker@joomla.org> (@mbabker)
# Wed, 13 Sep 2017 01:19:02 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 13 Sep 2017 01:19:03 GMT
RUN a2enmod rewrite
# Wed, 13 Sep 2017 01:19:40 GMT
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libmcrypt-dev zip unzip && rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd
# Wed, 13 Sep 2017 01:19:48 GMT
RUN docker-php-ext-install mysqli
# Wed, 13 Sep 2017 01:19:55 GMT
RUN docker-php-ext-install mcrypt
# Wed, 13 Sep 2017 01:20:14 GMT
RUN docker-php-ext-install zip
# Wed, 13 Sep 2017 01:20:15 GMT
VOLUME [/var/www/html]
# Wed, 13 Sep 2017 01:20:15 GMT
ENV JOOMLA_VERSION=3.7.5
# Wed, 13 Sep 2017 01:20:15 GMT
ENV JOOMLA_SHA1=4a8ba6c70265879cf5c77bcc1b3a0fe9620ba02a
# Wed, 13 Sep 2017 01:20:21 GMT
RUN curl -o joomla.zip -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.zip 	&& echo "$JOOMLA_SHA1 *joomla.zip" | sha1sum -c - 	&& mkdir /usr/src/joomla 	&& unzip joomla.zip -d /usr/src/joomla 	&& rm joomla.zip 	&& chown -R www-data:www-data /usr/src/joomla
# Wed, 13 Sep 2017 01:20:21 GMT
COPY file:27ca5c0b8509d6681e80aa6cd05b2e2e68da2f59fb0ee7fa2aa581f55d362b6d in /entrypoint.sh 
# Wed, 13 Sep 2017 01:20:21 GMT
COPY file:7328ebe063e26f7b7716dfd8778bb7d46b90702ea38b23b9147ba2fd837ac2c1 in /makedb.php 
# Wed, 13 Sep 2017 01:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Sep 2017 01:20:22 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:02ffa64ac1d4100965fdab1cb78896787937def3ac6e334e0599325563d946aa`  
		Last Modified: Fri, 08 Sep 2017 05:32:23 GMT  
		Size: 2.8 MB (2784936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e287078ab3e5cedce81066c35d7202dbe85c5ed7b06f994ea282a4a2f2eb197d`  
		Last Modified: Fri, 08 Sep 2017 05:32:21 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa908359a8ab8fdc571f9f235057a85b57e1d9f3638136b00aa56e15e68f6f8b`  
		Last Modified: Fri, 08 Sep 2017 05:32:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da80a4729d52be4f51c2f78d2cb9ee332f747c22d66a2f8b2e29941b87fbd717`  
		Last Modified: Fri, 08 Sep 2017 05:32:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892d5ce128a6e695fe5b770feb07ccf9d67524bfa28fa890d2ab7e3c771cba9a`  
		Last Modified: Fri, 08 Sep 2017 05:32:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38986916ae3ed831d8d3872e1a9b78557434b224dc9114e0b81f57a530bccadf`  
		Last Modified: Fri, 08 Sep 2017 05:38:45 GMT  
		Size: 12.6 MB (12588478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092c16c9a5a4f3e6f44c3e230c7c18a229e09c1b16aa6a759c7e400f7c834b6a`  
		Last Modified: Fri, 08 Sep 2017 05:38:42 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a221d2639d9f19a2c764ae6b9b83b21c36ac7dbf6f3a2a6851f5809d44e4e51`  
		Last Modified: Fri, 08 Sep 2017 05:38:45 GMT  
		Size: 9.2 MB (9175350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9cd61771d9cc635907e760e071085297b1d58ed4bf4849de7b17a5b2970756`  
		Last Modified: Fri, 08 Sep 2017 05:38:41 GMT  
		Size: 2.1 KB (2122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07fb6a4fe548b039400196fd92095a8b7ffd7d96a5425789247b238eb239ed0`  
		Last Modified: Fri, 08 Sep 2017 05:38:41 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20d55db4ab0a46686afe97fefbf522f21a3cfbc2fd7c7c77f26cf85ea4f594d`  
		Last Modified: Wed, 13 Sep 2017 01:24:59 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e92fd676cebc733b1d98b0ea3793893c0cacafdf08c971f473504c31c7e471`  
		Last Modified: Wed, 13 Sep 2017 01:24:59 GMT  
		Size: 3.0 MB (3001629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ba77d2cb680b3b4c86a4d79c3dff3391c06df4453192466d7bfdd61945b553`  
		Last Modified: Wed, 13 Sep 2017 01:24:58 GMT  
		Size: 58.0 KB (57992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c62ef48ed94c7b6bc0f4c3d8a8d29a1a0e6c2080544c45c96a67b116daba98`  
		Last Modified: Wed, 13 Sep 2017 01:24:55 GMT  
		Size: 19.7 KB (19699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e0251dab2570c0d4031db1ade8490e05c6a263e4243fd6dc64d98d120ca12`  
		Last Modified: Wed, 13 Sep 2017 01:24:57 GMT  
		Size: 63.4 KB (63397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f1fcd0a02d7f682820bf86aab5473ce40836971edb48cff5eded9533f531b7`  
		Last Modified: Wed, 13 Sep 2017 01:25:02 GMT  
		Size: 9.1 MB (9098962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcf0c43668afd3cd647f4162ef1a15fd656e551398fe60307cc6b6263b2984`  
		Last Modified: Wed, 13 Sep 2017 01:24:56 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2932c573062fd15e6eb6897b0b49cf528fc54be59c0a816d0a280d670609aa`  
		Last Modified: Wed, 13 Sep 2017 01:24:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
