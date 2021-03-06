## `influxdb:latest`

```console
$ docker pull influxdb@sha256:6e1cd158afaa4f0d364c8553397ed59895f4c59202ca41f3ae5af1f2d404c45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:7840c3402ce16c8841bf90c58eb03ff150fafd47bdc7ac66a9b67def1d6abd90
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90974210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23de4149cf1ea1757c3206a79bfcf3c85195540751cc2cb55f21dfaf6cf4a81e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:43 GMT
ADD file:d7333b3e0bc6479d2faed32e06d85f1975e5b23e13e75555aeed0f639770413b in / 
# Wed, 13 Sep 2017 08:40:43 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:32:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:32:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Sep 2017 15:12:20 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 13 Sep 2017 22:29:59 GMT
ENV INFLUXDB_VERSION=1.3.5
# Wed, 13 Sep 2017 22:30:05 GMT
RUN wget -q https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget -q https://dl.influxdata.com/influxdb/releases/influxdb_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb_${INFLUXDB_VERSION}_amd64.deb.asc influxdb_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 13 Sep 2017 22:30:06 GMT
COPY file:3ee2bc0321c2aa2451df7a508649c3a54f0eebc1ef9b8a24967c58105b4d3160 in /etc/influxdb/influxdb.conf 
# Wed, 13 Sep 2017 22:30:06 GMT
EXPOSE 8086/tcp
# Wed, 13 Sep 2017 22:30:06 GMT
VOLUME [/var/lib/influxdb]
# Wed, 13 Sep 2017 22:30:06 GMT
COPY file:098affa3d1b749dacb263ddacfd86a5de1f598d6ba1f7c789ce482c66ee9c80b in /entrypoint.sh 
# Wed, 13 Sep 2017 22:30:07 GMT
COPY file:cca8e5bdb025c728ca8521b015ace9545c2552d075f4c92d7345294a6f1371c2 in /init-influxdb.sh 
# Wed, 13 Sep 2017 22:30:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Sep 2017 22:30:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:aa18ad1a0d334d80981104c599fa8cef9264552a265b1197af11274beba767cf`  
		Last Modified: Thu, 07 Sep 2017 23:11:06 GMT  
		Size: 52.6 MB (52595547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a33158a1367c7c4103c89ae66e8f4fdec4ada6a39d4648cf254b32296d6668`  
		Last Modified: Wed, 13 Sep 2017 12:54:21 GMT  
		Size: 19.3 MB (19263717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3b448c00ff3eb3cdb18d6a05ec3eae7d5fcca3fd253189ff1a93de602488ee`  
		Last Modified: Wed, 13 Sep 2017 15:13:47 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ea8aa1009d218a6bd9526edb602fa3eb6eca1fb4247bc422853ab14253aa30`  
		Last Modified: Wed, 13 Sep 2017 22:35:43 GMT  
		Size: 19.1 MB (19106572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829ab21c1ef8eea61fdd0bfb1057b7725f79934931fda9d5f2ef17cc109e8977`  
		Last Modified: Wed, 13 Sep 2017 22:35:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a5a876fd5b61b43ad814b496b6ff643cdc48a0b9a786ff62a0c32bfb948d7b`  
		Last Modified: Wed, 13 Sep 2017 22:35:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2c454254dd415cbebfe4fa7a4f19c250b947683b43db3d221ec718669de86d`  
		Last Modified: Wed, 13 Sep 2017 22:35:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
