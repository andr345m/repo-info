## `jetty:latest`

```console
$ docker pull jetty@sha256:c446705be6834fc59368a27b237b48af0463bd91d1ec47480c1edcbb3398659f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jetty:latest` - linux; amd64

```console
$ docker pull jetty@sha256:5d8d079d2a58fbfa12b97259282486cc85c265f38447cff6d77a4da78cf9f5f8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236229523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49789bb4fbe515e760ae2fef30d885ccefa820dc838f23f6162f3635ab90fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 13 Sep 2017 08:41:42 GMT
ADD file:a7405474b639b2239b96a93d02803224c052a390fe42b3f9080f2ad07de94640 in / 
# Wed, 13 Sep 2017 08:41:42 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 12:36:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 12:36:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 Sep 2017 04:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 04:21:52 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 04:21:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 14 Sep 2017 04:21:54 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 14 Sep 2017 04:21:55 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 14 Sep 2017 04:21:55 GMT
ENV JAVA_VERSION=8u141
# Thu, 14 Sep 2017 04:21:55 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Thu, 14 Sep 2017 04:21:55 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 14 Sep 2017 04:23:09 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 14 Sep 2017 04:23:14 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Thu, 14 Sep 2017 06:33:52 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Thu, 14 Sep 2017 06:33:52 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 14 Sep 2017 06:33:53 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2017 06:33:53 GMT
RUN mkdir -p "$JETTY_HOME"
# Thu, 14 Sep 2017 06:33:53 GMT
WORKDIR /usr/local/jetty
# Thu, 14 Sep 2017 06:33:54 GMT
ENV JETTY_VERSION=9.4.6.v20170531
# Thu, 14 Sep 2017 06:33:54 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.6.v20170531/jetty-home-9.4.6.v20170531.tar.gz
# Thu, 14 Sep 2017 06:33:54 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E
# Thu, 14 Sep 2017 06:34:06 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -rf "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Thu, 14 Sep 2017 06:34:08 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 14 Sep 2017 06:34:09 GMT
RUN mkdir -p "$JETTY_BASE"
# Thu, 14 Sep 2017 06:34:09 GMT
WORKDIR /var/lib/jetty
# Thu, 14 Sep 2017 06:34:15 GMT
RUN set -xe 	&& java -jar "$JETTY_HOME/start.jar" --create-startd --add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket,setuid" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Thu, 14 Sep 2017 06:34:15 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 14 Sep 2017 06:34:18 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Thu, 14 Sep 2017 06:34:18 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Thu, 14 Sep 2017 06:34:18 GMT
EXPOSE 8080/tcp
# Thu, 14 Sep 2017 06:34:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Sep 2017 06:34:18 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
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
	-	`sha256:63678957352b01a378d047c9d036cc6173292cb74ab3ab1ef999f7c1795a4289`  
		Last Modified: Thu, 14 Sep 2017 04:59:44 GMT  
		Size: 852.4 KB (852355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929e9da71fa4b99a3e2311d9fbe8ed9309d64aa1e186d75cedd8376f2470ed12`  
		Last Modified: Thu, 14 Sep 2017 04:59:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ef2abace7441da328e7b5d88d7a9af50029e2708469dd04f2fba6c718ab466`  
		Last Modified: Thu, 14 Sep 2017 04:59:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee465bb23abdb02ce2e1a5ea1650604d45a2a340953fd984f5fbfe72d728e20e`  
		Last Modified: Thu, 14 Sep 2017 05:00:36 GMT  
		Size: 166.2 MB (166171116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389ed23519a6eade3f5bd0e2ddf2ee46626e8576179782441dbe628d4ac938b`  
		Last Modified: Thu, 14 Sep 2017 04:59:43 GMT  
		Size: 272.1 KB (272076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d3f36522beb50c35c9c96e4359c28d153848eeacbcd84b14b1731059e852b1`  
		Last Modified: Thu, 14 Sep 2017 06:36:22 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d0c7d995e51677cc7d7a2e9628507a918d8d394f85f3b57dc972217001953`  
		Last Modified: Thu, 14 Sep 2017 06:36:22 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8104d0b387c1b1cae0c1aefb7a2507cd80c067714abfada813f726e97fad6b7a`  
		Last Modified: Thu, 14 Sep 2017 06:36:21 GMT  
		Size: 8.1 MB (8065356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce75537734b47e4e2de89e19aa5da02318225f88de684247e2ff236e19d535b`  
		Last Modified: Thu, 14 Sep 2017 06:36:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf4ac57a50ff3095edbfae8458bd5aa017c68f63ccd58e9427bddf0d997caad`  
		Last Modified: Thu, 14 Sep 2017 06:36:19 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4209fdcd4e2cfae3ca972e9e5d31718f8d3eb63a6f36d31ac974181c19bd8a5`  
		Last Modified: Thu, 14 Sep 2017 06:36:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5606adb6513bb75145c7177b315dbb972ce1e3226c822f67d254a8015af28ea`  
		Last Modified: Thu, 14 Sep 2017 06:36:20 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
