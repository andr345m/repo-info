## `flink:latest`

```console
$ docker pull flink@sha256:1477b325affe7f85f1448ed306e7b5e6582337a02a9ced491338d6362e7d51d4
```

-	Platforms:
	-	linux; amd64

### `flink:latest` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256061732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1f032aeb6a9e4cba601ae2b6f62c6fefb59112d2931ae8c5b7d2112c9c9513`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Mon, 24 Apr 2017 19:20:41 GMT
ADD file:712c48086043553b85ffb031d8f6c5de857a2e53974df30cdfbc1e85c1b00a25 in / 
# Mon, 24 Apr 2017 19:20:42 GMT
CMD ["/bin/bash"]
# Mon, 24 Apr 2017 19:54:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2017 00:40:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Apr 2017 00:42:38 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 25 Apr 2017 00:42:39 GMT
ENV LANG=C.UTF-8
# Tue, 25 Apr 2017 00:42:40 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 05 May 2017 22:29:09 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 05 May 2017 22:29:10 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 05 May 2017 22:29:11 GMT
ENV JAVA_VERSION=8u121
# Fri, 05 May 2017 22:29:11 GMT
ENV JAVA_DEBIAN_VERSION=8u121-b13-1~bpo8+1
# Fri, 05 May 2017 22:29:12 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20161107~bpo8+1
# Fri, 05 May 2017 22:29:34 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 05 May 2017 22:29:37 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Mon, 08 May 2017 21:09:50 GMT
ENV GOSU_VERSION=1.7
# Tue, 09 May 2017 19:25:52 GMT
RUN set -ex;   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Tue, 09 May 2017 20:22:51 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1;   rm -rf /var/lib/apt/lists/*
# Tue, 09 May 2017 20:27:31 GMT
ENV FLINK_VERSION=1.2.1 HADOOP_VERSION=27 SCALA_VERSION=2.11
# Tue, 09 May 2017 20:27:31 GMT
ENV FLINK_HOME=/opt/flink
# Tue, 09 May 2017 20:27:32 GMT
ENV PATH=/opt/flink/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 May 2017 20:27:33 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Tue, 09 May 2017 20:27:34 GMT
WORKDIR /opt/flink
# Tue, 09 May 2017 20:27:35 GMT
ENV FLINK_URL_FILE_PATH=flink/flink-1.2.1/flink-1.2.1-bin-hadoop27-scala_2.11.tgz
# Tue, 09 May 2017 20:27:35 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.2.1/flink-1.2.1-bin-hadoop27-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.2.1/flink-1.2.1-bin-hadoop27-scala_2.11.tgz.asc
# Tue, 09 May 2017 20:27:36 GMT
COPY file:22c552c887979c8fbaa961276686f26badf8e846cdc00b8410c37479ebfa98ec in /KEYS 
# Tue, 09 May 2017 20:27:45 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";   wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";   gpg --import /KEYS;   gpg --batch --verify flink.tgz.asc flink.tgz;   rm -r "$GNUPGHOME" flink.tgz.asc;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Tue, 09 May 2017 20:27:46 GMT
COPY file:fe1fb6d5958f8d4352415a749ef7bd4569e1b11eec1c10c18e9e296765c72a61 in / 
# Tue, 09 May 2017 20:27:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 May 2017 20:27:47 GMT
EXPOSE 6123/tcp 8081/tcp
# Tue, 09 May 2017 20:27:48 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:cd0a524342efac6edff500c17e625735bbe479c926439b263bbe3c8518a0849c`  
		Last Modified: Mon, 24 Apr 2017 19:32:05 GMT  
		Size: 52.6 MB (52550276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39c3ffe41332a7a3c7f85f57e547361ec90b6e0091dd6058e06acccde2217d4`  
		Last Modified: Mon, 24 Apr 2017 22:19:28 GMT  
		Size: 19.3 MB (19266225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3320edf402163d25e312e38b3611696a39ea8cefb0f58bda4e29bf980ed0a`  
		Last Modified: Tue, 25 Apr 2017 00:50:41 GMT  
		Size: 573.7 KB (573718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e109682f71c933209cd7962c1dcc21b6b81d1e5bc8c7089ba47a9f237fd6d`  
		Last Modified: Tue, 25 Apr 2017 00:56:07 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a59efcf95535f4d4fc76173fde32486ab50fa8fbf293afae9412d4716cb59c4`  
		Last Modified: Tue, 25 Apr 2017 00:56:07 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b666d261d3b8c87670e9a57b9261a07977433af08d4d48d7fe37a5a7126350`  
		Last Modified: Fri, 05 May 2017 22:58:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98430ee944b3da76725b45f66548b40b10ad2b28dbf47a8b7a9a6a444020e8ab`  
		Last Modified: Fri, 05 May 2017 22:58:37 GMT  
		Size: 54.1 MB (54059101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0670b9fca61293fb13c831445d8604fa03674cdc0eea487af1db9df0cfadc859`  
		Last Modified: Fri, 05 May 2017 22:58:24 GMT  
		Size: 289.7 KB (289674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331112f53dfc41ffac22d864d657a8ca79bdef70c21404feefa5fe23226c0839`  
		Last Modified: Tue, 09 May 2017 20:28:16 GMT  
		Size: 818.8 KB (818816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea16ed2b7bc141fe399257c6b47dd1ec9ab2e22c6e81efddf47aa402e20c88bf`  
		Last Modified: Tue, 09 May 2017 20:28:13 GMT  
		Size: 154.3 KB (154288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7050f721c15ea12dea52362222ce5fea00d59fbeecc81364dfe750e48e77c29`  
		Last Modified: Tue, 09 May 2017 20:36:42 GMT  
		Size: 5.0 KB (4974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afbe61ab177ab69c59e9aba616eaefb83cc0a21acf9f172116ae674a8b33c45`  
		Last Modified: Tue, 09 May 2017 20:36:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a55b1170b0601b3b39c70bb78bf36d9873f9bc7704475eda47dc641a839371`  
		Last Modified: Tue, 09 May 2017 20:36:42 GMT  
		Size: 48.9 KB (48851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deb9a679b2e023a462dabe22352b609d6cf45b2a44b84e4ae42139deca63f8c`  
		Last Modified: Tue, 09 May 2017 20:36:52 GMT  
		Size: 128.3 MB (128294020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f018272b9e0fec76a2e13eb5c27c43ef322ec3770ad3190a1b8934f684703c5`  
		Last Modified: Tue, 09 May 2017 20:36:43 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip