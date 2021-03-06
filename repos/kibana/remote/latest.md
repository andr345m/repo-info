## `kibana:latest`

```console
$ docker pull kibana@sha256:a121bbf35425bb7d3448feae3211cdbfdfa128f0f7301bdb5dc82a0a91edb885
```

-	Platforms:
	-	linux; amd64

### `kibana:latest` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127358748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e73a80c44000e5272f5e5912aa6e6090f2cf3af031b5830732daa8d52c7d38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kibana"]`

```dockerfile
# Thu, 07 Sep 2017 23:04:40 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Thu, 07 Sep 2017 23:04:41 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 07:44:52 GMT
RUN groupadd -r kibana && useradd -r -m -g kibana kibana
# Fri, 08 Sep 2017 07:45:16 GMT
RUN apt-get update && apt-get install -y 		apt-transport-https 		ca-certificates 		wget 		libfontconfig 		libfreetype6 	--no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 07:45:16 GMT
ENV GOSU_VERSION=1.10
# Fri, 08 Sep 2017 07:45:20 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Fri, 08 Sep 2017 07:45:24 GMT
ENV TINI_VERSION=v0.9.0
# Fri, 08 Sep 2017 07:45:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Fri, 08 Sep 2017 07:45:35 GMT
RUN set -ex; 	key='46095ACC8548582C1A2699A9D27D666CD88E42B4'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/elastic.gpg; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 08 Sep 2017 07:45:39 GMT
RUN echo 'deb https://artifacts.elastic.co/packages/5.x/apt stable main' > /etc/apt/sources.list.d/kibana.list
# Fri, 08 Sep 2017 07:45:39 GMT
ENV KIBANA_VERSION=5.5.2
# Fri, 08 Sep 2017 07:46:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends kibana=$KIBANA_VERSION 	&& rm -rf /var/lib/apt/lists/* 		&& sed -ri "s!^(\#\s*)?(server\.host:).*!\2 '0.0.0.0'!" /etc/kibana/kibana.yml 	&& grep -q "^server\.host: '0.0.0.0'\$" /etc/kibana/kibana.yml 		&& sed -ri "s!^(\#\s*)?(elasticsearch\.url:).*!\2 'http://elasticsearch:9200'!" /etc/kibana/kibana.yml 	&& grep -q "^elasticsearch\.url: 'http://elasticsearch:9200'\$" /etc/kibana/kibana.yml
# Fri, 08 Sep 2017 07:46:16 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Sep 2017 07:46:17 GMT
COPY file:9a3ed3a1655d5afa631fded5211f1c33f5f49f1d1e0e0d9a031c9e8601111f05 in / 
# Fri, 08 Sep 2017 07:46:17 GMT
EXPOSE 5601/tcp
# Fri, 08 Sep 2017 07:46:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 Sep 2017 07:46:18 GMT
CMD ["kibana"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2d2a20bb848658c311a10d16133badb74899cc5bb30f8a9ce4488ad16721f6`  
		Last Modified: Fri, 08 Sep 2017 19:43:52 GMT  
		Size: 4.4 KB (4381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667931c73e5dccfde3f2e1a5c0b75f1d37a32c9cf76e2cae584fbbe322987ff2`  
		Last Modified: Fri, 08 Sep 2017 19:43:56 GMT  
		Size: 22.4 MB (22403570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8919cd44f8f3a08e0c92acbef43d7cc7d1c877c322980b264967309b8447d2`  
		Last Modified: Fri, 08 Sep 2017 19:43:50 GMT  
		Size: 500.7 KB (500660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d237d4fd339050646db35264fd2e6496f396f7e1ae8d9374728ed0aa52ee5f`  
		Last Modified: Fri, 08 Sep 2017 19:43:50 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28d9cc6e097af29886b145be5dc1eba908c6f2c43caf1b7e62310bd08dbe775`  
		Last Modified: Fri, 08 Sep 2017 19:43:50 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cc615b83bf2c13bf8fa69480a2c17ce1ff6a2a092e515816d6e62999c85a02`  
		Last Modified: Fri, 08 Sep 2017 19:43:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abde8e46c894c6789aa00693f302b80174f94c40e05221fa0aab466bca7f4ad`  
		Last Modified: Fri, 08 Sep 2017 19:44:24 GMT  
		Size: 51.8 MB (51845292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6f193cf5a9962f5f7f8bae9490c4b135c6fa18cfb102c76e15d21da7c2ed17`  
		Last Modified: Fri, 08 Sep 2017 19:43:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
