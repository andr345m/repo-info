## `neurodebian:zesty`

```console
$ docker pull neurodebian@sha256:7092b5b46ec363640f2379fb774354160124b9e7b623707c31be1d23ea4adb31
```

-	Platforms:
	-	linux; amd64

### `neurodebian:zesty` - linux; amd64

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41326146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de8454ce31c202b11e67c30271a3da559a7271da17dbb260f19dc5326534e94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jul 2017 17:16:21 GMT
ADD file:3edb19aa369fdf4f85f1977a7c3e40263def7b35c0172f9927406c161f22bccf in / 
# Thu, 20 Jul 2017 17:16:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 20 Jul 2017 17:16:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 20 Jul 2017 17:16:24 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 20 Jul 2017 17:16:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 20 Jul 2017 17:16:26 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2017 20:13:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg2 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 20 Jul 2017 20:13:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 20 Jul 2017 20:13:05 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian zesty main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel zesty main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
```

-	Layers:
	-	`sha256:e8a74323e913fcdecf4b97eaf9cdfe319efecd6e1cd30c1ff055bef20fbf0970`  
		Last Modified: Mon, 10 Jul 2017 14:40:06 GMT  
		Size: 38.1 MB (38051374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe91835aea80d04fbe0c1300d2d0573406ac2807004fd6453a59853da9a3040`  
		Last Modified: Thu, 20 Jul 2017 17:20:22 GMT  
		Size: 816.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2aac3e93a579b93195e10fd3196b349950bd22c8accf4b0588b65d3930584f`  
		Last Modified: Thu, 20 Jul 2017 17:20:22 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefbf4d7e6d0bae260aaa58b596a2543d2e4c48c06dec22945a80400e69bda4`  
		Last Modified: Thu, 20 Jul 2017 17:20:22 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071e113a30b5e30ffac44385d213d79d09a709326414b01cc7e6828e78183d9b`  
		Last Modified: Thu, 20 Jul 2017 17:20:22 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db0e5f55c3fb0869b9f85d243b57e4239380126b300c37f2ad36e4784d60f3b`  
		Last Modified: Thu, 20 Jul 2017 20:14:37 GMT  
		Size: 3.3 MB (3269064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa82e7538c4217dfaceaf71603d1977387c40a3d717d01e61164e2d1a761247`  
		Last Modified: Thu, 20 Jul 2017 20:14:32 GMT  
		Size: 3.1 KB (3136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1bc73719414b6fc816702a75d444f36c8e911e8ba3e805d5776182f910df6d`  
		Last Modified: Thu, 20 Jul 2017 20:14:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
