## `perl:threaded`

```console
$ docker pull perl@sha256:84965a2b22480412a99d779a61da9db33a7589037649cb38d00c26f1b74956fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `perl:threaded` - linux; amd64

```console
$ docker pull perl@sha256:ac65fb7d2e004f3d39c125a30ec818bbd2e4a178696cf65350e438f778965624
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336813031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9955f91488630d061c62e1c1c2beb48e0b406ac71afbdcf29a9a2c82bec4b4a`
-	Default Command: `["perl5.26.0","-de0"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:42 GMT
ADD file:a7405474b639b2239b96a93d02803224c052a390fe42b3f9080f2ad07de94640 in / 
# Wed, 13 Sep 2017 08:41:42 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:36:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:36:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 12:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:37:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 15:25:17 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 13 Sep 2017 15:25:17 GMT
COPY file:2be96a0b9a6d4b3ea837439f6ea05fc01b773b4b26dd6bd7635bd489469d0075 in /usr/src/perl/ 
# Wed, 13 Sep 2017 15:25:17 GMT
WORKDIR /usr/src/perl
# Wed, 13 Sep 2017 15:38:47 GMT
RUN curl -SL https://www.cpan.org/src/5.0/perl-5.26.0.tar.bz2 -o perl-5.26.0.tar.bz2     && echo 'f21d66de84982175e95ad15fd8d0e22fed2cc2de7e4394f5d48dbe451be2f6f2 *perl-5.26.0.tar.bz2' | sha256sum -c -     && tar --strip-components=1 -xjf perl-5.26.0.tar.bz2 -C /usr/src/perl     && rm perl-5.26.0.tar.bz2     && cat *.patch | patch -p1     && ./Configure -Dusethreads -Duse64bitall -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO http://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7043.tar.gz     && echo '68a06f7da80882a95bc02c92c7ee305846fb6ab648cf83678ea945e44ad65c65 *App-cpanminus-1.7043.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7043.tar.gz && cd App-cpanminus-1.7043 && perl bin/cpanm . && cd /root     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7043* /tmp/*
# Wed, 13 Sep 2017 15:38:47 GMT
WORKDIR /root
# Wed, 13 Sep 2017 15:38:48 GMT
CMD ["perl5.26.0" "-de0"]
```

-	Layers:
	-	`sha256:219d2e45b4afc3d80375a2fcf76505684de01f55027fb35a691099f0e538fdd8`  
		Last Modified: Thu, 07 Sep 2017 23:20:31 GMT  
		Size: 45.1 MB (45125497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9ce992ffe4e9206f990140191a5c20da0b4d94b00368b0cf95d842ff624a05`  
		Last Modified: Wed, 13 Sep 2017 12:57:46 GMT  
		Size: 11.1 MB (11103324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0df8518230c3fcec095c3d4d27ee2f0f7df43aff4edb1461414ed74fa0751ec`  
		Last Modified: Wed, 13 Sep 2017 12:57:44 GMT  
		Size: 4.6 MB (4634394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ae21afde7b8e1eac3c1778aafa74ca286c2b5fccbb710da1016ca24a0bac56`  
		Last Modified: Wed, 13 Sep 2017 12:58:12 GMT  
		Size: 50.0 MB (50015593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa1c2e15c01b98aa16e2438aa6cf21fcddab44134694366355f447516dc7c18`  
		Last Modified: Wed, 13 Sep 2017 12:59:06 GMT  
		Size: 212.8 MB (212756174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debef9879b869df2e42f916215bcd7640008bc5b60510173626bc802a54df196`  
		Last Modified: Wed, 13 Sep 2017 16:01:05 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99df600360d83873b602227c23414a67c7de9dbfeae07d5e2f967a469243e0`  
		Last Modified: Wed, 13 Sep 2017 16:01:29 GMT  
		Size: 13.2 MB (13177870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:c32244ba410b68add688081038c1c7048632ae9456af645d89fa3927d386c60d
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318561874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac722d3f8fe207b72d4c3dfc6a9a19c2fc84822b38d4ea0e2ef74bf57258f6ab`
-	Default Command: `["perl5.26.0","-de0"]`

```dockerfile
# Mon, 24 Jul 2017 17:24:29 GMT
ADD file:e7cdf243bc54956f36bab0ce3d5cae3c6dfdaeadd24280fe05691ba6b7f26860 in / 
# Mon, 24 Jul 2017 17:24:30 GMT
CMD ["bash"]
# Mon, 24 Jul 2017 18:17:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 24 Jul 2017 18:17:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 24 Jul 2017 18:18:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Aug 2017 10:11:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2017 08:11:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 07 Sep 2017 08:11:27 GMT
COPY file:2be96a0b9a6d4b3ea837439f6ea05fc01b773b4b26dd6bd7635bd489469d0075 in /usr/src/perl/ 
# Thu, 07 Sep 2017 08:11:27 GMT
WORKDIR /usr/src/perl
# Thu, 07 Sep 2017 08:37:29 GMT
RUN curl -SL https://www.cpan.org/src/5.0/perl-5.26.0.tar.bz2 -o perl-5.26.0.tar.bz2     && echo 'f21d66de84982175e95ad15fd8d0e22fed2cc2de7e4394f5d48dbe451be2f6f2 *perl-5.26.0.tar.bz2' | sha256sum -c -     && tar --strip-components=1 -xjf perl-5.26.0.tar.bz2 -C /usr/src/perl     && rm perl-5.26.0.tar.bz2     && cat *.patch | patch -p1     && ./Configure -Dusethreads -Duse64bitall -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO http://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7043.tar.gz     && echo '68a06f7da80882a95bc02c92c7ee305846fb6ab648cf83678ea945e44ad65c65 *App-cpanminus-1.7043.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7043.tar.gz && cd App-cpanminus-1.7043 && perl bin/cpanm . && cd /root     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7043* /tmp/*
# Thu, 07 Sep 2017 08:37:30 GMT
WORKDIR /root
# Thu, 07 Sep 2017 08:37:31 GMT
CMD ["perl5.26.0" "-de0"]
```

-	Layers:
	-	`sha256:774bc81cd4ddf5f394102ad2f77e00f2356dd6bedb23ecae3079dbea3e27f502`  
		Last Modified: Mon, 24 Jul 2017 17:30:34 GMT  
		Size: 42.9 MB (42911098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee7e4f77d4aa6f9bcc0763fa643da6da44b121dc949d2e51c94e5a19f595aed`  
		Last Modified: Mon, 24 Jul 2017 18:32:11 GMT  
		Size: 10.1 MB (10059995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9634dfe9d5dfaf995a20cf7eced9003e26754ad12eee2538c8acc1ed95bf7fa`  
		Last Modified: Mon, 24 Jul 2017 18:32:09 GMT  
		Size: 4.4 MB (4385339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48ef06aab1ecdc1cdd7a2d627918df0e2056f6cccc7182f0b50f98cc3919406`  
		Last Modified: Mon, 24 Jul 2017 18:32:43 GMT  
		Size: 48.0 MB (47963855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b2244d69635acf90f78bd437bd749244a79e7beefb7e6c08d8d9e57dcfc2b9`  
		Last Modified: Tue, 29 Aug 2017 20:16:06 GMT  
		Size: 200.2 MB (200232275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b7356404ebcaf6b67002c0d2e066fcb2f618d91ff4683c4c66db29b34d4e45`  
		Last Modified: Thu, 07 Sep 2017 09:14:46 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb826377ec5ddb78150bec68c8789356d74741ab3475997b7c3479a5988e3890`  
		Last Modified: Thu, 07 Sep 2017 09:15:32 GMT  
		Size: 13.0 MB (13009134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
