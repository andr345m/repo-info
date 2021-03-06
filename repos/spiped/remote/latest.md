## `spiped:latest`

```console
$ docker pull spiped@sha256:c9dd8a10b95cb14f44d0f3462907c9341b9a24816b535a99e8a0a7e852dbafc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:77eb4504a1c62b853d4917ef8ab9513ae6e8bc4765d581441b5f7c2297c3529a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53965683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b7956b06bc7622b936dd61e45cf62318448d7004b19527d01b60c1dd62a482`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 07 Sep 2017 23:07:26 GMT
ADD file:a7405474b639b2239b96a93d02803224c052a390fe42b3f9080f2ad07de94640 in / 
# Thu, 07 Sep 2017 23:07:26 GMT
CMD ["bash"]
# Tue, 12 Sep 2017 20:50:06 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Sep 2017 20:50:14 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Sep 2017 20:50:14 GMT
ENV SPIPED_VERSION=1.6.0
# Tue, 12 Sep 2017 20:50:15 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Tue, 12 Sep 2017 20:50:15 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Tue, 12 Sep 2017 20:50:49 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Sep 2017 20:50:50 GMT
VOLUME [/spiped]
# Tue, 12 Sep 2017 20:50:50 GMT
WORKDIR /spiped
# Tue, 12 Sep 2017 20:50:50 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Tue, 12 Sep 2017 20:50:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Sep 2017 20:50:51 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:219d2e45b4afc3d80375a2fcf76505684de01f55027fb35a691099f0e538fdd8`  
		Last Modified: Thu, 07 Sep 2017 23:20:31 GMT  
		Size: 45.1 MB (45125497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff0af6bce3106c41a3cd780fb4b783469e8aade34e9ba7ad0b58893230548df`  
		Last Modified: Tue, 12 Sep 2017 20:51:25 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aea6a04787c744d1643bc1df3ed860f7a9504b4827f73b2af8796d5a7a7c7e`  
		Last Modified: Tue, 12 Sep 2017 20:51:27 GMT  
		Size: 2.1 MB (2091794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b56f03eb7c857af4b2cf56ade16bed086a5a5df011b2b0ff4f881e4a23e1e1f`  
		Last Modified: Tue, 12 Sep 2017 20:51:30 GMT  
		Size: 6.7 MB (6746205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601282960c331994cb4f1188650f95aa95188e4c915557b3388c950499755efb`  
		Last Modified: Tue, 12 Sep 2017 20:51:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b1dc4fee9de0807349d9765a0e0fef885bc11887020636561a3461d745682`  
		Last Modified: Tue, 12 Sep 2017 20:51:25 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b4eb547cf199adccafc6078251dcfa8a90873dbc32960a38839da76cf2b01584
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51468665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4108ef461823a611e7642f16d535933224f61a5bbdf7b8fd58a2571587de7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 08 Sep 2017 20:03:39 GMT
ADD file:111ccf88fc474ec03491c012baa75d4f4b3b6d08391bb86364b9fabdf3b57d3e in / 
# Fri, 08 Sep 2017 20:03:42 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 02:53:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 09 Sep 2017 02:58:14 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 02:58:15 GMT
ENV SPIPED_VERSION=1.6.0
# Sat, 09 Sep 2017 02:58:16 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Sat, 09 Sep 2017 02:58:17 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Sat, 09 Sep 2017 03:00:50 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 09 Sep 2017 03:00:51 GMT
VOLUME [/spiped]
# Sat, 09 Sep 2017 03:00:52 GMT
WORKDIR /spiped
# Sat, 09 Sep 2017 03:00:53 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Sat, 09 Sep 2017 03:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Sep 2017 03:00:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dfcb038706ea089b8e701c5bfce59c00a98c88092993630571599baa72487c2b`  
		Last Modified: Fri, 08 Sep 2017 20:20:29 GMT  
		Size: 43.8 MB (43813379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024bdf7f68c09522ec4485e2612a5a70052ffc0152162799a8263700235b1e66`  
		Last Modified: Sat, 09 Sep 2017 03:01:20 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ad083448fce92ff3c0181f8b883afe36d194d93f012db2d9f4ee43884ea21`  
		Last Modified: Sat, 09 Sep 2017 03:01:21 GMT  
		Size: 1.8 MB (1833551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6c815d3d834300cc3547891beec44f119b475a0dd479c46a68c0a17a67c09b`  
		Last Modified: Sat, 09 Sep 2017 03:01:25 GMT  
		Size: 5.8 MB (5819558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1b6cbb2211c150d11394730ad380eb3ef1908a49300d48b2d98ab0e9d33b6c`  
		Last Modified: Sat, 09 Sep 2017 03:01:21 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4994916db0f202f1133c89caf42f7967afff8bd8007a0133a30687a617e6b856`  
		Last Modified: Sat, 09 Sep 2017 03:01:20 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:558cf3c0900721f79cfa048dd610d8f0d60445f8df6a26a003fb37e180d31b7f
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49200297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456be915f50d0ada8acbac4e0f25d973e3e4220fb088fa49982283296028b1e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 09 Sep 2017 01:44:46 GMT
ADD file:8ee5b45f171806d53c0b75acea33963e2387b8dce889faec31a19f69edc1adb4 in / 
# Sat, 09 Sep 2017 01:44:47 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 04:41:50 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 09 Sep 2017 04:44:06 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 04:44:07 GMT
ENV SPIPED_VERSION=1.6.0
# Sat, 09 Sep 2017 04:44:08 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Sat, 09 Sep 2017 04:44:09 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Sat, 09 Sep 2017 04:47:19 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 09 Sep 2017 04:47:20 GMT
VOLUME [/spiped]
# Sat, 09 Sep 2017 04:47:21 GMT
WORKDIR /spiped
# Sat, 09 Sep 2017 04:47:22 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Sat, 09 Sep 2017 04:47:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Sep 2017 04:47:23 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e7ea15fa8fb2205bfb6f991da9cc2670db66dc41509ffc196004edeffff585da`  
		Last Modified: Sat, 09 Sep 2017 01:57:36 GMT  
		Size: 41.8 MB (41847032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1922e66e96ef3413ca70ef5f9818bf78807729635d91ed06b91c5bda8dd0a5`  
		Last Modified: Sat, 09 Sep 2017 04:47:48 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ca393fa6f600fb63df93dabd8d7122bf933874de4235dde8fc9da2a5f8479c`  
		Last Modified: Sat, 09 Sep 2017 04:47:48 GMT  
		Size: 1.8 MB (1774852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e670473bfcf9c0e3e555f62d8495e6458ca1a6e2eddbb6c64c9ac7436e105d`  
		Last Modified: Sat, 09 Sep 2017 04:47:52 GMT  
		Size: 5.6 MB (5576233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62f5444323dbeb3419011a1170d7f278f61d1b240a518c54231bd519f618fce`  
		Last Modified: Sat, 09 Sep 2017 04:47:48 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4541222e020a07a8756e3e05529ed190ef8504f3c80bc942ac619200f37e575b`  
		Last Modified: Sat, 09 Sep 2017 04:47:48 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:6f3db62bbafd656d7ca06487e1c0cbf1bdf095dcd1d3c7171e3a893b2e71ce00
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50837139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9de9fc5ec123db250c5681033a43e5417881603719a189c6b37c272105fe4b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 08 Sep 2017 17:28:29 GMT
ADD file:b07e310ad0ecb33cde1c2343c00726e7850bdf28d515c2fbf89ab52cb524aecd in / 
# Fri, 08 Sep 2017 17:28:30 GMT
CMD ["bash"]
# Sat, 09 Sep 2017 02:22:19 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Sat, 09 Sep 2017 02:22:29 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 02:22:29 GMT
ENV SPIPED_VERSION=1.6.0
# Sat, 09 Sep 2017 02:22:30 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Sat, 09 Sep 2017 02:22:31 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Sat, 09 Sep 2017 02:24:05 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 09 Sep 2017 02:24:05 GMT
VOLUME [/spiped]
# Sat, 09 Sep 2017 02:24:06 GMT
WORKDIR /spiped
# Sat, 09 Sep 2017 02:24:07 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Sat, 09 Sep 2017 02:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 Sep 2017 02:24:08 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61e2133fe2d7b94a36716e9a4c49c342905068f6defa9060a6b963354addd21c`  
		Last Modified: Fri, 08 Sep 2017 17:42:14 GMT  
		Size: 42.9 MB (42904079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a53a4c72a860194e77a1412f7084594cb2e22770f08398c6d6e1ef7b135e0d3`  
		Last Modified: Sat, 09 Sep 2017 02:24:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc31f7419ed7686b13f5780b41ace9c717597dd10e065944a81a63bbc27417b`  
		Last Modified: Sat, 09 Sep 2017 02:24:26 GMT  
		Size: 1.8 MB (1825805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17800646da7388cf54e384ede2d46ae5c6382e038a7bc1ca62c5e0edadaae128`  
		Last Modified: Sat, 09 Sep 2017 02:24:28 GMT  
		Size: 6.1 MB (6105065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006f11c48633a27431ce757b1913e7d5aee029b7c5c78b754972363ed1d892d0`  
		Last Modified: Sat, 09 Sep 2017 02:24:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a96444a24e8994fecb4ba73cdf9daf341b65ad09406359e6d95d8407fef199`  
		Last Modified: Sat, 09 Sep 2017 02:24:26 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:57f9a2974ae5006f47650a160501397f5437b90945eb88cd567f96c91ff15c6b
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58090715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855b6b169a840fff7ae44c7f56e804e2b2beea82fa2c8a4320d624378c5224a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 08 Sep 2017 13:19:45 GMT
ADD file:402d57d8bc933b07f97c70a7d47950ab9db320f2efcbfe638adc290d1a0c159d in / 
# Fri, 08 Sep 2017 13:19:46 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 14:38:03 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 08 Sep 2017 14:38:12 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 14:38:12 GMT
ENV SPIPED_VERSION=1.6.0
# Fri, 08 Sep 2017 14:38:12 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Fri, 08 Sep 2017 14:38:13 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Fri, 08 Sep 2017 14:39:13 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 14:39:13 GMT
VOLUME [/spiped]
# Fri, 08 Sep 2017 14:39:14 GMT
WORKDIR /spiped
# Fri, 08 Sep 2017 14:39:14 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Fri, 08 Sep 2017 14:39:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 14:39:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38807300bd16de4a00efeffb81570740677ff99a2307929b5335a897a79864df`  
		Last Modified: Fri, 08 Sep 2017 13:27:10 GMT  
		Size: 45.8 MB (45831803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489e58ae59b31b84bc4618121018307d9de75588f892348e253fa530f60331f5`  
		Last Modified: Fri, 08 Sep 2017 14:42:48 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60e8c2ed44d1731a4ac956b6752292b4bc240f454b39a8ead6b9264f594be9a`  
		Last Modified: Fri, 08 Sep 2017 14:42:48 GMT  
		Size: 2.1 MB (2084718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab811c3bb77b2b4f9ef2c39a2accd1e81a5a726853b1404052e508c1f572206`  
		Last Modified: Fri, 08 Sep 2017 14:42:51 GMT  
		Size: 10.2 MB (10172012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c88cb7bd155c09c8fd91bb776162c89493e49076037ee8013fa9c8d13471c2f`  
		Last Modified: Fri, 08 Sep 2017 14:42:48 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea0aecb3ab46b4be64e130b1f1cf450207bea5354dcb9faba2348644a7edd55`  
		Last Modified: Fri, 08 Sep 2017 14:42:48 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:b8f0c6ffe26d08dc94e6fdf6ce7aceedfcd614dd49bd7a2011b2732ac751448c
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53857286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419c3bd7f08503497054b1f131cb88f82fb98afc588184f8d2f193ca5b3ca67d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 08 Sep 2017 00:34:09 GMT
ADD file:dcb3d4c61a7bf218af93e213165a66227776bbbf5a29daf22d6bf27b0925f97a in / 
# Fri, 08 Sep 2017 00:34:09 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 01:18:41 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 08 Sep 2017 01:18:47 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 01:18:49 GMT
ENV SPIPED_VERSION=1.6.0
# Fri, 08 Sep 2017 01:18:49 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Fri, 08 Sep 2017 01:18:49 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Fri, 08 Sep 2017 01:19:31 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 01:19:31 GMT
VOLUME [/spiped]
# Fri, 08 Sep 2017 01:19:32 GMT
WORKDIR /spiped
# Fri, 08 Sep 2017 01:19:32 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Fri, 08 Sep 2017 01:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 01:19:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:97a7e851b7e2e26b94781e2f2bd23043fa46c09b45f0944d9ee2dfd81fa79762`  
		Last Modified: Fri, 08 Sep 2017 00:40:54 GMT  
		Size: 45.4 MB (45376722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b1985b34e4ce152eb529fd081080743578653e0e27be7f616516be22e36ef3`  
		Last Modified: Fri, 08 Sep 2017 01:19:44 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6790fe71be54730002df9c8370ccb065d369850177885d0f22eeb30ddca944f8`  
		Last Modified: Fri, 08 Sep 2017 01:19:44 GMT  
		Size: 1.8 MB (1763122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cbd888cd0ac34fdc565893a4f4266d1acdc33ac5c7684db18a57551501b6ad`  
		Last Modified: Fri, 08 Sep 2017 01:19:46 GMT  
		Size: 6.7 MB (6715225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39784baba7d2b02f931a0c8c1860eab8c1407deaa47777b0803c5d0bdecd8935`  
		Last Modified: Fri, 08 Sep 2017 01:19:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3150362cd94a0fdc887e9fb590d9e567b10dda4c5ef6b1864276f64b0dd896ba`  
		Last Modified: Fri, 08 Sep 2017 01:19:44 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:3812c872cdd0769c0b72eec36eabe427d1735765126845beb09d628fc896921f
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54436769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec78a57154b19953a100f5b73e0b2fcc39cbea31eeeeb5a63d3b6b151bfb3332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 08 Sep 2017 05:22:51 GMT
ADD file:2fc0b17ef015eff73a1fa19bbc2a72baf39b9f2abe8ccd1cd8ce1c757be70308 in / 
# Fri, 08 Sep 2017 05:22:53 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 07:20:09 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 08 Sep 2017 07:20:13 GMT
RUN apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 07:20:13 GMT
ENV SPIPED_VERSION=1.6.0
# Fri, 08 Sep 2017 07:20:13 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.6.0.tgz
# Fri, 08 Sep 2017 07:20:13 GMT
ENV SPIPED_DOWNLOAD_SHA256=e6f7f8f912172c3ad55638af8346ae7c4ecaa92aed6d3fb60f2bda4359cba1e4
# Fri, 08 Sep 2017 07:20:32 GMT
RUN set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 08 Sep 2017 07:20:32 GMT
VOLUME [/spiped]
# Fri, 08 Sep 2017 07:20:32 GMT
WORKDIR /spiped
# Fri, 08 Sep 2017 07:20:32 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Fri, 08 Sep 2017 07:20:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Sep 2017 07:20:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2f25bc6ba506d980514ec3fda2b8f9cbb5e39423e5e4edad7fadf3faa9e3aef7`  
		Last Modified: Fri, 08 Sep 2017 05:26:51 GMT  
		Size: 45.0 MB (44968557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6d691f59684482abb235f2d280524402c95c8183b4a52cbb68afd8da6a1784`  
		Last Modified: Fri, 08 Sep 2017 07:20:42 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d422f4223c603dc56617bcbd5b0802c0bac2bad3c60d6e1c2f60ac5fcd10721e`  
		Last Modified: Fri, 08 Sep 2017 07:20:43 GMT  
		Size: 1.8 MB (1825758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670081c07e0c6ae2db33195685f89aeaf743c8424629b67ff4c660e0643fe592`  
		Last Modified: Fri, 08 Sep 2017 07:20:44 GMT  
		Size: 7.6 MB (7640268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08979825015319578a259eed3a2f9fe697adb90189f0f9db9375f4d9a0a585bf`  
		Last Modified: Fri, 08 Sep 2017 07:20:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f51b1c0b48184ce952b48287d8d894ad3c1a799613e6d24b701d0392d99ca31`  
		Last Modified: Fri, 08 Sep 2017 07:20:42 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
