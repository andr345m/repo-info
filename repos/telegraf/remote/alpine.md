## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:c71c4179ec84f5aa21ac8ca76b272d67e84c9ca87f3dc2c6e3f5aacb9595534d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:3e7442997bc978076b6070a98c79b07e24867a238e8d7f362c4b4a249fd1c132
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12612584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd1ecb06022d29fb8105be193810eac4ceddbae2727ec42e5332f1c2bc68dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 13 Sep 2017 14:32:20 GMT
ADD file:9d67752278c0e5a1298cd2d6603ebaaab2aa342e27ddf191ee0fde138f82698c in / 
# Wed, 13 Sep 2017 14:32:20 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 15:12:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 14 Sep 2017 00:38:16 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools &&     update-ca-certificates
# Thu, 14 Sep 2017 00:38:38 GMT
ENV TELEGRAF_VERSION=1.4.0
# Thu, 14 Sep 2017 00:38:47 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 14 Sep 2017 00:38:47 GMT
EXPOSE 8092/udp 8094/tcp 8125/udp
# Thu, 14 Sep 2017 00:38:48 GMT
COPY file:43e6828e001b57ab465cff8dfd3d30830289afe7ca5944b61641956bfe38cd1c in /entrypoint.sh 
# Thu, 14 Sep 2017 00:38:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Sep 2017 00:38:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:019300c8a437a2d60248f27c206795930626dfe7ddc0323d734143bd5eb131a6`  
		Last Modified: Tue, 27 Jun 2017 18:48:47 GMT  
		Size: 2.0 MB (1970271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f86ea3a05bc091d3d70e7de3d61d06e961eaeb967c4e0c6060196f0dcdc42f`  
		Last Modified: Wed, 13 Sep 2017 15:14:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533d12625f92f18763be93f4384313958baa2423c942b99b5f0194914c66f724`  
		Last Modified: Thu, 14 Sep 2017 00:39:13 GMT  
		Size: 1.8 MB (1771344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433f9e2525488f99cdae135fa28b934ed568893f17bf31aa2cf12f16d90e0be0`  
		Last Modified: Thu, 14 Sep 2017 00:39:48 GMT  
		Size: 8.9 MB (8870633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2836e75324d050888fbd9d716103c30db455708f4a0628aba03b5e832a8e95d`  
		Last Modified: Thu, 14 Sep 2017 00:39:46 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
