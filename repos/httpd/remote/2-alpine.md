## `httpd:2-alpine`

```console
$ docker pull httpd@sha256:1d48a251bc2448e100c728fa060f65ca7b91679d1b59948ed6c204151a06e7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `httpd:2-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:5aa79cdf430ea793f0a0c6ed50989ce51c4419c7181f28f4db29b1a56562e8e4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 MB (29150795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb831e403799e21583f609fdc2ef7366d4a23ade6a051f432fb6cd5eb9ef98c5`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 27 Jun 2017 18:41:51 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Tue, 27 Jun 2017 18:42:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 00:58:22 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Wed, 13 Sep 2017 00:58:22 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 13 Sep 2017 00:58:22 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2017 00:58:23 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Wed, 13 Sep 2017 00:58:23 GMT
WORKDIR /usr/local/apache2
# Wed, 13 Sep 2017 00:58:23 GMT
ENV HTTPD_VERSION=2.4.27
# Wed, 13 Sep 2017 00:58:23 GMT
ENV HTTPD_SHA1=699e4e917e8fb5fd7d0ce7e009f8256ed02ec6fc
# Wed, 13 Sep 2017 00:58:23 GMT
ENV HTTPD_BZ2_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=httpd/httpd-2.4.27.tar.bz2
# Wed, 13 Sep 2017 00:58:23 GMT
ENV HTTPD_ASC_URL=https://www.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Wed, 13 Sep 2017 00:58:24 GMT
ENV HTTPD_BZ2_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2
# Wed, 13 Sep 2017 00:58:24 GMT
ENV HTTPD_ASC_FALLBACK_URL=https://archive.apache.org/dist/httpd/httpd-2.4.27.tar.bz2.asc
# Wed, 13 Sep 2017 00:59:28 GMT
RUN set -x 	&& runDeps=' 		apr-dev 		apr-util-dev 		apr-util-ldap 		perl 	' 	&& apk add --no-cache --virtual .build-deps 		$runDeps 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		libressl 		libressl-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		pcre-dev 		tar 		zlib-dev 		&& { 		wget -O httpd.tar.bz2 "$HTTPD_BZ2_URL" 		|| wget -O httpd.tar.bz2 "$HTTPD_BZ2_FALLBACK_URL" 	; } 	&& echo "$HTTPD_SHA1 *httpd.tar.bz2" | sha1sum -c - 	&& { 		wget -O httpd.tar.bz2.asc "$HTTPD_ASC_URL" 		|| wget -O httpd.tar.bz2.asc "$HTTPD_ASC_FALLBACK_URL" 	; } 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A93D62ECC3C8EA12DB220EC934EA76E6791485A8 	&& gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2 	&& rm -rf "$GNUPGHOME" httpd.tar.bz2.asc 		&& mkdir -p src 	&& tar -xf httpd.tar.bz2 -C src --strip-components=1 	&& rm httpd.tar.bz2 	&& cd src 		&& wget -O libressl.patch 'https://git.alpinelinux.org/cgit/aports/plain/main/apache2/libressl.patch?id=d7292029f25a131a0f15ebc3bc2300e75f4c131a' 	&& patch -p1 < libressl.patch 	&& rm libressl.patch 		&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 	&& make -j "$(nproc)" 	&& make install 		&& cd .. 	&& rm -r src man manual 		&& sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		&& runDeps="$runDeps $( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .httpd-rundeps $runDeps 	&& apk del .build-deps
# Wed, 13 Sep 2017 00:59:29 GMT
COPY file:761e313354b918b6cd7ea99975a4f6b53ff5381ba689bab2984aec4dab597215 in /usr/local/bin/ 
# Wed, 13 Sep 2017 00:59:29 GMT
EXPOSE 80/tcp
# Wed, 13 Sep 2017 00:59:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90497a997d46cf92a48d6eaf06d5ae46115247d44339cfb7980c47ea2fa0f81`  
		Last Modified: Wed, 13 Sep 2017 01:00:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377c5332d63e44594c71c718596694a79bc96af5c110a108756728d1e8581be7`  
		Last Modified: Wed, 13 Sep 2017 01:00:23 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c633dfd05f8fd7a38540febf08210aa5280cbda05c7e88768d0ed2a9ad3f912`  
		Last Modified: Wed, 13 Sep 2017 01:00:29 GMT  
		Size: 27.2 MB (27158708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2408cbae34412f6a32cbf420145dde5bb4753561a236a959e5f4830c6470a4d3`  
		Last Modified: Wed, 13 Sep 2017 01:00:23 GMT  
		Size: 288.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
