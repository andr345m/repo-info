<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.0`](#mongo30)
-	[`mongo:3.0.15`](#mongo3015)
-	[`mongo:3.0.15-windowsservercore`](#mongo3015-windowsservercore)
-	[`mongo:3.0-windowsservercore`](#mongo30-windowsservercore)
-	[`mongo:3.2`](#mongo32)
-	[`mongo:3.2.16`](#mongo3216)
-	[`mongo:3.2.16-windowsservercore`](#mongo3216-windowsservercore)
-	[`mongo:3.2-windowsservercore`](#mongo32-windowsservercore)
-	[`mongo:3.4`](#mongo34)
-	[`mongo:3.4.9`](#mongo349)
-	[`mongo:3.4.9-windowsservercore`](#mongo349-windowsservercore)
-	[`mongo:3.4-windowsservercore`](#mongo34-windowsservercore)
-	[`mongo:3.5`](#mongo35)
-	[`mongo:3.5.13`](#mongo3513)
-	[`mongo:3.5.13-windowsservercore`](#mongo3513-windowsservercore)
-	[`mongo:3.5-windowsservercore`](#mongo35-windowsservercore)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:latest`](#mongolatest)
-	[`mongo:unstable`](#mongounstable)
-	[`mongo:unstable-windowsservercore`](#mongounstable-windowsservercore)
-	[`mongo:windowsservercore`](#mongowindowsservercore)

## `mongo:3`

```console
$ docker pull mongo@sha256:0fb08869b40c4b010f38110de7c052aa27f72b96af30a80066f49cdf84573d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3` - linux; amd64

```console
$ docker pull mongo@sha256:2a3c09d75989fce007085be380ae9edfe9dc25668f90ea5737f6953336bc0d84
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132104964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5c173b5d403baaf377eb0af4ad8b3db1952a18308b55d51fe56a7e67808e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:17 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 13 Sep 2017 21:18:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_MAJOR=3.4
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_VERSION=3.4.9
# Wed, 13 Sep 2017 21:18:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:18:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:18:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:18:48 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:18:48 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:18:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:18:49 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:18:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8839dddd1bf8aff82a2809b4534787d721a7f89825d50041975a67d9927e6c`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bbe4efe84371f3d4664bdc7939529223786b08fbd6968bbc2049d9195f583a`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09839ba72070f40726620eba8730b93ad3c88b1860aa1e22077ccb29e446c405`  
		Last Modified: Wed, 13 Sep 2017 21:21:13 GMT  
		Size: 98.5 MB (98477908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e47fbec441c937fbdbd3d6f87eb35d2ae3913eb256399d25d34b71c648a2`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02774c69fefaa7a7eebcdbfa26d4b2cd3a2f8fafc467166ac52c8f0d8e751c93`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17a1e0f668c78e1304d0f24ca13a924ab2da4e4cd003b278c78659c0190376`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0`

```console
$ docker pull mongo@sha256:caee88655df28cb7b9118fa848a46fd1aab7681de175ad3ff7c0f6fab1ea8a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.0` - linux; amd64

```console
$ docker pull mongo@sha256:9c3936c36ce21fc5e7fe30f11c27a42a64bdd6f86470463c3f4ede1c69f4560e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84817189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bc2c0eb5c1a01f28090825da13f081d06e932f08146dbd5402d323f7c06ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:42:21 GMT
ADD file:d8e4b007ff77e115dfa0e34b040d0e3d1edd716458d2cf8598fbceaf1c012a5a in / 
# Wed, 13 Sep 2017 08:42:21 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:15:23 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian wheezy-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 13 Sep 2017 21:15:35 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:15:36 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:15:47 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:15:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:15:48 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Wed, 13 Sep 2017 21:15:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:15:49 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:15:49 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:15:49 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:15:50 GMT
ENV MONGO_MAJOR=3.0
# Wed, 13 Sep 2017 21:15:50 GMT
ENV MONGO_VERSION=3.0.15
# Wed, 13 Sep 2017 21:15:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian wheezy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:16:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:16:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:16:01 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:16:02 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:16:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:16:03 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:16:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1b2cb524b2ec19dd2a539218233a5ef7a1c94bcda95c6be54d3ebdb85fa8d85f`  
		Last Modified: Thu, 07 Sep 2017 23:24:30 GMT  
		Size: 19.2 MB (19159087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95629a9af962ddb9c6b8533ec97a7257924b27315d45a75876c66ab05373754f`  
		Last Modified: Wed, 13 Sep 2017 21:19:50 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9344b5f35f1b87838475600efb482bd906aa59e9d0803c44b1b6ba9469bac9a5`  
		Last Modified: Wed, 13 Sep 2017 21:19:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3358141a975ed47dfdaa395646b29f04033afa36684aabc3009dc5fa2e139087`  
		Last Modified: Wed, 13 Sep 2017 21:19:46 GMT  
		Size: 2.7 MB (2660799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b48dda540b451dd4ebaf0e79d86b1d92ae7e1387acbd1a2b3152715e0f7d92`  
		Last Modified: Wed, 13 Sep 2017 21:19:46 GMT  
		Size: 1.1 MB (1103222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446875dc015b7687e559aa9439aa9d1d92526819c03b858d952be4e815a0886`  
		Last Modified: Wed, 13 Sep 2017 21:19:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8c44aed8d466ef452d65bb61aba6f44ef56bfc6b9069102b5a7c96914b3cd8`  
		Last Modified: Wed, 13 Sep 2017 21:19:41 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad375044a74f39e254825d57d9e74641439cc6e8acc9f435acca053e93d82b9`  
		Last Modified: Wed, 13 Sep 2017 21:19:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49502d6abdae2cd4cf2ed2680358f008f04a859c73d828cc57ca051eabf7fb38`  
		Last Modified: Wed, 13 Sep 2017 21:19:55 GMT  
		Size: 61.9 MB (61886355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960bccdc96cc7b66b760d8449979d2a81c2544669b013d0b2d38d5ed441eb39e`  
		Last Modified: Wed, 13 Sep 2017 21:19:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77602a8f49542a431c56f8514bf0aa5f08a4c7b071bf9fa1454f4ced9da1491f`  
		Last Modified: Wed, 13 Sep 2017 21:19:37 GMT  
		Size: 3.1 KB (3111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12640adf9c4186e8c51a0e6b4b08bd5b296852d06843a14f6d5003d60c382dcd`  
		Last Modified: Wed, 13 Sep 2017 21:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0.15`

```console
$ docker pull mongo@sha256:caee88655df28cb7b9118fa848a46fd1aab7681de175ad3ff7c0f6fab1ea8a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.0.15` - linux; amd64

```console
$ docker pull mongo@sha256:9c3936c36ce21fc5e7fe30f11c27a42a64bdd6f86470463c3f4ede1c69f4560e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84817189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bc2c0eb5c1a01f28090825da13f081d06e932f08146dbd5402d323f7c06ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:42:21 GMT
ADD file:d8e4b007ff77e115dfa0e34b040d0e3d1edd716458d2cf8598fbceaf1c012a5a in / 
# Wed, 13 Sep 2017 08:42:21 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:15:23 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian wheezy-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 13 Sep 2017 21:15:35 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:15:36 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:15:47 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:15:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:15:48 GMT
ENV GPG_KEYS=492EAFE8CD016A07919F1D2B9ECBEC467F0CEB10
# Wed, 13 Sep 2017 21:15:49 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:15:49 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:15:49 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:15:49 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:15:50 GMT
ENV MONGO_MAJOR=3.0
# Wed, 13 Sep 2017 21:15:50 GMT
ENV MONGO_VERSION=3.0.15
# Wed, 13 Sep 2017 21:15:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian wheezy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:16:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:16:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:16:01 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:16:02 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:16:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:16:03 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:16:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1b2cb524b2ec19dd2a539218233a5ef7a1c94bcda95c6be54d3ebdb85fa8d85f`  
		Last Modified: Thu, 07 Sep 2017 23:24:30 GMT  
		Size: 19.2 MB (19159087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95629a9af962ddb9c6b8533ec97a7257924b27315d45a75876c66ab05373754f`  
		Last Modified: Wed, 13 Sep 2017 21:19:50 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9344b5f35f1b87838475600efb482bd906aa59e9d0803c44b1b6ba9469bac9a5`  
		Last Modified: Wed, 13 Sep 2017 21:19:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3358141a975ed47dfdaa395646b29f04033afa36684aabc3009dc5fa2e139087`  
		Last Modified: Wed, 13 Sep 2017 21:19:46 GMT  
		Size: 2.7 MB (2660799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b48dda540b451dd4ebaf0e79d86b1d92ae7e1387acbd1a2b3152715e0f7d92`  
		Last Modified: Wed, 13 Sep 2017 21:19:46 GMT  
		Size: 1.1 MB (1103222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8446875dc015b7687e559aa9439aa9d1d92526819c03b858d952be4e815a0886`  
		Last Modified: Wed, 13 Sep 2017 21:19:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8c44aed8d466ef452d65bb61aba6f44ef56bfc6b9069102b5a7c96914b3cd8`  
		Last Modified: Wed, 13 Sep 2017 21:19:41 GMT  
		Size: 2.0 KB (2044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad375044a74f39e254825d57d9e74641439cc6e8acc9f435acca053e93d82b9`  
		Last Modified: Wed, 13 Sep 2017 21:19:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49502d6abdae2cd4cf2ed2680358f008f04a859c73d828cc57ca051eabf7fb38`  
		Last Modified: Wed, 13 Sep 2017 21:19:55 GMT  
		Size: 61.9 MB (61886355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960bccdc96cc7b66b760d8449979d2a81c2544669b013d0b2d38d5ed441eb39e`  
		Last Modified: Wed, 13 Sep 2017 21:19:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77602a8f49542a431c56f8514bf0aa5f08a4c7b071bf9fa1454f4ced9da1491f`  
		Last Modified: Wed, 13 Sep 2017 21:19:37 GMT  
		Size: 3.1 KB (3111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12640adf9c4186e8c51a0e6b4b08bd5b296852d06843a14f6d5003d60c382dcd`  
		Last Modified: Wed, 13 Sep 2017 21:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0.15-windowsservercore`

```console
$ docker pull mongo@sha256:7c02d8cb44155531dd06f382ee7d8085d61a04667e6e4ff44855c6e722c7ce5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:3.0.15-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:72ce51c8b42d816644de933a0039ef1bdd2fab6e504b17a324c435e934ce5508
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5374594967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4064544d209b639fefb97b7228035a5e450486ba6d6099604fc644293ee6d1b`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Aug 2017 23:26:27 GMT
ENV MONGO_VERSION=3.0.15
# Wed, 09 Aug 2017 23:26:29 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.15-signed.msi
# Wed, 09 Aug 2017 23:26:31 GMT
ENV MONGO_DOWNLOAD_SHA256=0a10cb87da164df7a1d31180d2ea1f3b096dda6e3d7b9f95c184ef953a1677bb
# Wed, 09 Aug 2017 23:27:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Aug 2017 23:27:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Aug 2017 23:27:22 GMT
EXPOSE 27017/tcp
# Wed, 09 Aug 2017 23:27:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358f7525f35ef975b00f5befc1ecca513a5a2825d5c35f5a73ef742e27730e4b`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be84f10938eb7737c7539aa14060c02ca640a97b842fd45513d26468543f29f`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e685bfc300c53104b2bd6da75da3496d414be74073e44948ff56debc40ef31`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f845ecff39ee85d05b53864084a3721c016d11a80e92e8cc2405a39f120d20`  
		Last Modified: Wed, 09 Aug 2017 23:31:33 GMT  
		Size: 46.9 MB (46902236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5491943309ee39fa354a7b6f5a1027c5ef8832db1fb6a03a1db75dd51af3c0`  
		Last Modified: Wed, 09 Aug 2017 23:31:24 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6e44a90b089dec68db52f44a59ad83e11d7a17c5ada34b587c8b53cadccf8c`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dcc1b0d176ac33da3bf5522ad880898b38ca55d9397d50ac62b26a5a9fb20`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.0-windowsservercore`

```console
$ docker pull mongo@sha256:7c02d8cb44155531dd06f382ee7d8085d61a04667e6e4ff44855c6e722c7ce5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:3.0-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:72ce51c8b42d816644de933a0039ef1bdd2fab6e504b17a324c435e934ce5508
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5374594967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4064544d209b639fefb97b7228035a5e450486ba6d6099604fc644293ee6d1b`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Aug 2017 23:26:27 GMT
ENV MONGO_VERSION=3.0.15
# Wed, 09 Aug 2017 23:26:29 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.0.15-signed.msi
# Wed, 09 Aug 2017 23:26:31 GMT
ENV MONGO_DOWNLOAD_SHA256=0a10cb87da164df7a1d31180d2ea1f3b096dda6e3d7b9f95c184ef953a1677bb
# Wed, 09 Aug 2017 23:27:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Aug 2017 23:27:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Aug 2017 23:27:22 GMT
EXPOSE 27017/tcp
# Wed, 09 Aug 2017 23:27:25 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358f7525f35ef975b00f5befc1ecca513a5a2825d5c35f5a73ef742e27730e4b`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be84f10938eb7737c7539aa14060c02ca640a97b842fd45513d26468543f29f`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e685bfc300c53104b2bd6da75da3496d414be74073e44948ff56debc40ef31`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f845ecff39ee85d05b53864084a3721c016d11a80e92e8cc2405a39f120d20`  
		Last Modified: Wed, 09 Aug 2017 23:31:33 GMT  
		Size: 46.9 MB (46902236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5491943309ee39fa354a7b6f5a1027c5ef8832db1fb6a03a1db75dd51af3c0`  
		Last Modified: Wed, 09 Aug 2017 23:31:24 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6e44a90b089dec68db52f44a59ad83e11d7a17c5ada34b587c8b53cadccf8c`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dcc1b0d176ac33da3bf5522ad880898b38ca55d9397d50ac62b26a5a9fb20`  
		Last Modified: Wed, 09 Aug 2017 23:31:23 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2`

```console
$ docker pull mongo@sha256:fcd2388d73ff3d93d0c8cc7536c4759e345dc051308147a2523cc7693cd010cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.2` - linux; amd64

```console
$ docker pull mongo@sha256:eb0580b320a21463fb5ddfc8b7a719ef56885f9011093788557a65c39dded1aa
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104452230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16149f61df5797019239eb4497034276573961559280f68c5ce66e43a0ce4d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:16:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates			jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:16:27 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:16:54 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:16:54 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:16:54 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Wed, 13 Sep 2017 21:17:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:17:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:17:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:17:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:17:00 GMT
ENV MONGO_MAJOR=3.2
# Wed, 13 Sep 2017 21:17:01 GMT
ENV MONGO_VERSION=3.2.16
# Wed, 13 Sep 2017 21:17:01 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:17:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:17:26 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:17:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:17:27 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:17:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2017979d193f1a628fb4cf72fc1e3249b3276377ba970ecba6458815a4c9202d`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.4 MB (2397898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d21d92a41771207e33e7b7b64e4b2393c60ed7687d7b4bf7d5a2dffa4d3409c`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 1.1 MB (1108732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63237591b1880bf0618026bc927b2292778a5f6f5188e64acdc15d4bae3e97c`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034b34661ee5208f49c7eb0c0c6e598a6e5526d05b5163057585beb53b97c11`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 3.1 KB (3072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9199b5efbcce9e2d92b5c8684876dcf7ad6fcf6163fcbf997b6a8bf7991e6df`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c2318c947cfb64ddb484cc7a9bc8cab823766bbbdacd1a6b6a287adbdf2636`  
		Last Modified: Wed, 13 Sep 2017 21:20:24 GMT  
		Size: 70.8 MB (70823588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3155ef795942434d8417738d31a9b76f0d2e9648fe1cd81a07e3648ae921d8b5`  
		Last Modified: Wed, 13 Sep 2017 21:20:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7ad9295b911f259c9136d9109eb94daa5e2f07a91992ebfc59fb7bf097acdf`  
		Last Modified: Wed, 13 Sep 2017 21:20:09 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c06af7df467d6ae7dbf9349393bdc9b0d88685e6efcf2e073cd3a7fe337826`  
		Last Modified: Wed, 13 Sep 2017 21:20:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.16`

```console
$ docker pull mongo@sha256:fcd2388d73ff3d93d0c8cc7536c4759e345dc051308147a2523cc7693cd010cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.2.16` - linux; amd64

```console
$ docker pull mongo@sha256:eb0580b320a21463fb5ddfc8b7a719ef56885f9011093788557a65c39dded1aa
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104452230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16149f61df5797019239eb4497034276573961559280f68c5ce66e43a0ce4d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:16:27 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates			jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:16:27 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:16:54 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:16:54 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:16:54 GMT
ENV GPG_KEYS=DFFA3DCF326E302C4787673A01C4E7FAAAB2461C 	42F3E95A2C4F08279C4960ADD68FA50FEA312927
# Wed, 13 Sep 2017 21:17:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:17:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:17:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:17:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:17:00 GMT
ENV MONGO_MAJOR=3.2
# Wed, 13 Sep 2017 21:17:01 GMT
ENV MONGO_VERSION=3.2.16
# Wed, 13 Sep 2017 21:17:01 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:17:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:17:26 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:17:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:17:27 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:17:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2017979d193f1a628fb4cf72fc1e3249b3276377ba970ecba6458815a4c9202d`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.4 MB (2397898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d21d92a41771207e33e7b7b64e4b2393c60ed7687d7b4bf7d5a2dffa4d3409c`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 1.1 MB (1108732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63237591b1880bf0618026bc927b2292778a5f6f5188e64acdc15d4bae3e97c`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034b34661ee5208f49c7eb0c0c6e598a6e5526d05b5163057585beb53b97c11`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 3.1 KB (3072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9199b5efbcce9e2d92b5c8684876dcf7ad6fcf6163fcbf997b6a8bf7991e6df`  
		Last Modified: Wed, 13 Sep 2017 21:20:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c2318c947cfb64ddb484cc7a9bc8cab823766bbbdacd1a6b6a287adbdf2636`  
		Last Modified: Wed, 13 Sep 2017 21:20:24 GMT  
		Size: 70.8 MB (70823588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3155ef795942434d8417738d31a9b76f0d2e9648fe1cd81a07e3648ae921d8b5`  
		Last Modified: Wed, 13 Sep 2017 21:20:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7ad9295b911f259c9136d9109eb94daa5e2f07a91992ebfc59fb7bf097acdf`  
		Last Modified: Wed, 13 Sep 2017 21:20:09 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c06af7df467d6ae7dbf9349393bdc9b0d88685e6efcf2e073cd3a7fe337826`  
		Last Modified: Wed, 13 Sep 2017 21:20:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2.16-windowsservercore`

```console
$ docker pull mongo@sha256:ce29600bc4f2434ef749bbd26571a57e0e67993f3dacf5ff5fb88d1394ed5324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:3.2.16-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:54812ed05c0b7aa54cfebcdce99b0e411e586b6807564eede630bc023ff6e3af
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5380576554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fda73086b96978d2bb579f273261bf1359bbcb6de576ac1b0a0c1b3d7c5d560`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Aug 2017 23:27:28 GMT
ENV MONGO_VERSION=3.2.16
# Wed, 09 Aug 2017 23:27:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.16-signed.msi
# Wed, 09 Aug 2017 23:27:33 GMT
ENV MONGO_DOWNLOAD_SHA256=d27765ea1042f83b8a34cd60758c7ebf037520b9fb0e7c0c972e8256ee717829
# Wed, 09 Aug 2017 23:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Aug 2017 23:28:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Aug 2017 23:28:22 GMT
EXPOSE 27017/tcp
# Wed, 09 Aug 2017 23:28:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f81e684e1fae36e71fbb56768612bc521935935dc467dd156c0ce143fcc384b`  
		Last Modified: Wed, 09 Aug 2017 23:31:52 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3207f3020275df8c87dc381f53c6b5fe64c8944879c517af8443e20fba58328b`  
		Last Modified: Wed, 09 Aug 2017 23:31:52 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92451224920586ad919138ef57f4f779d94b3c3feb1e0767b05e0397e378a97d`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3076b9cffa8f6b3fb3443a9b81db96924ea48e2da14febafc5a0c88587b2d`  
		Last Modified: Wed, 09 Aug 2017 23:31:55 GMT  
		Size: 52.9 MB (52883816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf16f812ebb17d481cdf791a674d801e06673f930d7f450877375abdeba69a8`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d63dfcbc390afaa99e1db4f24505fbfab3719de9caca6a4ae32d82f234374f`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58158c49402aedd4a1c1877eda2e5eaf76dc19033abc873850875f48f3d75db`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.2-windowsservercore`

```console
$ docker pull mongo@sha256:ce29600bc4f2434ef749bbd26571a57e0e67993f3dacf5ff5fb88d1394ed5324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:3.2-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:54812ed05c0b7aa54cfebcdce99b0e411e586b6807564eede630bc023ff6e3af
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5380576554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fda73086b96978d2bb579f273261bf1359bbcb6de576ac1b0a0c1b3d7c5d560`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Aug 2017 23:27:28 GMT
ENV MONGO_VERSION=3.2.16
# Wed, 09 Aug 2017 23:27:30 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.2.16-signed.msi
# Wed, 09 Aug 2017 23:27:33 GMT
ENV MONGO_DOWNLOAD_SHA256=d27765ea1042f83b8a34cd60758c7ebf037520b9fb0e7c0c972e8256ee717829
# Wed, 09 Aug 2017 23:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Aug 2017 23:28:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Aug 2017 23:28:22 GMT
EXPOSE 27017/tcp
# Wed, 09 Aug 2017 23:28:26 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f81e684e1fae36e71fbb56768612bc521935935dc467dd156c0ce143fcc384b`  
		Last Modified: Wed, 09 Aug 2017 23:31:52 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3207f3020275df8c87dc381f53c6b5fe64c8944879c517af8443e20fba58328b`  
		Last Modified: Wed, 09 Aug 2017 23:31:52 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92451224920586ad919138ef57f4f779d94b3c3feb1e0767b05e0397e378a97d`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d3076b9cffa8f6b3fb3443a9b81db96924ea48e2da14febafc5a0c88587b2d`  
		Last Modified: Wed, 09 Aug 2017 23:31:55 GMT  
		Size: 52.9 MB (52883816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf16f812ebb17d481cdf791a674d801e06673f930d7f450877375abdeba69a8`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d63dfcbc390afaa99e1db4f24505fbfab3719de9caca6a4ae32d82f234374f`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58158c49402aedd4a1c1877eda2e5eaf76dc19033abc873850875f48f3d75db`  
		Last Modified: Wed, 09 Aug 2017 23:31:43 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4`

```console
$ docker pull mongo@sha256:0fb08869b40c4b010f38110de7c052aa27f72b96af30a80066f49cdf84573d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.4` - linux; amd64

```console
$ docker pull mongo@sha256:2a3c09d75989fce007085be380ae9edfe9dc25668f90ea5737f6953336bc0d84
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132104964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5c173b5d403baaf377eb0af4ad8b3db1952a18308b55d51fe56a7e67808e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:17 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 13 Sep 2017 21:18:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_MAJOR=3.4
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_VERSION=3.4.9
# Wed, 13 Sep 2017 21:18:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:18:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:18:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:18:48 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:18:48 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:18:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:18:49 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:18:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8839dddd1bf8aff82a2809b4534787d721a7f89825d50041975a67d9927e6c`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bbe4efe84371f3d4664bdc7939529223786b08fbd6968bbc2049d9195f583a`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09839ba72070f40726620eba8730b93ad3c88b1860aa1e22077ccb29e446c405`  
		Last Modified: Wed, 13 Sep 2017 21:21:13 GMT  
		Size: 98.5 MB (98477908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e47fbec441c937fbdbd3d6f87eb35d2ae3913eb256399d25d34b71c648a2`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02774c69fefaa7a7eebcdbfa26d4b2cd3a2f8fafc467166ac52c8f0d8e751c93`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17a1e0f668c78e1304d0f24ca13a924ab2da4e4cd003b278c78659c0190376`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.9`

```console
$ docker pull mongo@sha256:0fb08869b40c4b010f38110de7c052aa27f72b96af30a80066f49cdf84573d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.4.9` - linux; amd64

```console
$ docker pull mongo@sha256:2a3c09d75989fce007085be380ae9edfe9dc25668f90ea5737f6953336bc0d84
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132104964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5c173b5d403baaf377eb0af4ad8b3db1952a18308b55d51fe56a7e67808e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:17 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 13 Sep 2017 21:18:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_MAJOR=3.4
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_VERSION=3.4.9
# Wed, 13 Sep 2017 21:18:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:18:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:18:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:18:48 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:18:48 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:18:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:18:49 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:18:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8839dddd1bf8aff82a2809b4534787d721a7f89825d50041975a67d9927e6c`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bbe4efe84371f3d4664bdc7939529223786b08fbd6968bbc2049d9195f583a`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09839ba72070f40726620eba8730b93ad3c88b1860aa1e22077ccb29e446c405`  
		Last Modified: Wed, 13 Sep 2017 21:21:13 GMT  
		Size: 98.5 MB (98477908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e47fbec441c937fbdbd3d6f87eb35d2ae3913eb256399d25d34b71c648a2`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02774c69fefaa7a7eebcdbfa26d4b2cd3a2f8fafc467166ac52c8f0d8e751c93`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17a1e0f668c78e1304d0f24ca13a924ab2da4e4cd003b278c78659c0190376`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.9-windowsservercore`

**does not exist** (yet?)

## `mongo:3.4-windowsservercore`

```console
$ docker pull mongo@sha256:0d13a70f34c00e8603a134814e18ece718f625e09927d75bc5926ec53fa45a3a
```

-	Platforms:
	-	windows; amd64

### `mongo:3.4-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5358350943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb915cddd00568a782ad6abedc4684e4b22a22affc9b0d40e059c844151896`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Jul 2017 22:35:45 GMT
RUN Install update 10.0.14393.1480
# Fri, 28 Jul 2017 18:55:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Aug 2017 17:59:43 GMT
ENV MONGO_VERSION=3.4.7
# Tue, 08 Aug 2017 17:59:45 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.7-signed.msi
# Tue, 08 Aug 2017 17:59:48 GMT
ENV MONGO_DOWNLOAD_SHA256=baf43fcf28ff8c486d6af9036c0f15e96c0663a222626aed97d1e48c143ab865
# Tue, 08 Aug 2017 18:00:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Aug 2017 18:00:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Aug 2017 18:00:57 GMT
EXPOSE 27017/tcp
# Tue, 08 Aug 2017 18:01:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e29afd68a947fc566b71a432a6df352eea9e59eb221c3cb9f6bf5a4df206571e`  
		Size: 1.2 GB (1225343627 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2e2fab7692964a46adf839b6fe66a115f2c7617697a351e412c382936629b9f`  
		Last Modified: Fri, 28 Jul 2017 19:01:16 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaabfc0a85fd64385ab0664b34279ce72e6bff4a6b8c58dedd53ad4f66c9fb2`  
		Last Modified: Tue, 08 Aug 2017 18:01:28 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508dd55adcea973a45acc8f9981b23f137b3a844120e591716a09ddb94504ce9`  
		Last Modified: Tue, 08 Aug 2017 18:01:26 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161c225da1cbf013946d3d586072a48bf356124d19c893e8fee6bd8e10e0b702`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048633be839a58e73ee0e1fe673e1f3ca264f3d05ce16daf62e126cfb6755671`  
		Last Modified: Tue, 08 Aug 2017 18:01:32 GMT  
		Size: 63.0 MB (63012874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e86db3b2a06546f19358f223be6d63879a86dbc96958d34df29b9199469a74e`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20595e6fd7b3a5b7b9d29f58ca5a453b670fe771d12bae4831c84a19224bf1d`  
		Last Modified: Tue, 08 Aug 2017 18:01:19 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762fc90c18a94331366cc3d336c5721199149789dbb0ca684c0ad9f5bea44b8d`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5`

```console
$ docker pull mongo@sha256:6b97da14c7db7bc5b1e5a38493ced16f0b433e9f494cee4f90bc422e09119ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.5` - linux; amd64

```console
$ docker pull mongo@sha256:0cad107d1bf9534e23f7367c2325d17cfff48b90d3baf94e8194ad70d7567621
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132812512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d767208390d025057c8cd246bec4f733b22c4ab74106c3559a3d63fcf54d4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 13 Sep 2017 21:18:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:57 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Wed, 13 Sep 2017 21:18:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_MAJOR=3.5
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_VERSION=3.5.13
# Wed, 13 Sep 2017 21:18:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:19:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:19:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:19:27 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:19:28 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:19:28 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:19:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7793924ac6bfcc021dee9c2474c4eef4ac81ccff443e994d5fe8182b384827d`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617c3159d28f586728d4b1e6d1379c0a9215ff5afeefb2fd7409cf33f3f5678`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3d90f438196687c40b075a5c41d6dbfc3b21df0233e0c01e7e6250f91276b4`  
		Last Modified: Wed, 13 Sep 2017 21:21:52 GMT  
		Size: 99.2 MB (99185509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9d70f0f906f6f0bf5c18ca667881f9e8899f9cfa4fb957df352504643c6744`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5530164457e317b27ba198fe8e14368c6e4a88b0d8ba6f520e425ca5f2ce60b6`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 3.2 KB (3175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5.13`

```console
$ docker pull mongo@sha256:6b97da14c7db7bc5b1e5a38493ced16f0b433e9f494cee4f90bc422e09119ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:3.5.13` - linux; amd64

```console
$ docker pull mongo@sha256:0cad107d1bf9534e23f7367c2325d17cfff48b90d3baf94e8194ad70d7567621
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132812512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d767208390d025057c8cd246bec4f733b22c4ab74106c3559a3d63fcf54d4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 13 Sep 2017 21:18:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:57 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Wed, 13 Sep 2017 21:18:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_MAJOR=3.5
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_VERSION=3.5.13
# Wed, 13 Sep 2017 21:18:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:19:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:19:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:19:27 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:19:28 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:19:28 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:19:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7793924ac6bfcc021dee9c2474c4eef4ac81ccff443e994d5fe8182b384827d`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617c3159d28f586728d4b1e6d1379c0a9215ff5afeefb2fd7409cf33f3f5678`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3d90f438196687c40b075a5c41d6dbfc3b21df0233e0c01e7e6250f91276b4`  
		Last Modified: Wed, 13 Sep 2017 21:21:52 GMT  
		Size: 99.2 MB (99185509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9d70f0f906f6f0bf5c18ca667881f9e8899f9cfa4fb957df352504643c6744`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5530164457e317b27ba198fe8e14368c6e4a88b0d8ba6f520e425ca5f2ce60b6`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 3.2 KB (3175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.5.13-windowsservercore`

**does not exist** (yet?)

## `mongo:3.5-windowsservercore`

```console
$ docker pull mongo@sha256:3ef6fae398cb580f74b6e422a7e4d33ab7c12c351b940b9df06af015515938f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:3.5-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:9f5cd919b90498dad0e30842caf73daeb10c3d8b7feb4baa135f7e3f54b75149
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5392612175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc0766c32354cd8f3e8eecaaf9e56cb3358c05860d7ea1ef7b67b77e7aa6034`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 24 Aug 2017 01:36:32 GMT
ENV MONGO_VERSION=3.5.12
# Thu, 24 Aug 2017 01:36:34 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.5.12-signed.msi
# Thu, 24 Aug 2017 01:36:37 GMT
ENV MONGO_DOWNLOAD_SHA256=15cedbca560a65dc3362a42a070c4f110e1b8cb20ebcd5e61bd795f673ededdc
# Thu, 24 Aug 2017 01:37:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 24 Aug 2017 01:37:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 24 Aug 2017 01:37:46 GMT
EXPOSE 27017/tcp
# Thu, 24 Aug 2017 01:37:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c898968f529278c0af8db05709183928d28f86024f198eaa7ed10269c3a2e65c`  
		Last Modified: Thu, 24 Aug 2017 01:38:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1a7ee713204b5839c54f61f60404498f3257cc80f5d5cebc89481740a2ecdc`  
		Last Modified: Thu, 24 Aug 2017 01:38:27 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce1c2768ad669f71bfe571800bece463fbc4573b7cd23f9fe9265832c757a6e`  
		Last Modified: Thu, 24 Aug 2017 01:38:17 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31a810382195d4deab495bbd2492395698a029aca8a86e202bda4ba25b6eb51`  
		Last Modified: Thu, 24 Aug 2017 01:38:30 GMT  
		Size: 64.9 MB (64919441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08929e16eef1f65703588e8b59447f4536cbc39f076830e8fa5259fb27bb4d86`  
		Last Modified: Thu, 24 Aug 2017 01:38:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb5a438b35a85fa9c6e06382b9815beb3ac2fa76179c8b99eee8ff47b9e555`  
		Last Modified: Thu, 24 Aug 2017 01:38:18 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e02f5fe2f1c2e58c1497651ece6f4e01ac3c8ac16595b945217b278a064a727`  
		Last Modified: Thu, 24 Aug 2017 01:38:18 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:0d13a70f34c00e8603a134814e18ece718f625e09927d75bc5926ec53fa45a3a
```

-	Platforms:
	-	windows; amd64

### `mongo:3-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5358350943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb915cddd00568a782ad6abedc4684e4b22a22affc9b0d40e059c844151896`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Jul 2017 22:35:45 GMT
RUN Install update 10.0.14393.1480
# Fri, 28 Jul 2017 18:55:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Aug 2017 17:59:43 GMT
ENV MONGO_VERSION=3.4.7
# Tue, 08 Aug 2017 17:59:45 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.7-signed.msi
# Tue, 08 Aug 2017 17:59:48 GMT
ENV MONGO_DOWNLOAD_SHA256=baf43fcf28ff8c486d6af9036c0f15e96c0663a222626aed97d1e48c143ab865
# Tue, 08 Aug 2017 18:00:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Aug 2017 18:00:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Aug 2017 18:00:57 GMT
EXPOSE 27017/tcp
# Tue, 08 Aug 2017 18:01:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e29afd68a947fc566b71a432a6df352eea9e59eb221c3cb9f6bf5a4df206571e`  
		Size: 1.2 GB (1225343627 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2e2fab7692964a46adf839b6fe66a115f2c7617697a351e412c382936629b9f`  
		Last Modified: Fri, 28 Jul 2017 19:01:16 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaabfc0a85fd64385ab0664b34279ce72e6bff4a6b8c58dedd53ad4f66c9fb2`  
		Last Modified: Tue, 08 Aug 2017 18:01:28 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508dd55adcea973a45acc8f9981b23f137b3a844120e591716a09ddb94504ce9`  
		Last Modified: Tue, 08 Aug 2017 18:01:26 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161c225da1cbf013946d3d586072a48bf356124d19c893e8fee6bd8e10e0b702`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048633be839a58e73ee0e1fe673e1f3ca264f3d05ce16daf62e126cfb6755671`  
		Last Modified: Tue, 08 Aug 2017 18:01:32 GMT  
		Size: 63.0 MB (63012874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e86db3b2a06546f19358f223be6d63879a86dbc96958d34df29b9199469a74e`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20595e6fd7b3a5b7b9d29f58ca5a453b670fe771d12bae4831c84a19224bf1d`  
		Last Modified: Tue, 08 Aug 2017 18:01:19 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762fc90c18a94331366cc3d336c5721199149789dbb0ca684c0ad9f5bea44b8d`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:0fb08869b40c4b010f38110de7c052aa27f72b96af30a80066f49cdf84573d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:2a3c09d75989fce007085be380ae9edfe9dc25668f90ea5737f6953336bc0d84
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132104964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f5c173b5d403baaf377eb0af4ad8b3db1952a18308b55d51fe56a7e67808e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:17 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 13 Sep 2017 21:18:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Sep 2017 21:18:22 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_MAJOR=3.4
# Wed, 13 Sep 2017 21:18:22 GMT
ENV MONGO_VERSION=3.4.9
# Wed, 13 Sep 2017 21:18:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:18:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:18:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:18:48 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:18:48 GMT
COPY file:dbebaf4376a8d615e05b80e0bc26a2dfc5f8f8687b16ab47e64928fb5a00498d in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:18:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 13 Sep 2017 21:18:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:18:49 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:18:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8839dddd1bf8aff82a2809b4534787d721a7f89825d50041975a67d9927e6c`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bbe4efe84371f3d4664bdc7939529223786b08fbd6968bbc2049d9195f583a`  
		Last Modified: Wed, 13 Sep 2017 21:20:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09839ba72070f40726620eba8730b93ad3c88b1860aa1e22077ccb29e446c405`  
		Last Modified: Wed, 13 Sep 2017 21:21:13 GMT  
		Size: 98.5 MB (98477908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c28e47fbec441c937fbdbd3d6f87eb35d2ae3913eb256399d25d34b71c648a2`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02774c69fefaa7a7eebcdbfa26d4b2cd3a2f8fafc467166ac52c8f0d8e751c93`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 3.1 KB (3113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e17a1e0f668c78e1304d0f24ca13a924ab2da4e4cd003b278c78659c0190376`  
		Last Modified: Wed, 13 Sep 2017 21:20:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:unstable`

```console
$ docker pull mongo@sha256:6b97da14c7db7bc5b1e5a38493ced16f0b433e9f494cee4f90bc422e09119ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mongo:unstable` - linux; amd64

```console
$ docker pull mongo@sha256:0cad107d1bf9534e23f7367c2325d17cfff48b90d3baf94e8194ad70d7567621
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132812512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d767208390d025057c8cd246bec4f733b22c4ab74106c3559a3d63fcf54d4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod","--bind_ip_all"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 21:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 13 Sep 2017 21:17:50 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 21:17:50 GMT
ENV GOSU_VERSION=1.7
# Wed, 13 Sep 2017 21:18:16 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove wget
# Wed, 13 Sep 2017 21:18:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 13 Sep 2017 21:18:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 13 Sep 2017 21:18:57 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 13 Sep 2017 21:18:57 GMT
ARG MONGO_PACKAGE=mongodb-org-unstable
# Wed, 13 Sep 2017 21:18:58 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_PACKAGE=mongodb-org-unstable MONGO_REPO=repo.mongodb.org
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_MAJOR=3.5
# Wed, 13 Sep 2017 21:18:58 GMT
ENV MONGO_VERSION=3.5.13
# Wed, 13 Sep 2017 21:18:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/debian jessie/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR main" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 13 Sep 2017 21:19:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 13 Sep 2017 21:19:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 13 Sep 2017 21:19:27 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Sep 2017 21:19:28 GMT
COPY file:2693b7d26a4d17558bb637a0ad2c43c3be68788377b0e9eb105cd67726d4b645 in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:19:28 GMT
EXPOSE 27017/tcp
# Wed, 13 Sep 2017 21:19:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804fbd93397b69eb5743a54bff7523238dc68dda7a2c9b73a226eca5bc25cc2`  
		Last Modified: Wed, 13 Sep 2017 21:20:15 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aea8781e40b5e67b16bc15553de2191010be5871a58d429868f48f38978335`  
		Last Modified: Wed, 13 Sep 2017 21:20:49 GMT  
		Size: 2.4 MB (2397922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bb0fb15879d49913e59eda1824d86f724eb18d1e1384ede573ec3642d0ea7e`  
		Last Modified: Wed, 13 Sep 2017 21:20:48 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf794b7d8d7e68799bb699d3df7ce379dcb3cbc282c4016f80d6f012e4544f`  
		Last Modified: Wed, 13 Sep 2017 21:20:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7793924ac6bfcc021dee9c2474c4eef4ac81ccff443e994d5fe8182b384827d`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b617c3159d28f586728d4b1e6d1379c0a9215ff5afeefb2fd7409cf33f3f5678`  
		Last Modified: Wed, 13 Sep 2017 21:21:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3d90f438196687c40b075a5c41d6dbfc3b21df0233e0c01e7e6250f91276b4`  
		Last Modified: Wed, 13 Sep 2017 21:21:52 GMT  
		Size: 99.2 MB (99185509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9d70f0f906f6f0bf5c18ca667881f9e8899f9cfa4fb957df352504643c6744`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5530164457e317b27ba198fe8e14368c6e4a88b0d8ba6f520e425ca5f2ce60b6`  
		Last Modified: Wed, 13 Sep 2017 21:21:35 GMT  
		Size: 3.2 KB (3175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:unstable-windowsservercore`

```console
$ docker pull mongo@sha256:3ef6fae398cb580f74b6e422a7e4d33ab7c12c351b940b9df06af015515938f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `mongo:unstable-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull mongo@sha256:9f5cd919b90498dad0e30842caf73daeb10c3d8b7feb4baa135f7e3f54b75149
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5392612175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc0766c32354cd8f3e8eecaaf9e56cb3358c05860d7ea1ef7b67b77e7aa6034`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 24 Aug 2017 01:36:32 GMT
ENV MONGO_VERSION=3.5.12
# Thu, 24 Aug 2017 01:36:34 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.5.12-signed.msi
# Thu, 24 Aug 2017 01:36:37 GMT
ENV MONGO_DOWNLOAD_SHA256=15cedbca560a65dc3362a42a070c4f110e1b8cb20ebcd5e61bd795f673ededdc
# Thu, 24 Aug 2017 01:37:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 24 Aug 2017 01:37:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 24 Aug 2017 01:37:46 GMT
EXPOSE 27017/tcp
# Thu, 24 Aug 2017 01:37:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:26b20bf503d22eb20def58f4afcc85ce2ef80aaa1b1cfb4d9b219b9f303aa503`  
		Last Modified: Wed, 09 Aug 2017 23:31:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c898968f529278c0af8db05709183928d28f86024f198eaa7ed10269c3a2e65c`  
		Last Modified: Thu, 24 Aug 2017 01:38:27 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1a7ee713204b5839c54f61f60404498f3257cc80f5d5cebc89481740a2ecdc`  
		Last Modified: Thu, 24 Aug 2017 01:38:27 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce1c2768ad669f71bfe571800bece463fbc4573b7cd23f9fe9265832c757a6e`  
		Last Modified: Thu, 24 Aug 2017 01:38:17 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31a810382195d4deab495bbd2492395698a029aca8a86e202bda4ba25b6eb51`  
		Last Modified: Thu, 24 Aug 2017 01:38:30 GMT  
		Size: 64.9 MB (64919441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08929e16eef1f65703588e8b59447f4536cbc39f076830e8fa5259fb27bb4d86`  
		Last Modified: Thu, 24 Aug 2017 01:38:17 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb5a438b35a85fa9c6e06382b9815beb3ac2fa76179c8b99eee8ff47b9e555`  
		Last Modified: Thu, 24 Aug 2017 01:38:18 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e02f5fe2f1c2e58c1497651ece6f4e01ac3c8ac16595b945217b278a064a727`  
		Last Modified: Thu, 24 Aug 2017 01:38:18 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:0d13a70f34c00e8603a134814e18ece718f625e09927d75bc5926ec53fa45a3a
```

-	Platforms:
	-	windows; amd64

### `mongo:windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5358350943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eb915cddd00568a782ad6abedc4684e4b22a22affc9b0d40e059c844151896`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 10 Jul 2017 22:35:45 GMT
RUN Install update 10.0.14393.1480
# Fri, 28 Jul 2017 18:55:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 08 Aug 2017 17:59:43 GMT
ENV MONGO_VERSION=3.4.7
# Tue, 08 Aug 2017 17:59:45 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.7-signed.msi
# Tue, 08 Aug 2017 17:59:48 GMT
ENV MONGO_DOWNLOAD_SHA256=baf43fcf28ff8c486d6af9036c0f15e96c0663a222626aed97d1e48c143ab865
# Tue, 08 Aug 2017 18:00:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 08 Aug 2017 18:00:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 08 Aug 2017 18:00:57 GMT
EXPOSE 27017/tcp
# Tue, 08 Aug 2017 18:01:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e29afd68a947fc566b71a432a6df352eea9e59eb221c3cb9f6bf5a4df206571e`  
		Size: 1.2 GB (1225343627 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2e2fab7692964a46adf839b6fe66a115f2c7617697a351e412c382936629b9f`  
		Last Modified: Fri, 28 Jul 2017 19:01:16 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaabfc0a85fd64385ab0664b34279ce72e6bff4a6b8c58dedd53ad4f66c9fb2`  
		Last Modified: Tue, 08 Aug 2017 18:01:28 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508dd55adcea973a45acc8f9981b23f137b3a844120e591716a09ddb94504ce9`  
		Last Modified: Tue, 08 Aug 2017 18:01:26 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161c225da1cbf013946d3d586072a48bf356124d19c893e8fee6bd8e10e0b702`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048633be839a58e73ee0e1fe673e1f3ca264f3d05ce16daf62e126cfb6755671`  
		Last Modified: Tue, 08 Aug 2017 18:01:32 GMT  
		Size: 63.0 MB (63012874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e86db3b2a06546f19358f223be6d63879a86dbc96958d34df29b9199469a74e`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20595e6fd7b3a5b7b9d29f58ca5a453b670fe771d12bae4831c84a19224bf1d`  
		Last Modified: Tue, 08 Aug 2017 18:01:19 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762fc90c18a94331366cc3d336c5721199149789dbb0ca684c0ad9f5bea44b8d`  
		Last Modified: Tue, 08 Aug 2017 18:01:18 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
