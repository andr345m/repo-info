## `docker:rc-git`

```console
$ docker pull docker@sha256:aa15050c84b655963b52c59cb1bd1cc49f12c7ce02d61d340f7e09933b82c791
```

-	Platforms:
	-	linux; amd64

### `docker:rc-git` - linux; amd64

-	Docker Version: 17.04.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43580376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7dda11f42e2d1858534e4aa093b4d5575763dc665e863f02955303141819ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Fri, 03 Mar 2017 21:48:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Wed, 22 Mar 2017 23:46:00 GMT
ENV DOCKER_BUCKET=test.docker.com
# Thu, 04 May 2017 16:46:44 GMT
ENV DOCKER_VERSION=17.05.0-ce-rc3
# Thu, 04 May 2017 16:46:44 GMT
ENV DOCKER_SHA256_x86_64=4cae10fab8860c824ae46d644cab08c088ee0f5b20b759f975ebf5e19ae7a83c
# Thu, 04 May 2017 16:46:45 GMT
ENV DOCKER_SHA256_armel=8ac04d9f4a56af501c82d2a3df6dfe750eed351036b281ce78933cdb65373369
# Thu, 04 May 2017 16:46:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch=x86_64 ;; 		armhf) dockerArch=armel ;; 		*) echo >&2 "error: unknown Docker static binary arch $apkArch"; exit 1 ;; 	esac; 	curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/${dockerArch}/docker-${DOCKER_VERSION}.tgz" -o docker.tgz; 	sha256="DOCKER_SHA256_${dockerArch}"; sha256="$(eval "echo \$${sha256}")"; 	echo "${sha256} *docker.tgz" | sha256sum -c -; 	tar -xzvf docker.tgz; 	mv docker/* /usr/local/bin/; 	rmdir docker; 	rm docker.tgz; 	docker -v
# Thu, 04 May 2017 16:46:51 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Thu, 04 May 2017 16:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 May 2017 16:46:53 GMT
CMD ["sh"]
# Thu, 04 May 2017 16:47:46 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed492db3a66ce1d7073597aa9d3c6715468e3804abe6d8a0ba6790f61c3fe65`  
		Last Modified: Sat, 04 Mar 2017 04:39:06 GMT  
		Size: 2.2 MB (2167713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7476b3e2fdbe50e8e8f0cef1929de967bd962b14758b934cfa61ad58682ee110`  
		Last Modified: Thu, 04 May 2017 16:48:29 GMT  
		Size: 28.8 MB (28784509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83f01096420ece042e0703ecf084aaac7f31f9641067bbd75d38ade85f23691`  
		Last Modified: Thu, 04 May 2017 16:48:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74267b2331c8b0ef9988cb643496c11121a0da38cc415537167097f1e044807c`  
		Last Modified: Thu, 04 May 2017 16:53:03 GMT  
		Size: 10.7 MB (10722393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip