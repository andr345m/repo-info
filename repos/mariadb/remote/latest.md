## `mariadb:latest`

```console
$ docker pull mariadb@sha256:c22eec18498fc23734a8e26c21c9b3019cebcf96ed1323aa147ec01c4038d307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:7897416f98c0ceb76f300ae865e55e62900f66c4fa3d7187763b343b94b184c1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135572324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7b193b16316b8914c4d8fdc37d82dfb0e86d15d44788f7ae2b1769e8ea9f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 09:40:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 13 Sep 2017 09:40:16 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 09:40:45 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 13 Sep 2017 09:40:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 09:41:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		apt-transport-https ca-certificates 		pwgen 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 11:36:19 GMT
ENV GPG_KEYS=199369E5404BD5FC7D2FE43BCBCB082A1BB943DB 	430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	4D1BB29D63D98E422B2113B19334A25F8507EFA5
# Wed, 13 Sep 2017 11:38:32 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 11:38:33 GMT
RUN echo "deb https://repo.percona.com/apt jessie main" > /etc/apt/sources.list.d/percona.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release o=Percona Development Team'; 		echo 'Pin-Priority: 998'; 	} > /etc/apt/preferences.d/percona
# Wed, 13 Sep 2017 11:39:17 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 13 Sep 2017 11:39:18 GMT
ENV MARIADB_VERSION=10.2.8+maria~jessie
# Wed, 13 Sep 2017 11:39:18 GMT
RUN echo "deb http://ftp.osuosl.org/pub/mariadb/repo/$MARIADB_MAJOR/debian jessie main" > /etc/apt/sources.list.d/mariadb.list 	&& { 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 13 Sep 2017 11:39:56 GMT
RUN { 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		percona-xtrabackup-24 		socat 	&& rm -rf /var/lib/apt/lists/* 	&& sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf /etc/mysql/conf.d/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 13 Sep 2017 11:39:57 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 13 Sep 2017 11:39:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 13 Sep 2017 11:39:57 GMT
COPY file:d559178e6a2929e36791c6a1fa232dc4ac4298ecc446d38972ee1d2a58e30621 in /usr/local/bin/ 
# Wed, 13 Sep 2017 11:39:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 13 Sep 2017 11:39:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 11:39:58 GMT
EXPOSE 3306/tcp
# Wed, 13 Sep 2017 11:39:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb8d83dece30495d3d9b7c752c4cc36780c9f1aa03571b6a7b9a8850c7d9979`  
		Last Modified: Wed, 13 Sep 2017 09:45:57 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b6ce7b50d3eb246f2ef5fbdd083199d828807abee54d47e3297c866b3d0d2e`  
		Last Modified: Wed, 13 Sep 2017 09:45:56 GMT  
		Size: 1.3 MB (1302934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1d0a3a64e4720c1352929f9133f7beafb5d0ce74c631e7528b4465b1d908fc`  
		Last Modified: Wed, 13 Sep 2017 09:45:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b153f26fb6de368b9a388f803ba658a6bca4023651fa947cd010916cdc852720`  
		Last Modified: Wed, 13 Sep 2017 09:45:56 GMT  
		Size: 6.7 MB (6670574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df63694312ab22de31c1270067830e994ea535641121ca59e18f68003e45605`  
		Last Modified: Wed, 13 Sep 2017 11:42:52 GMT  
		Size: 20.8 KB (20830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efb9b48cc94424cd5c829c8d8ef7872c75f43794e8433351406a9cb43256f5f`  
		Last Modified: Wed, 13 Sep 2017 11:42:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d20c5b1bed262c39f8a93da7152596139e215d2389412318e92c6806d0095`  
		Last Modified: Wed, 13 Sep 2017 11:43:32 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e2d8374be76047111a756b12a7683ed68e6a296f3217c67cbaee7d3c0d544`  
		Last Modified: Wed, 13 Sep 2017 11:44:04 GMT  
		Size: 75.0 MB (74974253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dd69e1aee68b3ffbf748674d5831434cc4476b32dc3a4ff4322d45d2b66910`  
		Last Modified: Wed, 13 Sep 2017 11:43:32 GMT  
		Size: 2.7 KB (2676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b31a5c10d66eec1eeb45f27099adbc2c6653b1fbcffa622941773969b12688`  
		Last Modified: Wed, 13 Sep 2017 11:43:32 GMT  
		Size: 2.6 KB (2551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d7139db154f16b57e0d7a5f70ec8dd06ce153de82ffd7759349353358f1fcd`  
		Last Modified: Wed, 13 Sep 2017 11:43:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
