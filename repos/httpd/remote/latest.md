## `httpd:latest`

```console
$ docker pull httpd@sha256:7cebd11a0d5309c53202ed9e36e4704a6a38d8fe732742305a4aebfa975a21e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `httpd:latest` - linux; amd64

```console
$ docker pull httpd@sha256:01b66708dffb8a44198267dd346193cb2b0dac964df588fc3c90df1bd9dc925f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68877780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4e03d65aa3697d448050d15ecc13aae5688a1289593977a66f91fea884e539`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 07 Sep 2017 23:04:40 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Thu, 07 Sep 2017 23:04:41 GMT
CMD ["bash"]
# Thu, 07 Sep 2017 23:04:47 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 13 Sep 2017 00:56:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 13 Sep 2017 00:56:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2017 00:56:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Wed, 13 Sep 2017 00:56:15 GMT
WORKDIR /usr/local/apache2
# Wed, 13 Sep 2017 00:56:15 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Wed, 13 Sep 2017 00:56:15 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Wed, 13 Sep 2017 00:56:16 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Wed, 13 Sep 2017 00:56:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:56:45 GMT
ENV HTTPD_VERSION=2.4.27
# Wed, 13 Sep 2017 00:56:45 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Wed, 13 Sep 2017 00:56:46 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Wed, 13 Sep 2017 00:56:46 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Wed, 13 Sep 2017 00:56:46 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Wed, 13 Sep 2017 00:56:46 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Wed, 13 Sep 2017 00:58:20 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Sep 2017 00:58:20 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Wed, 13 Sep 2017 00:58:20 GMT
EXPOSE 80/tcp
# Wed, 13 Sep 2017 00:58:20 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57095d1c44f233ca8d98890a008c637d8f5263adf74f0a30579836c3983a9bc8`  
		Last Modified: Thu, 07 Sep 2017 23:11:39 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5cfb71676749f3928f1ec5e08471b8aba95c5dc448c4f4cbf1567061d064cb`  
		Last Modified: Wed, 13 Sep 2017 01:00:03 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b77fd81a6f6e18e109eb12f93b2ee8bbbf93dfbbac96dee2ec1da0850fb0584`  
		Last Modified: Wed, 13 Sep 2017 01:00:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a7b67625a9f475075a30c9bfbc837d59aacad7a004c51502ab8707edc133de`  
		Last Modified: Wed, 13 Sep 2017 01:00:06 GMT  
		Size: 13.4 MB (13365248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444a3c783c9e820e5a440238acc8a4a8454233bc7bfa3641fc053ee2526da0e5`  
		Last Modified: Wed, 13 Sep 2017 01:00:04 GMT  
		Size: 2.9 MB (2915981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c99018b2cd163290febb3e495b9d1f1b35deb94213a15bcdb968a34d7d90ced`  
		Last Modified: Wed, 13 Sep 2017 01:00:04 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm variant v5

```console
$ docker pull httpd@sha256:d8a8a3cb0580c871bfad5d8e1490609a6e3b6bf7c29601b6577656c1fd07c17d
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65832797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c301c0889d00d45b0e6644fedc651bdbcca183b43cfe8ed3bd71f69427f39f3`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Sep 2017 19:56:37 GMT
ADD file:195667b0ccd6dad7d7793044adefb6ab0b4934a95d6383e0e1b09275397bc1e7 in / 
# Fri, 08 Sep 2017 19:56:39 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 19:56:56 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 08 Sep 2017 22:15:31 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Sep 2017 22:15:32 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 22:15:35 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 08 Sep 2017 22:15:36 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Sep 2017 22:15:37 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Fri, 08 Sep 2017 22:15:38 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Fri, 08 Sep 2017 22:15:41 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Fri, 08 Sep 2017 22:26:51 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 22:26:52 GMT
ENV HTTPD_VERSION=2.4.27
# Fri, 08 Sep 2017 22:26:53 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Fri, 08 Sep 2017 22:26:53 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 22:26:54 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 22:26:56 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 22:26:57 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 22:38:10 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 22:38:11 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Fri, 08 Sep 2017 22:38:12 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 22:38:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:ab9efa2081b39a1cb31bd23524b8c558c5ed00605e9d06b88d5aa68198966df1`  
		Last Modified: Fri, 08 Sep 2017 20:11:48 GMT  
		Size: 50.9 MB (50877486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec6eb2dde9f9e22c7218a4ab3d97a8ab6aedb0bb8390dc9dd86822e39687507`  
		Last Modified: Fri, 08 Sep 2017 20:12:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eabfa08cefdfe5f344276c873399d5c6854a0279718758ac8940e7f5e93120a`  
		Last Modified: Fri, 08 Sep 2017 22:39:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6241cd59b3f06c4b40a71b05b284bd9131c81ba0e57ed423e678a44f4b7a315`  
		Last Modified: Fri, 08 Sep 2017 22:39:03 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d5455a15e9f75aa61783b9762b7bb1b8e63f1c352e8daceacfe082706c62c1`  
		Last Modified: Fri, 08 Sep 2017 22:39:13 GMT  
		Size: 12.0 MB (12033095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7710135af6d856e49ec82f245a9838f2eb512b30d8889ec92a4e48df9886b`  
		Last Modified: Fri, 08 Sep 2017 22:39:07 GMT  
		Size: 2.9 MB (2921200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad00cd1092b171f745fef9e4aa4c42549174683dddc5e90019e949f28771e999`  
		Last Modified: Fri, 08 Sep 2017 22:39:02 GMT  
		Size: 299.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm variant v7

```console
$ docker pull httpd@sha256:3e1f996bf6cc57b7a3ab326fb924febeccc2a0b760dee26859b713426d538de9
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63016836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9140482c4c9017823d2a32c5207c9d362fc0486e9a73723939b21c74d87b1b75`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 09 Sep 2017 01:40:17 GMT
ADD file:ef59ce7fe68882b1b44bc3c4a5e9e465561cb257fb63f8c2b3c247abb012486b in / 
# Sat, 09 Sep 2017 01:40:18 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 01:40:26 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Tue, 12 Sep 2017 00:40:22 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 12 Sep 2017 00:40:23 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Sep 2017 00:40:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 12 Sep 2017 00:40:26 GMT
WORKDIR /usr/local/apache2
# Tue, 12 Sep 2017 00:40:27 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Tue, 12 Sep 2017 00:40:28 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Tue, 12 Sep 2017 00:40:30 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Tue, 12 Sep 2017 00:45:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Tue, 12 Sep 2017 00:45:50 GMT
ENV HTTPD_VERSION=2.4.27
# Tue, 12 Sep 2017 00:45:50 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Tue, 12 Sep 2017 00:45:51 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Tue, 12 Sep 2017 00:45:52 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Tue, 12 Sep 2017 00:45:53 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Tue, 12 Sep 2017 00:45:54 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Tue, 12 Sep 2017 01:27:03 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Sep 2017 01:27:04 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Tue, 12 Sep 2017 01:27:06 GMT
EXPOSE 80/tcp
# Tue, 12 Sep 2017 01:27:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:e925dd4ffa2a7ffdc23dbce8d2b25866e687204da4ed5a664a51d787e32366d4`  
		Last Modified: Sat, 09 Sep 2017 01:50:36 GMT  
		Size: 48.7 MB (48682076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7465345c56e57d4f5936077ff1647ba4f2e9fe6d8aceab8453cc05bc2e16265`  
		Last Modified: Sat, 09 Sep 2017 01:51:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efe3b5e23f8f48bf934afd7f7951782c75f786cf044ef0387632c0b7f116b1a`  
		Last Modified: Tue, 12 Sep 2017 01:27:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11964832762350428d8b204079e05ced30eec0183b6a7cb86a5992018a80b2e0`  
		Last Modified: Tue, 12 Sep 2017 01:27:57 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a8dc691d466fb32fde4e26b3e247eda436d977173609be4009af5490550af`  
		Last Modified: Tue, 12 Sep 2017 01:28:09 GMT  
		Size: 11.5 MB (11543072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4c10fe2ddd64d355f6bd3a38fe42e9b6d95433b7c18679ff272579d74eed69`  
		Last Modified: Tue, 12 Sep 2017 01:28:03 GMT  
		Size: 2.8 MB (2790671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a48918afaafa00b8b09161b76a72af95c99e58d7fe32c73185bf3eb49aea59`  
		Last Modified: Tue, 12 Sep 2017 01:27:57 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:321769e4590b62693203f8846a099b39cef78c645647e07cee098c065826a9a9
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64769692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba0a51357c593165a822932a9c36242979c8bbed654c823e618f19463b2f70a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 17:23:54 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 08 Sep 2017 21:08:57 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Sep 2017 21:08:57 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 21:09:00 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 08 Sep 2017 21:09:02 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Sep 2017 21:09:03 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Fri, 08 Sep 2017 21:09:04 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Fri, 08 Sep 2017 21:09:07 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Fri, 08 Sep 2017 21:10:33 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 21:10:34 GMT
ENV HTTPD_VERSION=2.4.27
# Fri, 08 Sep 2017 21:10:35 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Fri, 08 Sep 2017 21:10:36 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 21:10:37 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 21:10:38 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 21:10:39 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 21:17:35 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 21:17:36 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Fri, 08 Sep 2017 21:17:37 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 21:17:38 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8076495958236d7bdb5452a421c8c7a10288ca80cfa845d0ab92a4e92c547bb0`  
		Last Modified: Fri, 08 Sep 2017 17:35:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872dd904ef769f00d6816b9169047c14c297f1b58f2138c1d6459aa6ffce2e36`  
		Last Modified: Fri, 08 Sep 2017 21:18:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dace0777345085b7f6f7dfde5c759999893138e36f15a1e40dd1337495533cb`  
		Last Modified: Fri, 08 Sep 2017 21:18:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a3d202fdca12024e1f5f4f0e8e01933947a84d8bfa03a6340934d29ff723af`  
		Last Modified: Fri, 08 Sep 2017 21:18:50 GMT  
		Size: 12.1 MB (12081017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e550d3d900947105116e0529927785c5ff18a45e5730f7bb22f90c3e5eeb47`  
		Last Modified: Fri, 08 Sep 2017 21:18:42 GMT  
		Size: 2.8 MB (2758199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de596fb48369a3440d9b0524372546adefd52ddd5be8ac6a40fb5aa4584dbbf5`  
		Last Modified: Fri, 08 Sep 2017 21:18:39 GMT  
		Size: 300.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; 386

```console
$ docker pull httpd@sha256:c66a64e0c4fe5d77806e0c8e1ee8049f1fa1b7097478319e52cdae12c46ed20c
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73518742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6dbaa55b256d4ebcf473e77d340854250cd0204d40d567e3752eab5580def4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Sep 2017 13:17:52 GMT
ADD file:e02edf114d3ee3a58b6c6729d41261abc361f69333d3b08c7c730572fd6c1874 in / 
# Fri, 08 Sep 2017 13:17:52 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 13:17:57 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 08 Sep 2017 14:29:58 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Sep 2017 14:29:58 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 14:29:59 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 08 Sep 2017 14:30:01 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Sep 2017 14:30:01 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Fri, 08 Sep 2017 14:30:01 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Fri, 08 Sep 2017 14:30:02 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Fri, 08 Sep 2017 14:31:01 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 14:31:01 GMT
ENV HTTPD_VERSION=2.4.27
# Fri, 08 Sep 2017 14:31:02 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Fri, 08 Sep 2017 14:31:02 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 14:31:02 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 14:31:03 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 14:31:03 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 14:35:31 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 14:35:32 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Fri, 08 Sep 2017 14:35:32 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 14:35:32 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f611f84acffe6a66fad3356eb9101ed9fff54e980701079bbce3ee4826ccd3ae`  
		Last Modified: Fri, 08 Sep 2017 13:22:33 GMT  
		Size: 52.8 MB (52773126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc768172ab89d7a6e85f6de8ef6d326e5dcff81fa0abeacdf106fa59a527fb`  
		Last Modified: Fri, 08 Sep 2017 13:22:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc2bac7300fee0acb6b9d9dc7710c4812ca85aa7999ada77c5af90ad416bdaf`  
		Last Modified: Fri, 08 Sep 2017 14:37:13 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f34d19137438e14b6d2f1e29546db1e59137778c5144a2a6094ed424ab99d`  
		Last Modified: Fri, 08 Sep 2017 14:37:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcafc45970dbf078abcfc2c660fbd4c4cf0a66a2b24af7236718418e8cf794a`  
		Last Modified: Fri, 08 Sep 2017 14:37:18 GMT  
		Size: 18.0 MB (17968926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc763006998830b30a7f66fd9e756a058514bd22e10df60c06d624869b36a12`  
		Last Modified: Fri, 08 Sep 2017 14:37:15 GMT  
		Size: 2.8 MB (2775677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cc40c358e5bd3a2734d8505694787c76356d4a26ca9a368050d3b67bec915e`  
		Last Modified: Fri, 08 Sep 2017 14:37:13 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; ppc64le

```console
$ docker pull httpd@sha256:8d6fd6fdde9c2e726ee4a07a371d9c29a4c2277887f62297932398ed2de6c5a6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67744483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb4876c724c8d12c35305c76da466dd5eea3e083690d05637378c428290e504`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 00:32:25 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 08 Sep 2017 01:00:27 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Sep 2017 01:00:27 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 01:00:28 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 08 Sep 2017 01:00:28 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Sep 2017 01:00:28 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Fri, 08 Sep 2017 01:00:28 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Fri, 08 Sep 2017 01:00:29 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Fri, 08 Sep 2017 01:00:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:00:55 GMT
ENV HTTPD_VERSION=2.4.27
# Fri, 08 Sep 2017 01:00:56 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Fri, 08 Sep 2017 01:00:56 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 01:00:56 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 01:00:56 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 01:00:56 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 01:02:35 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 01:02:36 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Fri, 08 Sep 2017 01:02:36 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 01:02:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e4919532c9228bb9d7e1885752902770f2f552da7fb4342bd31c4182b004fa`  
		Last Modified: Fri, 08 Sep 2017 00:37:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb9172121693b5a3b03c677ea0bc526ed87b1c6008a042826862ffa09efda82`  
		Last Modified: Fri, 08 Sep 2017 01:03:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f764a5c3b56cada244e6348c9fcd4ba9756e369a5073b3232a82e95359980e6e`  
		Last Modified: Fri, 08 Sep 2017 01:03:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5326fe740bd1e987a2c43712c5c0518126d4bbc0e31c34e2eebff7e7b27013f`  
		Last Modified: Fri, 08 Sep 2017 01:03:19 GMT  
		Size: 13.0 MB (13034963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d8728e33b270221f87e12824b21584363217f67837a59371cf3c15c47f7835`  
		Last Modified: Fri, 08 Sep 2017 01:03:16 GMT  
		Size: 2.9 MB (2898911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c0e59bf9826da0d01af6857d007666db13480a50e79be5198759ca7f09bfcc`  
		Last Modified: Fri, 08 Sep 2017 01:03:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; s390x

```console
$ docker pull httpd@sha256:ce7eb51235cb95b12ea2b503afd170d77a87412e7aa172be4e96bf1f07766c26
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68836946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46701b03d4953026ab98e0f3cf7b3e0de5d487d4414fd6d6c93581fab5e80a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 05:21:45 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 08 Sep 2017 05:49:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Sep 2017 05:49:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 05:49:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 08 Sep 2017 05:49:42 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Sep 2017 05:49:43 GMT
ENV NGHTTP2_VERSION=1.18.1-1
# Fri, 08 Sep 2017 05:49:43 GMT
ENV OPENSSL_VERSION=1.0.2l-1~bpo8+1
# Fri, 08 Sep 2017 05:49:43 GMT
RUN { 		echo 'deb http://deb.debian.org/debian stretch main'; 	} > /etc/apt/sources.list.d/stretch.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release n=stretch'; 		echo 'Pin-Priority: -10'; 		echo; 		echo 'Package: libnghttp2*'; 		echo "Pin: version $NGHTTP2_VERSION"; 		echo 'Pin-Priority: 990'; 		echo; 	} > /etc/apt/preferences.d/unstable-nghttp2
# Fri, 08 Sep 2017 05:50:09 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		libapr1 		libaprutil1 		libaprutil1-ldap 		libapr1-dev 		libaprutil1-dev 		liblua5.2-0 		libnghttp2-14=$NGHTTP2_VERSION 		libpcre++0 		libssl1.0.0=$OPENSSL_VERSION 		libxml2 	&& rm -r /var/lib/apt/lists/*
# Fri, 08 Sep 2017 05:50:09 GMT
ENV HTTPD_VERSION=2.4.27
# Fri, 08 Sep 2017 05:50:09 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Fri, 08 Sep 2017 05:50:09 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 05:50:10 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 05:50:10 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Fri, 08 Sep 2017 05:50:10 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Fri, 08 Sep 2017 05:51:30 GMT
RUN set -x 	&& buildDeps=" 		bzip2 		ca-certificates 		dpkg-dev 		gcc 		liblua5.2-dev 		libnghttp2-dev=$NGHTTP2_VERSION 		libpcre++-dev 		libssl-dev=$OPENSSL_VERSION 		libxml2-dev 		zlib1g-dev 		make 		wget 	" 	&& apt-get update 	&& apt-get install -y --no-install-recommends -V $buildDeps 	&& rm -r /var/lib/apt/lists/* 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 05:51:30 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Fri, 08 Sep 2017 05:51:30 GMT
EXPOSE 80/tcp
# Fri, 08 Sep 2017 05:51:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c747fbf4faeb1dce4f7abd4d39a590917ebc8c73256a2277eb5e6774a9faade5`  
		Last Modified: Fri, 08 Sep 2017 05:24:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8a98ac909b3967a45c6023d10e26080cb3fe02d270248f87f8e0988b7d8220`  
		Last Modified: Fri, 08 Sep 2017 05:51:56 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be15e267b38ac7d1046284da645f41a5108acc2cbb85e6f332ebbeab5cec7f5c`  
		Last Modified: Fri, 08 Sep 2017 05:51:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c621f844bacaaddda0343fcb4f3bc1806c96a9141a4dee4dbf17c4e6d6698d`  
		Last Modified: Fri, 08 Sep 2017 05:51:59 GMT  
		Size: 13.0 MB (13004287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35442bd212e054700313c55d6568843cd053c8501235520d3ea2449bd8d7b4e6`  
		Last Modified: Fri, 08 Sep 2017 05:51:57 GMT  
		Size: 3.0 MB (3042849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bc059ee36a1817001dbf235068437efef48ffa6fb83ba002d89f481fe262c`  
		Last Modified: Fri, 08 Sep 2017 05:51:56 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
