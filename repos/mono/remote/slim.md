## `mono:slim`

```console
$ docker pull mono@sha256:8c655859efe282ec68105c644dbd0f0f17721a964726de3bfe2556d4973bf0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:slim` - linux; amd64

```console
$ docker pull mono@sha256:e1fd1bc977e26ee937e69bb49e3bf605342f6d8b49da1cfb7366519fa86475c4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57355877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c2b496f3bc5d0565b2a4905e0c9363e4a8f9f67087b4b54d1c293df2598e17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:05:00 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Thu, 07 Sep 2017 23:05:01 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:34:18 GMT
ENV MONO_VERSION=5.2.0.215
# Wed, 13 Sep 2017 00:34:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:35:05 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e2e3514337cacb7bbe4bb75132b50c3d968c478aa013ef5bee42c450cc0513`  
		Last Modified: Wed, 13 Sep 2017 00:39:22 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65333a70c20f000c97b08db96a4c2f63f2a7d7013fb1405d4412100f8fe1f97c`  
		Last Modified: Wed, 13 Sep 2017 00:39:27 GMT  
		Size: 27.2 MB (27240675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm variant v7

```console
$ docker pull mono@sha256:fcbfa4c617212f33457b7448483a1e4621223dc56e4ebcecfa61753dfa67413f
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47376307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d1da119304e2b9f72efe58570a175c45ee6da6a5119de29de80e2788dc398c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 12:48:22 GMT
ADD file:e389776a9a3fc95d77b1de986f0ae670ac389527f87ee7b71a4ffc21c973dff0 in / 
# Tue, 25 Jul 2017 12:48:24 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:17:32 GMT
ENV MONO_VERSION=5.2.0.215
# Mon, 21 Aug 2017 18:17:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 18:33:30 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d2780fdc969b3bfd6ebba1e3649e76fc061ec96f60ff3460086bf2148f1a03d`  
		Last Modified: Tue, 25 Jul 2017 13:06:38 GMT  
		Size: 26.3 MB (26288325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf6a88abcb0afb31532456afe0b7531599fedd36c9237e43813a35017a546d6`  
		Last Modified: Tue, 22 Aug 2017 20:37:54 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b35f61ba025a103d623daf322a61c2b9e3ce979cabdb91a133fdc9612aa32`  
		Last Modified: Tue, 22 Aug 2017 20:38:24 GMT  
		Size: 21.1 MB (21085912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:07bde0662fe8e219a5ffc3cbc8639c1e91f50f8e9440a1d4cbe129bf09dfe507
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52702685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f0b21bb4602ebd3fec639ece8f9f0c60aee3fb0fb747f8a204e7a1c55df41f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:24:21 GMT
ADD file:e941b26069cf288fadf2ab835d4f0c3a681f3f882d81686662d20f9642928795 in / 
# Fri, 08 Sep 2017 17:24:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:36:14 GMT
ENV MONO_VERSION=5.2.0.215
# Fri, 08 Sep 2017 21:36:20 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 21:38:00 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:01c8fcecd171557c0af8130e86fd47e393a2791dc2ea655cb5f4f0ed6b95ef51`  
		Last Modified: Fri, 08 Sep 2017 17:36:14 GMT  
		Size: 27.5 MB (27480389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba25909a569941f571a4d7a8476b98f797f5985e5d5d3c2d4d51833f7d4be57`  
		Last Modified: Fri, 08 Sep 2017 21:57:32 GMT  
		Size: 2.1 KB (2065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d88b9da28f7d692e1b6ef4b73d23901156b68d0f299e5c39476ac06221eff2`  
		Last Modified: Fri, 08 Sep 2017 21:57:45 GMT  
		Size: 25.2 MB (25220231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:slim` - linux; 386

```console
$ docker pull mono@sha256:08609af96127a10c78bdbeb52ee200ca0c36c0df7a9e18675c02dde7fdbbaf17
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59287350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31db445013577c0fbcebc88247b31748133037829e916e437c663a7893a62435`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:18:05 GMT
ADD file:cd8c8c04f635ce6e14de5271949afcf67b9c480ea35ba633423d385975e330ad in / 
# Fri, 08 Sep 2017 13:18:05 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 14:59:21 GMT
ENV MONO_VERSION=5.2.0.215
# Fri, 08 Sep 2017 14:59:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:00:33 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y mono-runtime   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:60dc9bcedd31a278f8b25a98451958fb75022352fe550042039e16ce32422ecf`  
		Last Modified: Fri, 08 Sep 2017 13:23:15 GMT  
		Size: 30.3 MB (30264166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325b9bac4dce8f564f62f1e3679087d1017b8a1519d6cc9697fdf1f8d3a07b8a`  
		Last Modified: Fri, 08 Sep 2017 15:11:12 GMT  
		Size: 2.1 KB (2066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf1c078a2bda3af6881583c84ffd48e8ccb2e90708fb2e1e067fe68a9542127`  
		Last Modified: Fri, 08 Sep 2017 15:11:23 GMT  
		Size: 29.0 MB (29021118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
