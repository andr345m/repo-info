## `docker:stable-dind`

```console
$ docker pull docker@sha256:2f56f3f65376e4f33a6ae8dbe9ed567ecebfbb691fa1947a5f9cfebb42ac5ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:stable-dind` - linux; amd64

```console
$ docker pull docker@sha256:d925d2e21e373e51e3993c9c239614b755a40ff8ea94449f95046b6e8a16d251
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34747824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49aa309624bd93208a19cd8400895a788c25d879419ba89a11e03dd080561cf7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 13 Sep 2017 14:32:25 GMT
ADD file:4583e12bf5caec40b861a3409f2a1624c3f3556cc457edb99c9707f00e779e45 in / 
# Wed, 13 Sep 2017 14:32:26 GMT
CMD ["/bin/sh"]
# Wed, 13 Sep 2017 21:40:03 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 13 Sep 2017 21:40:52 GMT
ENV DOCKER_CHANNEL=stable
# Wed, 13 Sep 2017 21:40:52 GMT
ENV DOCKER_VERSION=17.06.2-ce
# Wed, 13 Sep 2017 21:40:58 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Wed, 13 Sep 2017 21:40:58 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Sep 2017 21:40:58 GMT
CMD ["sh"]
# Wed, 13 Sep 2017 21:41:04 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Wed, 13 Sep 2017 21:41:04 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 13 Sep 2017 21:41:05 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Wed, 13 Sep 2017 21:41:07 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Wed, 13 Sep 2017 21:41:07 GMT
COPY file:7070e4b35c137a8ec5904300d19b8f7ee74aa76659517767c617249cece98a4a in /usr/local/bin/ 
# Wed, 13 Sep 2017 21:41:07 GMT
VOLUME [/var/lib/docker]
# Wed, 13 Sep 2017 21:41:08 GMT
EXPOSE 2375/tcp
# Wed, 13 Sep 2017 21:41:08 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 13 Sep 2017 21:41:08 GMT
CMD []
```

-	Layers:
	-	`sha256:88286f41530e93dffd4b964e1db22ce4939fffa4a4c665dab8591fbab03d4926`  
		Last Modified: Tue, 27 Jun 2017 18:49:37 GMT  
		Size: 2.0 MB (1990402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c401a59c6e8718eb4eb9b2bf735786e3eccdaa23b1f8996630c3a6f9ccd66c45`  
		Last Modified: Wed, 13 Sep 2017 21:41:28 GMT  
		Size: 351.4 KB (351356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6c2fc1a6d783bd820db608c7c5962e655ecde471516103cd974f31947f0494`  
		Last Modified: Wed, 13 Sep 2017 21:44:30 GMT  
		Size: 30.0 MB (30018198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebeaec9b229b486d7d433db96cba9f74c4408d91f4e58b64c3a76dd71f3ec748`  
		Last Modified: Wed, 13 Sep 2017 21:44:24 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e1a7d17178e188532dcfb017c2256bb717115d667f83a40d53cf983334e6c9`  
		Last Modified: Wed, 13 Sep 2017 21:44:52 GMT  
		Size: 2.2 MB (2209125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fa9ee837cbfa3265b46a304cc5f2d716e81fe154b2bd533b96e4e43982254`  
		Last Modified: Wed, 13 Sep 2017 21:44:52 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2573fddee9ab9470e474633208dd1fb03ff6a92c6c40cf4e4c74e13612dd12`  
		Last Modified: Wed, 13 Sep 2017 21:44:52 GMT  
		Size: 176.2 KB (176200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac937820aab7abdbc4c4ba2737534c231e23b9138c650a23b672cc8317e32ffc`  
		Last Modified: Wed, 13 Sep 2017 21:44:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
