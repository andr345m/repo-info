## `postgres:latest`

```console
$ docker pull postgres@sha256:f594c0086738f808f3aa6de591b0c3349dd23ebcc42b45d16ed2ba1e9f09b02a
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:a20312c79c42e777fa5f0a965fcdd6eb99cea945c02e328d03aa66e9baf62336
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104065647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b23ab70487a50fe8d7b1cf2b9f990adc181e1aef7e7247cc7b9a0da4e9fdf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2017 23:04:40 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Thu, 07 Sep 2017 23:04:41 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 06:57:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 06:57:56 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Wed, 13 Sep 2017 06:57:56 GMT
ENV GOSU_VERSION=1.10
# Wed, 13 Sep 2017 06:58:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 13 Sep 2017 06:58:42 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 13 Sep 2017 06:58:42 GMT
ENV LANG=en_US.utf8
# Wed, 13 Sep 2017 06:58:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 06:58:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 06:58:47 GMT
ENV PG_MAJOR=9.6
# Wed, 13 Sep 2017 06:58:47 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Wed, 13 Sep 2017 06:59:33 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Wed, 13 Sep 2017 06:59:34 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Wed, 13 Sep 2017 06:59:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 13 Sep 2017 06:59:35 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Sep 2017 06:59:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 13 Sep 2017 06:59:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Wed, 13 Sep 2017 06:59:36 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 13 Sep 2017 06:59:36 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Wed, 13 Sep 2017 06:59:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 13 Sep 2017 06:59:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 06:59:37 GMT
EXPOSE 5432/tcp
# Wed, 13 Sep 2017 06:59:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e25dde31be88bb44cdb36cb4484ea2df2a25e407f3ea45890874500739d89`  
		Last Modified: Wed, 13 Sep 2017 07:15:58 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2dab8762cf34850bb99e04ebfd754f1a73176c1ca0fe2ba8d6f94335466445`  
		Last Modified: Wed, 13 Sep 2017 07:15:58 GMT  
		Size: 985.1 KB (985140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5dda99857a86b53e8cf8cc25489d7b27fc5d16d3119da0db4aad9d530f64db`  
		Last Modified: Wed, 13 Sep 2017 07:15:59 GMT  
		Size: 7.1 MB (7112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab771f0785fe4b8c088191022becfd6f9c9d19d83bde4630037cf2d280f0798`  
		Last Modified: Wed, 13 Sep 2017 07:15:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2297bb8ef4e10f137a3c577e6526dba51be626454cd2428582b26ccff74c945e`  
		Last Modified: Wed, 13 Sep 2017 07:15:56 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264e4152011a7332bf600952d8b4ab9677d8a722c84f943333fd849a26634d3b`  
		Last Modified: Wed, 13 Sep 2017 07:16:04 GMT  
		Size: 43.4 MB (43356002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8257d34a60746205c2a7fe2b86f38717a82d9f4cba44d5f7b012af9befdc2d84`  
		Last Modified: Wed, 13 Sep 2017 07:15:54 GMT  
		Size: 7.1 KB (7107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7f588669cbca769ea6adebb2b810b9081533a328c85fe29e82e707f5f1113`  
		Last Modified: Wed, 13 Sep 2017 07:15:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d984a1e2c85bf92c039363cfdbfe7a6d627be4c2fcd8b2bff96832d8ca55a0e0`  
		Last Modified: Wed, 13 Sep 2017 07:15:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e467ce94b6e22f5115a80c99fe29dd013a2f43a639c417a633fb3fc064eac22c`  
		Last Modified: Wed, 13 Sep 2017 07:15:55 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26053fcd931290200eaedc3d956447b426c010bea31982afe2f72e54ddd75fcd`  
		Last Modified: Wed, 13 Sep 2017 07:15:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d1a131aeda1204ca9616fa39c837434b40fe009021dfe30703a76ee4957b0e01
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96579507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e60fce83a4482e113405f7b23df7947c4bf023e12370b3d7e85fa7aa906a685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Sep 2017 19:56:37 GMT
ADD file:195667b0ccd6dad7d7793044adefb6ab0b4934a95d6383e0e1b09275397bc1e7 in / 
# Fri, 08 Sep 2017 19:56:39 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 00:58:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 09 Sep 2017 00:58:47 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Sat, 09 Sep 2017 00:58:47 GMT
ENV GOSU_VERSION=1.10
# Sat, 09 Sep 2017 01:05:45 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 09 Sep 2017 01:11:13 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 09 Sep 2017 01:11:14 GMT
ENV LANG=en_US.utf8
# Sat, 09 Sep 2017 01:11:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 09 Sep 2017 01:11:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Sat, 09 Sep 2017 01:11:35 GMT
ENV PG_MAJOR=9.6
# Sat, 09 Sep 2017 01:11:36 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Tue, 12 Sep 2017 06:51:30 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Tue, 12 Sep 2017 06:51:33 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Tue, 12 Sep 2017 06:51:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 12 Sep 2017 06:51:36 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Sep 2017 06:51:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 12 Sep 2017 06:51:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Tue, 12 Sep 2017 06:51:39 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 12 Sep 2017 06:51:40 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Tue, 12 Sep 2017 06:51:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 12 Sep 2017 06:51:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Sep 2017 06:51:44 GMT
EXPOSE 5432/tcp
# Tue, 12 Sep 2017 06:51:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab9efa2081b39a1cb31bd23524b8c558c5ed00605e9d06b88d5aa68198966df1`  
		Last Modified: Fri, 08 Sep 2017 20:11:48 GMT  
		Size: 50.9 MB (50877486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39962272c0530ad0928255e61d3f0f07a54be2a08a7983edf5f92bccb1e344bb`  
		Last Modified: Tue, 12 Sep 2017 10:17:35 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a47eb5f3f45c31676515a5b278c63b18e3afcca219698043819792821a72f2`  
		Last Modified: Tue, 12 Sep 2017 10:17:31 GMT  
		Size: 974.8 KB (974811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f091af872634ff526a4a9307bd97fc771ba09bb7a72496b59ef5a7093f1ca0`  
		Last Modified: Tue, 12 Sep 2017 10:17:46 GMT  
		Size: 7.1 MB (7112984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4debf953b6545bce21594847ae1cdec6ed9a6b3db0b3301e4cd5ca177181bef9`  
		Last Modified: Tue, 12 Sep 2017 10:17:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83e144e78add6abe2b5e4ebe3f9f76472192da8c576d49053bde479081ea709`  
		Last Modified: Tue, 12 Sep 2017 10:17:25 GMT  
		Size: 4.5 KB (4495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fa2f6245765995a90abbe93193ba1639dfb4e7fc087c11345b1e3519d543e5`  
		Last Modified: Tue, 12 Sep 2017 10:18:03 GMT  
		Size: 37.6 MB (37598198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608085701aebcc62f2d219edcd20b4f07b0e75d3f5b23e9870a12a5745158672`  
		Last Modified: Tue, 12 Sep 2017 10:17:22 GMT  
		Size: 7.1 KB (7107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f28a16c9a0092f60eff440dbda01f07de38674e865fea65ea17e14f34c5b3`  
		Last Modified: Tue, 12 Sep 2017 10:17:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6925025d7db958a515c46e2fadf6d13eb126380b3a54d643cf480fc71b143b3f`  
		Last Modified: Tue, 12 Sep 2017 10:17:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7e5c887cfaaf0f7a6b1662c59ea96269cec90278a01ac8b95a04cfc218b4f8`  
		Last Modified: Tue, 12 Sep 2017 10:17:22 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce32cbdf65fc09a9d9b0850be683498e9280a3bf8852fb383f7d33aafc39bd7`  
		Last Modified: Tue, 12 Sep 2017 10:17:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8facf2298de82094e3597fe0a7f9fdc2cf931fe1aee505c4853091f6c8a00d8a
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93178558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8700fbd1782a42613ee76a85778026d810f33451b821616333461a4493a556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 25 Jul 2017 12:47:49 GMT
ADD file:0448b2cd9da7d0c40fa8f3ee9ac6db219379c4631011ee1495ec8ad66be4f52e in / 
# Tue, 25 Jul 2017 12:47:52 GMT
CMD ["bash"]
# Thu, 31 Aug 2017 21:21:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 31 Aug 2017 21:21:12 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Thu, 31 Aug 2017 21:21:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 31 Aug 2017 21:24:18 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Thu, 31 Aug 2017 21:28:12 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 31 Aug 2017 21:28:13 GMT
ENV LANG=en_US.utf8
# Thu, 31 Aug 2017 21:28:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Aug 2017 21:28:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 31 Aug 2017 21:28:39 GMT
ENV PG_MAJOR=9.6
# Thu, 31 Aug 2017 21:28:39 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Thu, 31 Aug 2017 22:18:44 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Thu, 31 Aug 2017 22:18:49 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Thu, 31 Aug 2017 22:18:52 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 31 Aug 2017 22:18:53 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2017 22:18:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 31 Aug 2017 22:18:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Thu, 31 Aug 2017 22:18:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 31 Aug 2017 22:18:58 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Thu, 31 Aug 2017 22:19:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 31 Aug 2017 22:19:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Aug 2017 22:19:03 GMT
EXPOSE 5432/tcp
# Thu, 31 Aug 2017 22:19:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5e32d580a9d26e16dd26eaf656c25de16f6fc4a5e2cf51e5d73de3d0b5a0966c`  
		Last Modified: Tue, 25 Jul 2017 13:05:41 GMT  
		Size: 48.7 MB (48691924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cd8fd42f1fc46425d7c5a1f0b87026bd2877c1179d597f0eef3edaaed0bd91`  
		Last Modified: Fri, 01 Sep 2017 21:01:43 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda1d931115ddf63ec0f8a314dbdc1d35df727d4ef56030bf76a860e8e0b0d9`  
		Last Modified: Fri, 01 Sep 2017 21:01:41 GMT  
		Size: 959.7 KB (959661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54575937da13979c378d90bb18e326341f053c288ab4434efa17a5cbebeba3`  
		Last Modified: Fri, 01 Sep 2017 21:01:58 GMT  
		Size: 7.1 MB (7113014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3db813713b340b9e73b11fa8dc01293bbd0d96cb87c876aad10bb1d187f10d4`  
		Last Modified: Fri, 01 Sep 2017 21:01:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a7d0fbe8d473796305c768bc1d7b7437be2fe9ed2192848066d5f61bf4a2d7`  
		Last Modified: Fri, 01 Sep 2017 21:01:34 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085d041a82ccd92ed1728803a1894ed0defdbd7d6e9d653bcf64d1d36fc5654`  
		Last Modified: Fri, 01 Sep 2017 21:02:11 GMT  
		Size: 36.4 MB (36397930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d6628c4417ab1c45465003ab0df7bceefc78cbb6f88936a83f0a9a7f916e8`  
		Last Modified: Fri, 01 Sep 2017 21:01:32 GMT  
		Size: 7.1 KB (7109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c067b42d18cab8bb389679324b7793c2b58945aef3176a17bac35e4d67a1ef`  
		Last Modified: Fri, 01 Sep 2017 21:01:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e30ec009bea8ace73be54db7ea45a6d47a7880af8f385aec250ae8ce752c3`  
		Last Modified: Fri, 01 Sep 2017 21:01:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5d2a237e2bfbbe35b42e015f56a5f0f050cbe53acb8d220b745785aa9a4cf1`  
		Last Modified: Fri, 01 Sep 2017 21:01:31 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e51cf292fed8e286b872b80b10df2d1392f1d801041874fe0dbd13326226c4e`  
		Last Modified: Fri, 01 Sep 2017 21:01:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f80dc2795e9d8fe7999e4255c73812b131404b27cc8373dafd785e44fdab45df
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95155573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721c6c56ceb2129a8b6805463ad1b7d9e8593f3e0a2aa5b87db1a635c83e2d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Sep 2017 17:23:41 GMT
ADD file:9f576a63a5e03994904e585c35fbeef6a2c96c41d8f696705c033f3ca69b6a2b in / 
# Fri, 08 Sep 2017 17:23:42 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 23:42:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 23:43:03 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Fri, 08 Sep 2017 23:43:05 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 23:44:24 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 08 Sep 2017 23:44:58 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 08 Sep 2017 23:44:59 GMT
ENV LANG=en_US.utf8
# Fri, 08 Sep 2017 23:45:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 08 Sep 2017 23:45:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 08 Sep 2017 23:45:10 GMT
ENV PG_MAJOR=9.6
# Fri, 08 Sep 2017 23:45:11 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Sat, 09 Sep 2017 00:25:12 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Sat, 09 Sep 2017 00:25:14 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Sat, 09 Sep 2017 00:25:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 09 Sep 2017 00:25:17 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Sep 2017 00:25:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 09 Sep 2017 00:25:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Sat, 09 Sep 2017 00:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 09 Sep 2017 00:25:21 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Sat, 09 Sep 2017 00:25:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 09 Sep 2017 00:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Sep 2017 00:25:25 GMT
EXPOSE 5432/tcp
# Sat, 09 Sep 2017 00:25:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e91a355b0d3ff86add037a3f24718b760d8eb3f346f998e5116375ddce9eae19`  
		Last Modified: Fri, 08 Sep 2017 17:34:56 GMT  
		Size: 49.9 MB (49929457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781759b649c26203b4a27e64393e8bdd9872dd044e760bcf0282e0a7abdfeb19`  
		Last Modified: Sat, 09 Sep 2017 02:43:40 GMT  
		Size: 2.1 KB (2102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b522a80fe77c156872a74759ae149d99524b8c092e53f780553609e6241f87`  
		Last Modified: Sat, 09 Sep 2017 02:43:38 GMT  
		Size: 952.1 KB (952051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f59a9e2347edd55703588c84d162d20e81e78dea423e66342d1851b82c7618`  
		Last Modified: Sat, 09 Sep 2017 02:43:42 GMT  
		Size: 7.1 MB (7112967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5d9409d3241798ccac167cc07742ce716374926c58e89e83923b8368531cdc`  
		Last Modified: Sat, 09 Sep 2017 02:43:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578dc02e2c71817dc01ae642dc5ac2d77a2e96f359040662288f3fa3036ec05d`  
		Last Modified: Sat, 09 Sep 2017 02:43:36 GMT  
		Size: 4.5 KB (4495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ed3a41cc652aa346acbb0f65c6f9945f80da65406cf3aae26cf569fd130b37`  
		Last Modified: Sat, 09 Sep 2017 02:43:52 GMT  
		Size: 37.1 MB (37145050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ba00d97c6783154c89f143092848a5030e3e0bad27e8578f96b9779f40b7e`  
		Last Modified: Sat, 09 Sep 2017 02:43:34 GMT  
		Size: 7.1 KB (7109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c984a74d41bc82cb9fe00dadf875cd424fa97ba307148b915d9429824da2678`  
		Last Modified: Sat, 09 Sep 2017 02:43:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beb2e73e2f4ae30c23d03669b883f10ee8923e1b54daedcceb5f10d0b942f52`  
		Last Modified: Sat, 09 Sep 2017 02:43:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a301a920e52e601d9104389f6ba9e292b61ffbc109554df8b09bdf4fe18fbc7`  
		Last Modified: Sat, 09 Sep 2017 02:43:34 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2961f7f2d32fcfac0d5fd16324aa97191ddf34319428bf3bc5f825154e15092`  
		Last Modified: Sat, 09 Sep 2017 02:43:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:4c88a52e6fe16220ee7bfcb7fb99f10191aa2fa3e5feb3a47b19677e59ebfe25
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106024583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337e6527c76be5530dda9bd2d4e8f4f53ecd2f711df1e6c54556b12f9b35548e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Sep 2017 13:17:52 GMT
ADD file:e02edf114d3ee3a58b6c6729d41261abc361f69333d3b08c7c730572fd6c1874 in / 
# Fri, 08 Sep 2017 13:17:52 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:43:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 15:43:50 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Fri, 08 Sep 2017 15:43:50 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 15:44:39 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 08 Sep 2017 15:45:13 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 08 Sep 2017 15:45:13 GMT
ENV LANG=en_US.utf8
# Fri, 08 Sep 2017 15:45:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 08 Sep 2017 15:45:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 08 Sep 2017 15:45:24 GMT
ENV PG_MAJOR=9.6
# Fri, 08 Sep 2017 15:45:24 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Fri, 08 Sep 2017 15:47:29 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Fri, 08 Sep 2017 15:47:30 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Fri, 08 Sep 2017 15:47:31 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 08 Sep 2017 15:47:32 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 15:47:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Sep 2017 15:47:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Fri, 08 Sep 2017 15:47:33 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Sep 2017 15:47:33 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Fri, 08 Sep 2017 15:47:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 08 Sep 2017 15:47:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 15:47:35 GMT
EXPOSE 5432/tcp
# Fri, 08 Sep 2017 15:47:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f611f84acffe6a66fad3356eb9101ed9fff54e980701079bbce3ee4826ccd3ae`  
		Last Modified: Fri, 08 Sep 2017 13:22:33 GMT  
		Size: 52.8 MB (52773126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e29584000b223981af70bcdb356028277885af1ddf7397b7e475d2823876d8`  
		Last Modified: Fri, 08 Sep 2017 16:01:10 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e56e40615ec67cdb8d3a6de7dd45fa6112eaf09d4c3b9f278c9cdac8fce42c2`  
		Last Modified: Fri, 08 Sep 2017 16:01:09 GMT  
		Size: 964.0 KB (964013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af4faa932721992cdf7a1d229fd2627ba97e839397964b61e0d11f094ad0a1`  
		Last Modified: Fri, 08 Sep 2017 16:01:12 GMT  
		Size: 7.1 MB (7112902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd403fe3acf4a49afbd93847a033b8e1e904f6a92ac64f82ee4a34c9a9b3170b`  
		Last Modified: Fri, 08 Sep 2017 16:01:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737c3a416099faa1a4c37b3da3850fe77e1e73595e56e16f8e0f39d38ac8d1c`  
		Last Modified: Fri, 08 Sep 2017 16:01:08 GMT  
		Size: 4.5 KB (4489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1ad3897ad4ddd7dff5e4a1527f0cc0618e13ed5999dbf08a7ad6d96d46eb6b`  
		Last Modified: Fri, 08 Sep 2017 16:01:25 GMT  
		Size: 45.2 MB (45158524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc9895c79bff683ea10c61dcdd8258dedf35ca664009ddd46b883dce690f26`  
		Last Modified: Fri, 08 Sep 2017 16:01:08 GMT  
		Size: 7.1 KB (7106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e407853a56a4788b634efa2d602d02e8d5e09298bc90c4e8a58b3fc573942cba`  
		Last Modified: Fri, 08 Sep 2017 16:01:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8116cb6b6e6011cc3a7e037fb6c019f3add378d85952910bbedc4f05ad01c2`  
		Last Modified: Fri, 08 Sep 2017 16:01:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898c7320c7b1c9b85586fa7cf78d86a560c3cee31a72c81e603ab77fccd44418`  
		Last Modified: Fri, 08 Sep 2017 16:01:08 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bf3aef489a78f3885362c2ee9d4749e155baa9ea3e209f0ec5f915960b4371`  
		Last Modified: Fri, 08 Sep 2017 16:01:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:99f2583d5be605c436afe4bb22a77e7f2df55eb38ca6893c5340f7eca231a1e1
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102264543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ff48cc6bedb39f528123984f1c0aeb82dc1abb222e548eee6ac2e513967d29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Sep 2017 00:32:21 GMT
ADD file:483b3245941140ac32394a804364a1a9bd5dfdf1b4475238b61068cc7252ac08 in / 
# Fri, 08 Sep 2017 00:32:21 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:37:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 01:37:32 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Fri, 08 Sep 2017 01:37:33 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 01:38:00 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 08 Sep 2017 01:38:15 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 08 Sep 2017 01:38:15 GMT
ENV LANG=en_US.utf8
# Fri, 08 Sep 2017 01:38:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 08 Sep 2017 01:38:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 08 Sep 2017 01:38:21 GMT
ENV PG_MAJOR=9.6
# Fri, 08 Sep 2017 01:38:22 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Fri, 08 Sep 2017 01:39:13 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Fri, 08 Sep 2017 01:39:14 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Fri, 08 Sep 2017 01:39:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 08 Sep 2017 01:39:16 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 01:39:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Sep 2017 01:39:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Fri, 08 Sep 2017 01:39:17 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Sep 2017 01:39:18 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Fri, 08 Sep 2017 01:39:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 08 Sep 2017 01:39:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 01:39:19 GMT
EXPOSE 5432/tcp
# Fri, 08 Sep 2017 01:39:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d4a5434e09b7ac8431060d347d6ef1233ae07514878fb2aff4085bcf441c29f3`  
		Last Modified: Fri, 08 Sep 2017 00:36:52 GMT  
		Size: 51.8 MB (51809570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3da2fa5d3ae6a119563e671559fb255d321cb98f3ba7675028524546ddc8bf`  
		Last Modified: Fri, 08 Sep 2017 01:44:18 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c3f480bdeb964600a455e3e4edb09bcb265ad5f55af3240196320f9eb9bbfc`  
		Last Modified: Fri, 08 Sep 2017 01:44:17 GMT  
		Size: 953.9 KB (953850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04a10e7ac5dcbefe9d51aad5235fbb1adbc43798aa27ebc83f51f77b473f420`  
		Last Modified: Fri, 08 Sep 2017 01:44:18 GMT  
		Size: 7.1 MB (7112842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56818957c9e6deea1b96e5c78a5e414abd9042de3c128d67282696ecb5e63c4b`  
		Last Modified: Fri, 08 Sep 2017 01:44:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9051b68d8b61b409754d353870e336d02973467d8e55a4d7566cbb5700869e`  
		Last Modified: Fri, 08 Sep 2017 01:44:16 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58efb6adbd28c83040fdb59fe204c4e526a9e51e3e26ec3582d23031dd2b2ee`  
		Last Modified: Fri, 08 Sep 2017 01:44:27 GMT  
		Size: 42.4 MB (42372182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6b270c9cafbfaf1ada8665bd2d7ca3128e4dfa876f93c317f1e924269e36d3`  
		Last Modified: Fri, 08 Sep 2017 01:44:13 GMT  
		Size: 7.1 KB (7107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2f0724273e20255f50b26fbde0481215c4326f53f225b0eae1400458818fa0`  
		Last Modified: Fri, 08 Sep 2017 01:44:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5c722701cf85da119c31c7487026ad706432b02e42a2d919b492111eb1ddba`  
		Last Modified: Fri, 08 Sep 2017 01:44:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f66128af7e88bace7ee239f67c769f2348218d333b7c5a49d354977f7e4661c`  
		Last Modified: Fri, 08 Sep 2017 01:44:13 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c09e22b084cbba3bc9d01d8ff0ab5e13e49d9bd67fbb2d8483d09a0e0de2d2`  
		Last Modified: Fri, 08 Sep 2017 01:44:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:b28aaaa4365594a567179c5b67548cda5df81f755756965291c960aa81ca56ef
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100566753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d132cabf41895dd1685d0ad77a02d6b1a090784b772f01803ec7379ff1b536`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 08 Sep 2017 05:21:42 GMT
ADD file:996e52a941b7162fafcf761c415142a34a2fc703e21d2f264b824373e9fa4b1e in / 
# Fri, 08 Sep 2017 05:21:43 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 06:25:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 08 Sep 2017 06:25:51 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Fri, 08 Sep 2017 06:25:51 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 06:26:10 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 08 Sep 2017 06:26:22 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 08 Sep 2017 06:26:23 GMT
ENV LANG=en_US.utf8
# Fri, 08 Sep 2017 06:26:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 08 Sep 2017 06:26:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 08 Sep 2017 06:26:26 GMT
ENV PG_MAJOR=9.6
# Fri, 08 Sep 2017 06:26:26 GMT
ENV PG_VERSION=9.6.5-1.pgdg80+1
# Fri, 08 Sep 2017 06:35:49 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64|i386|ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi
# Fri, 08 Sep 2017 06:35:50 GMT
RUN mv -v "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample" /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/" 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Fri, 08 Sep 2017 06:35:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 08 Sep 2017 06:35:51 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 06:35:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 Sep 2017 06:35:51 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Fri, 08 Sep 2017 06:35:51 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 Sep 2017 06:35:52 GMT
COPY file:643bb6306366c6990a8d7cc47297e0080cc2a18a48a305868c51739e9416a044 in /usr/local/bin/ 
# Fri, 08 Sep 2017 06:35:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 08 Sep 2017 06:35:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 06:35:52 GMT
EXPOSE 5432/tcp
# Fri, 08 Sep 2017 06:35:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f39dbffcd07e3254246d3c2e4b3532c3697ed04f83eadf5433da820098787df`  
		Last Modified: Fri, 08 Sep 2017 05:24:42 GMT  
		Size: 52.8 MB (52788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c3d70a45af67e2fccddfab83e47f9cf841a136ea0b42ea145e6f73a80f463a`  
		Last Modified: Fri, 08 Sep 2017 07:10:41 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbd9acad107b86ffe249d0e02ffb63cc8fb256e07670d91fef18cc51d5ec1e1`  
		Last Modified: Fri, 08 Sep 2017 07:10:41 GMT  
		Size: 970.2 KB (970238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91470ff9dd3a9b5a4ad38a788f3c83f93c0b842e0f60f3bd66b5a41a5a1077a5`  
		Last Modified: Fri, 08 Sep 2017 07:10:42 GMT  
		Size: 7.1 MB (7131175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad4c2524a72239708c66fa2c6d570cf522e7ef925cf51158d73dfca1cbe423b`  
		Last Modified: Fri, 08 Sep 2017 07:10:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2127eedf7f5d4b075e50093a24922b0a9a24cb164caf101075554fc4530abbed`  
		Last Modified: Fri, 08 Sep 2017 07:10:40 GMT  
		Size: 4.5 KB (4495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634bcfae229d3e353c380a34be6ca3b31c4f3c05cc085d320e538aa643a1ee3a`  
		Last Modified: Fri, 08 Sep 2017 07:10:48 GMT  
		Size: 39.7 MB (39660501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0caa17d671ee7963b28bb5f93d6de481e5aa62612ec0731e9ea35118220af9`  
		Last Modified: Fri, 08 Sep 2017 07:10:39 GMT  
		Size: 7.1 KB (7103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af83523678e63c2acf314edae41aaa11743a7251dc0622e1e16f34311650ab1`  
		Last Modified: Fri, 08 Sep 2017 07:10:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84f8bf0d2bbcc8eb0304a2d082fb9271fa4befa055359632e1694f8ee27a4e6`  
		Last Modified: Fri, 08 Sep 2017 07:10:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6994fead2becab397901820861ce4ad9bb8b2bc8d4a61476cb23dbcf39465774`  
		Last Modified: Fri, 08 Sep 2017 07:10:39 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850608b76a01570b0b66c0f20383a1830addaf980edcf2b1769352875dc36056`  
		Last Modified: Fri, 08 Sep 2017 07:10:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
