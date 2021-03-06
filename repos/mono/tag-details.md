<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mono`

-	[`mono:4`](#mono4)
-	[`mono:4.8`](#mono48)
-	[`mono:4.8.0`](#mono480)
-	[`mono:4.8.0.524`](#mono480524)
-	[`mono:5`](#mono5)
-	[`mono:5.0`](#mono50)
-	[`mono:5.0.1`](#mono501)
-	[`mono:5.0.1.1`](#mono5011)
-	[`mono:5.2`](#mono52)
-	[`mono:5.2.0`](#mono520)
-	[`mono:5.2.0.215`](#mono520215)
-	[`mono:5.2.0.215-slim`](#mono520215-slim)
-	[`mono:5.2.0-slim`](#mono520-slim)
-	[`mono:5.2-slim`](#mono52-slim)
-	[`mono:5-slim`](#mono5-slim)
-	[`mono:latest`](#monolatest)
-	[`mono:slim`](#monoslim)

## `mono:4`

```console
$ docker pull mono@sha256:642c57cb7a0bd0ce6f8c20928f8862210c25f59bc05ff6df693512be9ac1a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; 386

### `mono:4` - linux; amd64

```console
$ docker pull mono@sha256:35eee4a974ef62b8e56b65c817a6d6fd64d3475b98395ea4adb22b211134c4c9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153024012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9da77ef4bea63a35c37d5e166ef9fc55d021b3ce54b57aa08baa6d57a640ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:08:56 GMT
ADD file:240ed8d95c0f51cf9dbb7c83f7a0af7e37ee15c7449b864e8770a65f3e771b86 in / 
# Thu, 07 Sep 2017 23:08:56 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:36:57 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Wed, 13 Sep 2017 00:36:57 GMT
ENV MONO_VERSION=4.8.0.524
# Wed, 13 Sep 2017 00:37:07 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:37:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:48b042a4691b27483afd6b309d6dd2fc12f2c1d388409709b418094a3a4cdf54`  
		Last Modified: Thu, 07 Sep 2017 23:23:34 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8247eeb5e660a7ddae3f64c06c110d3099ba07d7c8b3c15c0be3b1321ba1894c`  
		Last Modified: Wed, 13 Sep 2017 00:40:46 GMT  
		Size: 7.8 MB (7756444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa426496c0e41994e25e868ce8871ab6035ec2e95d173783170ffc18d9d703c2`  
		Last Modified: Wed, 13 Sep 2017 00:40:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fac27c5d253212df2b21a2689641b531497ff0c814568a208b4a721c4fd5a9`  
		Last Modified: Wed, 13 Sep 2017 00:41:02 GMT  
		Size: 107.1 MB (107134537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4` - linux; arm variant v7

```console
$ docker pull mono@sha256:2d76c520c4ca22f016b0d19454295eebc06ec66cebbd5805885bade413a1e498
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138920141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195958719f6acfab204fe46e651565b5a0a496a6a9a020ed753467e39fa12d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 13:01:57 GMT
ADD file:383f867e58ac7d7020c618a7428b47b8b1911785ac6ae78a6751fb7f55eeb5c2 in / 
# Tue, 25 Jul 2017 13:01:59 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:59:42 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 21 Aug 2017 18:59:43 GMT
ENV MONO_VERSION=4.8.0.524
# Mon, 21 Aug 2017 19:09:41 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 19:09:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 22:17:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ada306cd59ed8be1f27f62bff2346a7c5647fef217a4b7fe851279c6c305e1f1`  
		Last Modified: Tue, 25 Jul 2017 13:16:28 GMT  
		Size: 35.7 MB (35656025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65fe06a51c537d8d8a580063324752ae832aaeadd86657a988aa5892d7b157a`  
		Last Modified: Tue, 22 Aug 2017 20:41:46 GMT  
		Size: 7.2 MB (7184515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be4390708771b6c63e5050721f22fa19eacb3b8861db0c5ad0fba81868a6ef`  
		Last Modified: Tue, 22 Aug 2017 20:41:35 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac2105eece8e1d64a887f8a1c2357ea6e64e62176b2d45c9ec7a1be186742fe`  
		Last Modified: Tue, 22 Aug 2017 20:42:53 GMT  
		Size: 96.0 MB (96049681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4` - linux; 386

```console
$ docker pull mono@sha256:ecfe02a03176620d67a57a5bd33d52d22533c7909932d3d9758967c7363f02fa
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153007233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b13b149eed408ca6ebf5c6484710868571eb568a22417e14c9e17600db1721`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:20:48 GMT
ADD file:6e69a03d6dde108627b32e45abd197b90df267d161800ebec8416063a64aef06 in / 
# Fri, 08 Sep 2017 13:20:48 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:03:22 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Fri, 08 Sep 2017 15:03:22 GMT
ENV MONO_VERSION=4.8.0.524
# Fri, 08 Sep 2017 15:03:39 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:03:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:05:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:62bb183541ac6fc75244fe087faa7c427d0bc7cd70f749e3415bc6cb2e02638a`  
		Last Modified: Fri, 08 Sep 2017 13:29:31 GMT  
		Size: 37.4 MB (37433264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b46b12d9c14c1a58efcf657bb1ece830e223d45b6f6b47426f7069fd3eb16`  
		Last Modified: Fri, 08 Sep 2017 15:15:48 GMT  
		Size: 9.6 MB (9606347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def8499eb61ff5538eb97cd88a98aa2dbd2ccc9ee75b6c439d684048ef2d6199`  
		Last Modified: Fri, 08 Sep 2017 15:15:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a0e076c959794a10fc9aff2ba5789e98b2fdae5738e7efb3b88c47a50fb26c`  
		Last Modified: Fri, 08 Sep 2017 15:16:18 GMT  
		Size: 105.9 MB (105937718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:4.8`

```console
$ docker pull mono@sha256:642c57cb7a0bd0ce6f8c20928f8862210c25f59bc05ff6df693512be9ac1a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; 386

### `mono:4.8` - linux; amd64

```console
$ docker pull mono@sha256:35eee4a974ef62b8e56b65c817a6d6fd64d3475b98395ea4adb22b211134c4c9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153024012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9da77ef4bea63a35c37d5e166ef9fc55d021b3ce54b57aa08baa6d57a640ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:08:56 GMT
ADD file:240ed8d95c0f51cf9dbb7c83f7a0af7e37ee15c7449b864e8770a65f3e771b86 in / 
# Thu, 07 Sep 2017 23:08:56 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:36:57 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Wed, 13 Sep 2017 00:36:57 GMT
ENV MONO_VERSION=4.8.0.524
# Wed, 13 Sep 2017 00:37:07 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:37:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:48b042a4691b27483afd6b309d6dd2fc12f2c1d388409709b418094a3a4cdf54`  
		Last Modified: Thu, 07 Sep 2017 23:23:34 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8247eeb5e660a7ddae3f64c06c110d3099ba07d7c8b3c15c0be3b1321ba1894c`  
		Last Modified: Wed, 13 Sep 2017 00:40:46 GMT  
		Size: 7.8 MB (7756444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa426496c0e41994e25e868ce8871ab6035ec2e95d173783170ffc18d9d703c2`  
		Last Modified: Wed, 13 Sep 2017 00:40:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fac27c5d253212df2b21a2689641b531497ff0c814568a208b4a721c4fd5a9`  
		Last Modified: Wed, 13 Sep 2017 00:41:02 GMT  
		Size: 107.1 MB (107134537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8` - linux; arm variant v7

```console
$ docker pull mono@sha256:2d76c520c4ca22f016b0d19454295eebc06ec66cebbd5805885bade413a1e498
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138920141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195958719f6acfab204fe46e651565b5a0a496a6a9a020ed753467e39fa12d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 13:01:57 GMT
ADD file:383f867e58ac7d7020c618a7428b47b8b1911785ac6ae78a6751fb7f55eeb5c2 in / 
# Tue, 25 Jul 2017 13:01:59 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:59:42 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 21 Aug 2017 18:59:43 GMT
ENV MONO_VERSION=4.8.0.524
# Mon, 21 Aug 2017 19:09:41 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 19:09:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 22:17:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ada306cd59ed8be1f27f62bff2346a7c5647fef217a4b7fe851279c6c305e1f1`  
		Last Modified: Tue, 25 Jul 2017 13:16:28 GMT  
		Size: 35.7 MB (35656025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65fe06a51c537d8d8a580063324752ae832aaeadd86657a988aa5892d7b157a`  
		Last Modified: Tue, 22 Aug 2017 20:41:46 GMT  
		Size: 7.2 MB (7184515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be4390708771b6c63e5050721f22fa19eacb3b8861db0c5ad0fba81868a6ef`  
		Last Modified: Tue, 22 Aug 2017 20:41:35 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac2105eece8e1d64a887f8a1c2357ea6e64e62176b2d45c9ec7a1be186742fe`  
		Last Modified: Tue, 22 Aug 2017 20:42:53 GMT  
		Size: 96.0 MB (96049681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8` - linux; 386

```console
$ docker pull mono@sha256:ecfe02a03176620d67a57a5bd33d52d22533c7909932d3d9758967c7363f02fa
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153007233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b13b149eed408ca6ebf5c6484710868571eb568a22417e14c9e17600db1721`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:20:48 GMT
ADD file:6e69a03d6dde108627b32e45abd197b90df267d161800ebec8416063a64aef06 in / 
# Fri, 08 Sep 2017 13:20:48 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:03:22 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Fri, 08 Sep 2017 15:03:22 GMT
ENV MONO_VERSION=4.8.0.524
# Fri, 08 Sep 2017 15:03:39 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:03:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:05:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:62bb183541ac6fc75244fe087faa7c427d0bc7cd70f749e3415bc6cb2e02638a`  
		Last Modified: Fri, 08 Sep 2017 13:29:31 GMT  
		Size: 37.4 MB (37433264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b46b12d9c14c1a58efcf657bb1ece830e223d45b6f6b47426f7069fd3eb16`  
		Last Modified: Fri, 08 Sep 2017 15:15:48 GMT  
		Size: 9.6 MB (9606347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def8499eb61ff5538eb97cd88a98aa2dbd2ccc9ee75b6c439d684048ef2d6199`  
		Last Modified: Fri, 08 Sep 2017 15:15:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a0e076c959794a10fc9aff2ba5789e98b2fdae5738e7efb3b88c47a50fb26c`  
		Last Modified: Fri, 08 Sep 2017 15:16:18 GMT  
		Size: 105.9 MB (105937718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:4.8.0`

```console
$ docker pull mono@sha256:642c57cb7a0bd0ce6f8c20928f8862210c25f59bc05ff6df693512be9ac1a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; 386

### `mono:4.8.0` - linux; amd64

```console
$ docker pull mono@sha256:35eee4a974ef62b8e56b65c817a6d6fd64d3475b98395ea4adb22b211134c4c9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153024012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9da77ef4bea63a35c37d5e166ef9fc55d021b3ce54b57aa08baa6d57a640ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:08:56 GMT
ADD file:240ed8d95c0f51cf9dbb7c83f7a0af7e37ee15c7449b864e8770a65f3e771b86 in / 
# Thu, 07 Sep 2017 23:08:56 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:36:57 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Wed, 13 Sep 2017 00:36:57 GMT
ENV MONO_VERSION=4.8.0.524
# Wed, 13 Sep 2017 00:37:07 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:37:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:48b042a4691b27483afd6b309d6dd2fc12f2c1d388409709b418094a3a4cdf54`  
		Last Modified: Thu, 07 Sep 2017 23:23:34 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8247eeb5e660a7ddae3f64c06c110d3099ba07d7c8b3c15c0be3b1321ba1894c`  
		Last Modified: Wed, 13 Sep 2017 00:40:46 GMT  
		Size: 7.8 MB (7756444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa426496c0e41994e25e868ce8871ab6035ec2e95d173783170ffc18d9d703c2`  
		Last Modified: Wed, 13 Sep 2017 00:40:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fac27c5d253212df2b21a2689641b531497ff0c814568a208b4a721c4fd5a9`  
		Last Modified: Wed, 13 Sep 2017 00:41:02 GMT  
		Size: 107.1 MB (107134537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:2d76c520c4ca22f016b0d19454295eebc06ec66cebbd5805885bade413a1e498
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138920141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195958719f6acfab204fe46e651565b5a0a496a6a9a020ed753467e39fa12d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 13:01:57 GMT
ADD file:383f867e58ac7d7020c618a7428b47b8b1911785ac6ae78a6751fb7f55eeb5c2 in / 
# Tue, 25 Jul 2017 13:01:59 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:59:42 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 21 Aug 2017 18:59:43 GMT
ENV MONO_VERSION=4.8.0.524
# Mon, 21 Aug 2017 19:09:41 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 19:09:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 22:17:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ada306cd59ed8be1f27f62bff2346a7c5647fef217a4b7fe851279c6c305e1f1`  
		Last Modified: Tue, 25 Jul 2017 13:16:28 GMT  
		Size: 35.7 MB (35656025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65fe06a51c537d8d8a580063324752ae832aaeadd86657a988aa5892d7b157a`  
		Last Modified: Tue, 22 Aug 2017 20:41:46 GMT  
		Size: 7.2 MB (7184515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be4390708771b6c63e5050721f22fa19eacb3b8861db0c5ad0fba81868a6ef`  
		Last Modified: Tue, 22 Aug 2017 20:41:35 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac2105eece8e1d64a887f8a1c2357ea6e64e62176b2d45c9ec7a1be186742fe`  
		Last Modified: Tue, 22 Aug 2017 20:42:53 GMT  
		Size: 96.0 MB (96049681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8.0` - linux; 386

```console
$ docker pull mono@sha256:ecfe02a03176620d67a57a5bd33d52d22533c7909932d3d9758967c7363f02fa
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153007233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b13b149eed408ca6ebf5c6484710868571eb568a22417e14c9e17600db1721`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:20:48 GMT
ADD file:6e69a03d6dde108627b32e45abd197b90df267d161800ebec8416063a64aef06 in / 
# Fri, 08 Sep 2017 13:20:48 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:03:22 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Fri, 08 Sep 2017 15:03:22 GMT
ENV MONO_VERSION=4.8.0.524
# Fri, 08 Sep 2017 15:03:39 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:03:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:05:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:62bb183541ac6fc75244fe087faa7c427d0bc7cd70f749e3415bc6cb2e02638a`  
		Last Modified: Fri, 08 Sep 2017 13:29:31 GMT  
		Size: 37.4 MB (37433264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b46b12d9c14c1a58efcf657bb1ece830e223d45b6f6b47426f7069fd3eb16`  
		Last Modified: Fri, 08 Sep 2017 15:15:48 GMT  
		Size: 9.6 MB (9606347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def8499eb61ff5538eb97cd88a98aa2dbd2ccc9ee75b6c439d684048ef2d6199`  
		Last Modified: Fri, 08 Sep 2017 15:15:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a0e076c959794a10fc9aff2ba5789e98b2fdae5738e7efb3b88c47a50fb26c`  
		Last Modified: Fri, 08 Sep 2017 15:16:18 GMT  
		Size: 105.9 MB (105937718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:4.8.0.524`

```console
$ docker pull mono@sha256:642c57cb7a0bd0ce6f8c20928f8862210c25f59bc05ff6df693512be9ac1a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; 386

### `mono:4.8.0.524` - linux; amd64

```console
$ docker pull mono@sha256:35eee4a974ef62b8e56b65c817a6d6fd64d3475b98395ea4adb22b211134c4c9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153024012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9da77ef4bea63a35c37d5e166ef9fc55d021b3ce54b57aa08baa6d57a640ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:08:56 GMT
ADD file:240ed8d95c0f51cf9dbb7c83f7a0af7e37ee15c7449b864e8770a65f3e771b86 in / 
# Thu, 07 Sep 2017 23:08:56 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:36:57 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Wed, 13 Sep 2017 00:36:57 GMT
ENV MONO_VERSION=4.8.0.524
# Wed, 13 Sep 2017 00:37:07 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:37:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:37:49 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:48b042a4691b27483afd6b309d6dd2fc12f2c1d388409709b418094a3a4cdf54`  
		Last Modified: Thu, 07 Sep 2017 23:23:34 GMT  
		Size: 38.1 MB (38103127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8247eeb5e660a7ddae3f64c06c110d3099ba07d7c8b3c15c0be3b1321ba1894c`  
		Last Modified: Wed, 13 Sep 2017 00:40:46 GMT  
		Size: 7.8 MB (7756444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa426496c0e41994e25e868ce8871ab6035ec2e95d173783170ffc18d9d703c2`  
		Last Modified: Wed, 13 Sep 2017 00:40:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fac27c5d253212df2b21a2689641b531497ff0c814568a208b4a721c4fd5a9`  
		Last Modified: Wed, 13 Sep 2017 00:41:02 GMT  
		Size: 107.1 MB (107134537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8.0.524` - linux; arm variant v7

```console
$ docker pull mono@sha256:2d76c520c4ca22f016b0d19454295eebc06ec66cebbd5805885bade413a1e498
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138920141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195958719f6acfab204fe46e651565b5a0a496a6a9a020ed753467e39fa12d01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 13:01:57 GMT
ADD file:383f867e58ac7d7020c618a7428b47b8b1911785ac6ae78a6751fb7f55eeb5c2 in / 
# Tue, 25 Jul 2017 13:01:59 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:59:42 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 21 Aug 2017 18:59:43 GMT
ENV MONO_VERSION=4.8.0.524
# Mon, 21 Aug 2017 19:09:41 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 19:09:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 22:17:01 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:ada306cd59ed8be1f27f62bff2346a7c5647fef217a4b7fe851279c6c305e1f1`  
		Last Modified: Tue, 25 Jul 2017 13:16:28 GMT  
		Size: 35.7 MB (35656025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65fe06a51c537d8d8a580063324752ae832aaeadd86657a988aa5892d7b157a`  
		Last Modified: Tue, 22 Aug 2017 20:41:46 GMT  
		Size: 7.2 MB (7184515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be4390708771b6c63e5050721f22fa19eacb3b8861db0c5ad0fba81868a6ef`  
		Last Modified: Tue, 22 Aug 2017 20:41:35 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac2105eece8e1d64a887f8a1c2357ea6e64e62176b2d45c9ec7a1be186742fe`  
		Last Modified: Tue, 22 Aug 2017 20:42:53 GMT  
		Size: 96.0 MB (96049681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:4.8.0.524` - linux; 386

```console
$ docker pull mono@sha256:ecfe02a03176620d67a57a5bd33d52d22533c7909932d3d9758967c7363f02fa
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153007233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b13b149eed408ca6ebf5c6484710868571eb568a22417e14c9e17600db1721`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:20:48 GMT
ADD file:6e69a03d6dde108627b32e45abd197b90df267d161800ebec8416063a64aef06 in / 
# Fri, 08 Sep 2017 13:20:48 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:03:22 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Fri, 08 Sep 2017 15:03:22 GMT
ENV MONO_VERSION=4.8.0.524
# Fri, 08 Sep 2017 15:03:39 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:03:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:05:31 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:62bb183541ac6fc75244fe087faa7c427d0bc7cd70f749e3415bc6cb2e02638a`  
		Last Modified: Fri, 08 Sep 2017 13:29:31 GMT  
		Size: 37.4 MB (37433264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b46b12d9c14c1a58efcf657bb1ece830e223d45b6f6b47426f7069fd3eb16`  
		Last Modified: Fri, 08 Sep 2017 15:15:48 GMT  
		Size: 9.6 MB (9606347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def8499eb61ff5538eb97cd88a98aa2dbd2ccc9ee75b6c439d684048ef2d6199`  
		Last Modified: Fri, 08 Sep 2017 15:15:45 GMT  
		Size: 29.9 KB (29904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a0e076c959794a10fc9aff2ba5789e98b2fdae5738e7efb3b88c47a50fb26c`  
		Last Modified: Fri, 08 Sep 2017 15:16:18 GMT  
		Size: 105.9 MB (105937718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5`

```console
$ docker pull mono@sha256:13403222956c6f7cc82ea4a40107991bd6e72175042bd3cef9a199d7be2397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5` - linux; amd64

```console
$ docker pull mono@sha256:32bb515e885d5e5cca67490aee0678b727a4541b802ffe9ecf4f0c8f38734e79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167042114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186c16432ee5d9705f2447d7aade2109ccb5e6baa4b80fc20a9770d31310922`
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
# Wed, 13 Sep 2017 00:39:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:1f8e8d8a329df8f777594db64fabb3945cb84118d658241e2f8df5a590ed0267`  
		Last Modified: Wed, 13 Sep 2017 00:39:41 GMT  
		Size: 109.7 MB (109686237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm variant v7

```console
$ docker pull mono@sha256:fe4d50c35b36ef711fa45aeec10b6b3f3f8cb023c29a42b604f80f68052d92d6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d468a641fcd7ef69da276026315607dbafa0025e94d07bcce91c1902ebb824`
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
# Tue, 22 Aug 2017 20:37:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ab730f6bac4ef1c0f0d10be43eafa9c70e028a5ed32960f3ba1509fd3a71b7a7`  
		Last Modified: Tue, 22 Aug 2017 20:39:16 GMT  
		Size: 98.5 MB (98536076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c66cb460bd80ea896ce2033717aaa2637af44bc024ecc5ca99535c6181c02c0e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160488661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803f978922ec733b276b827e01ac1b968dc50e61255fc1aa675f6de4498a435c`
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
# Fri, 08 Sep 2017 21:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:e709a0d3e3ce778bad5004c45914becc348bad7a2248ccc033f364881b338302`  
		Last Modified: Fri, 08 Sep 2017 21:58:25 GMT  
		Size: 107.8 MB (107785976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5` - linux; 386

```console
$ docker pull mono@sha256:7600f29450588abc55360c785bf9192b7e361e37d6656652e1e8996f9eedc002
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169437931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21562c286248adf684456ac1309a6589aa887e7c45884daf126a01b97fa46d`
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
# Fri, 08 Sep 2017 15:10:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:856fcfadb75d8447fa682ea2070bc78d832248250f1456ba5d2a8edbf8d44d82`  
		Last Modified: Fri, 08 Sep 2017 15:11:30 GMT  
		Size: 110.2 MB (110150581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.0`

```console
$ docker pull mono@sha256:93c430b4d552690d629b711316b428569aeaae4f2c03cba0fb3c3eef2909f900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.0` - linux; amd64

```console
$ docker pull mono@sha256:7ffadf2a472968212e231517263e673e1cb7cfacc42b7b360ce92bde0ddb0dd3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164211207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad329c5d91020e245bfe553c7e23ddbff8c3df80d47e166d78044b9ec445447`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:05:00 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Thu, 07 Sep 2017 23:05:01 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:35:05 GMT
ENV MONO_VERSION=5.0.1.1
# Wed, 13 Sep 2017 00:35:28 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:35:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:36:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cd8ae3a8bb178e168078e96093b71d9adc6fc044e9fe1188425822b293f808`  
		Last Modified: Wed, 13 Sep 2017 00:40:12 GMT  
		Size: 5.0 MB (5012192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60963dc64ebbca888cd753ac13058991c9a39af3b7a4eb6449efdc8356091331`  
		Last Modified: Wed, 13 Sep 2017 00:40:10 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9182e56bb8abe6ed636e1edf3db74826bb310c949c8d9ac685af3c78315fa1d`  
		Last Modified: Wed, 13 Sep 2017 00:40:32 GMT  
		Size: 129.1 MB (129083813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:7ebff814a3e4b211688ee98a95c1e7e0edce520a13a1a5f0e0d6daad5ff3fb74
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143136919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45d2d8173a2075645b68720157d060d36e7841bb389f66168f22e61b1a4604a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 12:48:22 GMT
ADD file:e389776a9a3fc95d77b1de986f0ae670ac389527f87ee7b71a4ffc21c973dff0 in / 
# Tue, 25 Jul 2017 12:48:24 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:33:33 GMT
ENV MONO_VERSION=5.0.1.1
# Mon, 21 Aug 2017 18:42:01 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 18:42:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 18:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d2780fdc969b3bfd6ebba1e3649e76fc061ec96f60ff3460086bf2148f1a03d`  
		Last Modified: Tue, 25 Jul 2017 13:06:38 GMT  
		Size: 26.3 MB (26288325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572874c03564b4e14efa8d75656cab4fdbe02f8f6d89a776a5da2253a9b9e53c`  
		Last Modified: Tue, 22 Aug 2017 20:40:00 GMT  
		Size: 4.3 MB (4344422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013b25af7553c921ef5f4e016f6840bf913f6395c6670b3da3eef4261a4aa60`  
		Last Modified: Tue, 22 Aug 2017 20:39:52 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6283161d539b484f5e1f083fb7406f58168cda2d076a01e5aacea24fd7fd9af8`  
		Last Modified: Tue, 22 Aug 2017 20:41:20 GMT  
		Size: 112.5 MB (112502103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:819b1010bbab592af9c120de6346375bbe2b357f8c919ac3b5098ea56de2dda2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157631943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d6158b8e0b43b6b0c33fcf58b989110e01bbb7cc2fab7ce4b70248d1245713`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:24:21 GMT
ADD file:e941b26069cf288fadf2ab835d4f0c3a681f3f882d81686662d20f9642928795 in / 
# Fri, 08 Sep 2017 17:24:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:38:07 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 21:38:58 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 21:39:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 21:48:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:01c8fcecd171557c0af8130e86fd47e393a2791dc2ea655cb5f4f0ed6b95ef51`  
		Last Modified: Fri, 08 Sep 2017 17:36:14 GMT  
		Size: 27.5 MB (27480389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4494d0af88f8ae875ba7ce9b23aeaefca51c9c836adb02e2aa6f9d2caa5c1d`  
		Last Modified: Fri, 08 Sep 2017 21:59:48 GMT  
		Size: 4.5 MB (4504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009872ee5201a7fb5230f507975e25684424c7fe5fe1a59f39ebd208e11b350`  
		Last Modified: Fri, 08 Sep 2017 21:59:45 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1c815ffac30487a0da7c7d84f542faa5c0cccb76fa1e4d83e62325563093a`  
		Last Modified: Fri, 08 Sep 2017 22:01:11 GMT  
		Size: 125.6 MB (125645123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0` - linux; 386

```console
$ docker pull mono@sha256:8630e1ad8eb9f61846ac3d220883f4d0af71a60766cd20e457ede245ac0edd34
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166719618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7502ce2bd5973dca2e1b5e326df9a152852f45afd18eedca77448954841e9183`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:18:05 GMT
ADD file:cd8c8c04f635ce6e14de5271949afcf67b9c480ea35ba633423d385975e330ad in / 
# Fri, 08 Sep 2017 13:18:05 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:00:36 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 15:01:14 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:01:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:03:19 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:60dc9bcedd31a278f8b25a98451958fb75022352fe550042039e16ce32422ecf`  
		Last Modified: Fri, 08 Sep 2017 13:23:15 GMT  
		Size: 30.3 MB (30264166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b528578fc03834d74d71cf1a698eb7ec0865388e4d92d07392eef3781e6e528`  
		Last Modified: Fri, 08 Sep 2017 15:12:25 GMT  
		Size: 7.2 MB (7220126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb857166ff45c35204de020682db19937e3dba9861f63e23ae521388c9fa8e1`  
		Last Modified: Fri, 08 Sep 2017 15:12:22 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdcd762b235a6b980c6dc15173783850a90d52c8bb77283cdab311c0e9c703a`  
		Last Modified: Fri, 08 Sep 2017 15:13:05 GMT  
		Size: 129.2 MB (129233256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.0.1`

```console
$ docker pull mono@sha256:93c430b4d552690d629b711316b428569aeaae4f2c03cba0fb3c3eef2909f900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.0.1` - linux; amd64

```console
$ docker pull mono@sha256:7ffadf2a472968212e231517263e673e1cb7cfacc42b7b360ce92bde0ddb0dd3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164211207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad329c5d91020e245bfe553c7e23ddbff8c3df80d47e166d78044b9ec445447`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:05:00 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Thu, 07 Sep 2017 23:05:01 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:35:05 GMT
ENV MONO_VERSION=5.0.1.1
# Wed, 13 Sep 2017 00:35:28 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:35:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:36:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cd8ae3a8bb178e168078e96093b71d9adc6fc044e9fe1188425822b293f808`  
		Last Modified: Wed, 13 Sep 2017 00:40:12 GMT  
		Size: 5.0 MB (5012192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60963dc64ebbca888cd753ac13058991c9a39af3b7a4eb6449efdc8356091331`  
		Last Modified: Wed, 13 Sep 2017 00:40:10 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9182e56bb8abe6ed636e1edf3db74826bb310c949c8d9ac685af3c78315fa1d`  
		Last Modified: Wed, 13 Sep 2017 00:40:32 GMT  
		Size: 129.1 MB (129083813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:7ebff814a3e4b211688ee98a95c1e7e0edce520a13a1a5f0e0d6daad5ff3fb74
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143136919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45d2d8173a2075645b68720157d060d36e7841bb389f66168f22e61b1a4604a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 12:48:22 GMT
ADD file:e389776a9a3fc95d77b1de986f0ae670ac389527f87ee7b71a4ffc21c973dff0 in / 
# Tue, 25 Jul 2017 12:48:24 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:33:33 GMT
ENV MONO_VERSION=5.0.1.1
# Mon, 21 Aug 2017 18:42:01 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 18:42:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 18:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d2780fdc969b3bfd6ebba1e3649e76fc061ec96f60ff3460086bf2148f1a03d`  
		Last Modified: Tue, 25 Jul 2017 13:06:38 GMT  
		Size: 26.3 MB (26288325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572874c03564b4e14efa8d75656cab4fdbe02f8f6d89a776a5da2253a9b9e53c`  
		Last Modified: Tue, 22 Aug 2017 20:40:00 GMT  
		Size: 4.3 MB (4344422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013b25af7553c921ef5f4e016f6840bf913f6395c6670b3da3eef4261a4aa60`  
		Last Modified: Tue, 22 Aug 2017 20:39:52 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6283161d539b484f5e1f083fb7406f58168cda2d076a01e5aacea24fd7fd9af8`  
		Last Modified: Tue, 22 Aug 2017 20:41:20 GMT  
		Size: 112.5 MB (112502103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:819b1010bbab592af9c120de6346375bbe2b357f8c919ac3b5098ea56de2dda2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157631943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d6158b8e0b43b6b0c33fcf58b989110e01bbb7cc2fab7ce4b70248d1245713`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:24:21 GMT
ADD file:e941b26069cf288fadf2ab835d4f0c3a681f3f882d81686662d20f9642928795 in / 
# Fri, 08 Sep 2017 17:24:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:38:07 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 21:38:58 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 21:39:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 21:48:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:01c8fcecd171557c0af8130e86fd47e393a2791dc2ea655cb5f4f0ed6b95ef51`  
		Last Modified: Fri, 08 Sep 2017 17:36:14 GMT  
		Size: 27.5 MB (27480389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4494d0af88f8ae875ba7ce9b23aeaefca51c9c836adb02e2aa6f9d2caa5c1d`  
		Last Modified: Fri, 08 Sep 2017 21:59:48 GMT  
		Size: 4.5 MB (4504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009872ee5201a7fb5230f507975e25684424c7fe5fe1a59f39ebd208e11b350`  
		Last Modified: Fri, 08 Sep 2017 21:59:45 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1c815ffac30487a0da7c7d84f542faa5c0cccb76fa1e4d83e62325563093a`  
		Last Modified: Fri, 08 Sep 2017 22:01:11 GMT  
		Size: 125.6 MB (125645123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1` - linux; 386

```console
$ docker pull mono@sha256:8630e1ad8eb9f61846ac3d220883f4d0af71a60766cd20e457ede245ac0edd34
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166719618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7502ce2bd5973dca2e1b5e326df9a152852f45afd18eedca77448954841e9183`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:18:05 GMT
ADD file:cd8c8c04f635ce6e14de5271949afcf67b9c480ea35ba633423d385975e330ad in / 
# Fri, 08 Sep 2017 13:18:05 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:00:36 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 15:01:14 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:01:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:03:19 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:60dc9bcedd31a278f8b25a98451958fb75022352fe550042039e16ce32422ecf`  
		Last Modified: Fri, 08 Sep 2017 13:23:15 GMT  
		Size: 30.3 MB (30264166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b528578fc03834d74d71cf1a698eb7ec0865388e4d92d07392eef3781e6e528`  
		Last Modified: Fri, 08 Sep 2017 15:12:25 GMT  
		Size: 7.2 MB (7220126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb857166ff45c35204de020682db19937e3dba9861f63e23ae521388c9fa8e1`  
		Last Modified: Fri, 08 Sep 2017 15:12:22 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdcd762b235a6b980c6dc15173783850a90d52c8bb77283cdab311c0e9c703a`  
		Last Modified: Fri, 08 Sep 2017 15:13:05 GMT  
		Size: 129.2 MB (129233256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.0.1.1`

```console
$ docker pull mono@sha256:93c430b4d552690d629b711316b428569aeaae4f2c03cba0fb3c3eef2909f900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.0.1.1` - linux; amd64

```console
$ docker pull mono@sha256:7ffadf2a472968212e231517263e673e1cb7cfacc42b7b360ce92bde0ddb0dd3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164211207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad329c5d91020e245bfe553c7e23ddbff8c3df80d47e166d78044b9ec445447`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2017 23:05:00 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Thu, 07 Sep 2017 23:05:01 GMT
CMD ["bash"]
# Wed, 13 Sep 2017 00:35:05 GMT
ENV MONO_VERSION=5.0.1.1
# Wed, 13 Sep 2017 00:35:28 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 00:35:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 13 Sep 2017 00:36:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cd8ae3a8bb178e168078e96093b71d9adc6fc044e9fe1188425822b293f808`  
		Last Modified: Wed, 13 Sep 2017 00:40:12 GMT  
		Size: 5.0 MB (5012192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60963dc64ebbca888cd753ac13058991c9a39af3b7a4eb6449efdc8356091331`  
		Last Modified: Wed, 13 Sep 2017 00:40:10 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9182e56bb8abe6ed636e1edf3db74826bb310c949c8d9ac685af3c78315fa1d`  
		Last Modified: Wed, 13 Sep 2017 00:40:32 GMT  
		Size: 129.1 MB (129083813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1.1` - linux; arm variant v7

```console
$ docker pull mono@sha256:7ebff814a3e4b211688ee98a95c1e7e0edce520a13a1a5f0e0d6daad5ff3fb74
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143136919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45d2d8173a2075645b68720157d060d36e7841bb389f66168f22e61b1a4604a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Jul 2017 12:48:22 GMT
ADD file:e389776a9a3fc95d77b1de986f0ae670ac389527f87ee7b71a4ffc21c973dff0 in / 
# Tue, 25 Jul 2017 12:48:24 GMT
CMD ["bash"]
# Mon, 21 Aug 2017 18:33:33 GMT
ENV MONO_VERSION=5.0.1.1
# Mon, 21 Aug 2017 18:42:01 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 21 Aug 2017 18:42:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 21 Aug 2017 18:59:38 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:3d2780fdc969b3bfd6ebba1e3649e76fc061ec96f60ff3460086bf2148f1a03d`  
		Last Modified: Tue, 25 Jul 2017 13:06:38 GMT  
		Size: 26.3 MB (26288325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572874c03564b4e14efa8d75656cab4fdbe02f8f6d89a776a5da2253a9b9e53c`  
		Last Modified: Tue, 22 Aug 2017 20:40:00 GMT  
		Size: 4.3 MB (4344422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013b25af7553c921ef5f4e016f6840bf913f6395c6670b3da3eef4261a4aa60`  
		Last Modified: Tue, 22 Aug 2017 20:39:52 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6283161d539b484f5e1f083fb7406f58168cda2d076a01e5aacea24fd7fd9af8`  
		Last Modified: Tue, 22 Aug 2017 20:41:20 GMT  
		Size: 112.5 MB (112502103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1.1` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:819b1010bbab592af9c120de6346375bbe2b357f8c919ac3b5098ea56de2dda2
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157631943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d6158b8e0b43b6b0c33fcf58b989110e01bbb7cc2fab7ce4b70248d1245713`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 17:24:21 GMT
ADD file:e941b26069cf288fadf2ab835d4f0c3a681f3f882d81686662d20f9642928795 in / 
# Fri, 08 Sep 2017 17:24:22 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 21:38:07 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 21:38:58 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 21:39:03 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 21:48:26 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:01c8fcecd171557c0af8130e86fd47e393a2791dc2ea655cb5f4f0ed6b95ef51`  
		Last Modified: Fri, 08 Sep 2017 17:36:14 GMT  
		Size: 27.5 MB (27480389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4494d0af88f8ae875ba7ce9b23aeaefca51c9c836adb02e2aa6f9d2caa5c1d`  
		Last Modified: Fri, 08 Sep 2017 21:59:48 GMT  
		Size: 4.5 MB (4504367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7009872ee5201a7fb5230f507975e25684424c7fe5fe1a59f39ebd208e11b350`  
		Last Modified: Fri, 08 Sep 2017 21:59:45 GMT  
		Size: 2.1 KB (2064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1c815ffac30487a0da7c7d84f542faa5c0cccb76fa1e4d83e62325563093a`  
		Last Modified: Fri, 08 Sep 2017 22:01:11 GMT  
		Size: 125.6 MB (125645123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.0.1.1` - linux; 386

```console
$ docker pull mono@sha256:8630e1ad8eb9f61846ac3d220883f4d0af71a60766cd20e457ede245ac0edd34
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166719618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7502ce2bd5973dca2e1b5e326df9a152852f45afd18eedca77448954841e9183`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Sep 2017 13:18:05 GMT
ADD file:cd8c8c04f635ce6e14de5271949afcf67b9c480ea35ba633423d385975e330ad in / 
# Fri, 08 Sep 2017 13:18:05 GMT
CMD ["bash"]
# Fri, 08 Sep 2017 15:00:36 GMT
ENV MONO_VERSION=5.0.1.1
# Fri, 08 Sep 2017 15:01:14 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 15:01:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Fri, 08 Sep 2017 15:03:19 GMT
RUN echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:60dc9bcedd31a278f8b25a98451958fb75022352fe550042039e16ce32422ecf`  
		Last Modified: Fri, 08 Sep 2017 13:23:15 GMT  
		Size: 30.3 MB (30264166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b528578fc03834d74d71cf1a698eb7ec0865388e4d92d07392eef3781e6e528`  
		Last Modified: Fri, 08 Sep 2017 15:12:25 GMT  
		Size: 7.2 MB (7220126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb857166ff45c35204de020682db19937e3dba9861f63e23ae521388c9fa8e1`  
		Last Modified: Fri, 08 Sep 2017 15:12:22 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdcd762b235a6b980c6dc15173783850a90d52c8bb77283cdab311c0e9c703a`  
		Last Modified: Fri, 08 Sep 2017 15:13:05 GMT  
		Size: 129.2 MB (129233256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.2`

```console
$ docker pull mono@sha256:13403222956c6f7cc82ea4a40107991bd6e72175042bd3cef9a199d7be2397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2` - linux; amd64

```console
$ docker pull mono@sha256:32bb515e885d5e5cca67490aee0678b727a4541b802ffe9ecf4f0c8f38734e79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167042114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186c16432ee5d9705f2447d7aade2109ccb5e6baa4b80fc20a9770d31310922`
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
# Wed, 13 Sep 2017 00:39:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:1f8e8d8a329df8f777594db64fabb3945cb84118d658241e2f8df5a590ed0267`  
		Last Modified: Wed, 13 Sep 2017 00:39:41 GMT  
		Size: 109.7 MB (109686237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2` - linux; arm variant v7

```console
$ docker pull mono@sha256:fe4d50c35b36ef711fa45aeec10b6b3f3f8cb023c29a42b604f80f68052d92d6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d468a641fcd7ef69da276026315607dbafa0025e94d07bcce91c1902ebb824`
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
# Tue, 22 Aug 2017 20:37:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ab730f6bac4ef1c0f0d10be43eafa9c70e028a5ed32960f3ba1509fd3a71b7a7`  
		Last Modified: Tue, 22 Aug 2017 20:39:16 GMT  
		Size: 98.5 MB (98536076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c66cb460bd80ea896ce2033717aaa2637af44bc024ecc5ca99535c6181c02c0e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160488661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803f978922ec733b276b827e01ac1b968dc50e61255fc1aa675f6de4498a435c`
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
# Fri, 08 Sep 2017 21:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:e709a0d3e3ce778bad5004c45914becc348bad7a2248ccc033f364881b338302`  
		Last Modified: Fri, 08 Sep 2017 21:58:25 GMT  
		Size: 107.8 MB (107785976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2` - linux; 386

```console
$ docker pull mono@sha256:7600f29450588abc55360c785bf9192b7e361e37d6656652e1e8996f9eedc002
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169437931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21562c286248adf684456ac1309a6589aa887e7c45884daf126a01b97fa46d`
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
# Fri, 08 Sep 2017 15:10:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:856fcfadb75d8447fa682ea2070bc78d832248250f1456ba5d2a8edbf8d44d82`  
		Last Modified: Fri, 08 Sep 2017 15:11:30 GMT  
		Size: 110.2 MB (110150581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.2.0`

```console
$ docker pull mono@sha256:13403222956c6f7cc82ea4a40107991bd6e72175042bd3cef9a199d7be2397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2.0` - linux; amd64

```console
$ docker pull mono@sha256:32bb515e885d5e5cca67490aee0678b727a4541b802ffe9ecf4f0c8f38734e79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167042114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186c16432ee5d9705f2447d7aade2109ccb5e6baa4b80fc20a9770d31310922`
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
# Wed, 13 Sep 2017 00:39:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:1f8e8d8a329df8f777594db64fabb3945cb84118d658241e2f8df5a590ed0267`  
		Last Modified: Wed, 13 Sep 2017 00:39:41 GMT  
		Size: 109.7 MB (109686237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0` - linux; arm variant v7

```console
$ docker pull mono@sha256:fe4d50c35b36ef711fa45aeec10b6b3f3f8cb023c29a42b604f80f68052d92d6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d468a641fcd7ef69da276026315607dbafa0025e94d07bcce91c1902ebb824`
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
# Tue, 22 Aug 2017 20:37:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ab730f6bac4ef1c0f0d10be43eafa9c70e028a5ed32960f3ba1509fd3a71b7a7`  
		Last Modified: Tue, 22 Aug 2017 20:39:16 GMT  
		Size: 98.5 MB (98536076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c66cb460bd80ea896ce2033717aaa2637af44bc024ecc5ca99535c6181c02c0e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160488661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803f978922ec733b276b827e01ac1b968dc50e61255fc1aa675f6de4498a435c`
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
# Fri, 08 Sep 2017 21:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:e709a0d3e3ce778bad5004c45914becc348bad7a2248ccc033f364881b338302`  
		Last Modified: Fri, 08 Sep 2017 21:58:25 GMT  
		Size: 107.8 MB (107785976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0` - linux; 386

```console
$ docker pull mono@sha256:7600f29450588abc55360c785bf9192b7e361e37d6656652e1e8996f9eedc002
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169437931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21562c286248adf684456ac1309a6589aa887e7c45884daf126a01b97fa46d`
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
# Fri, 08 Sep 2017 15:10:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:856fcfadb75d8447fa682ea2070bc78d832248250f1456ba5d2a8edbf8d44d82`  
		Last Modified: Fri, 08 Sep 2017 15:11:30 GMT  
		Size: 110.2 MB (110150581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.2.0.215`

```console
$ docker pull mono@sha256:13403222956c6f7cc82ea4a40107991bd6e72175042bd3cef9a199d7be2397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2.0.215` - linux; amd64

```console
$ docker pull mono@sha256:32bb515e885d5e5cca67490aee0678b727a4541b802ffe9ecf4f0c8f38734e79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167042114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186c16432ee5d9705f2447d7aade2109ccb5e6baa4b80fc20a9770d31310922`
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
# Wed, 13 Sep 2017 00:39:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:1f8e8d8a329df8f777594db64fabb3945cb84118d658241e2f8df5a590ed0267`  
		Last Modified: Wed, 13 Sep 2017 00:39:41 GMT  
		Size: 109.7 MB (109686237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0.215` - linux; arm variant v7

```console
$ docker pull mono@sha256:fe4d50c35b36ef711fa45aeec10b6b3f3f8cb023c29a42b604f80f68052d92d6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d468a641fcd7ef69da276026315607dbafa0025e94d07bcce91c1902ebb824`
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
# Tue, 22 Aug 2017 20:37:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ab730f6bac4ef1c0f0d10be43eafa9c70e028a5ed32960f3ba1509fd3a71b7a7`  
		Last Modified: Tue, 22 Aug 2017 20:39:16 GMT  
		Size: 98.5 MB (98536076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0.215` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c66cb460bd80ea896ce2033717aaa2637af44bc024ecc5ca99535c6181c02c0e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160488661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803f978922ec733b276b827e01ac1b968dc50e61255fc1aa675f6de4498a435c`
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
# Fri, 08 Sep 2017 21:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:e709a0d3e3ce778bad5004c45914becc348bad7a2248ccc033f364881b338302`  
		Last Modified: Fri, 08 Sep 2017 21:58:25 GMT  
		Size: 107.8 MB (107785976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:5.2.0.215` - linux; 386

```console
$ docker pull mono@sha256:7600f29450588abc55360c785bf9192b7e361e37d6656652e1e8996f9eedc002
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169437931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21562c286248adf684456ac1309a6589aa887e7c45884daf126a01b97fa46d`
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
# Fri, 08 Sep 2017 15:10:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:856fcfadb75d8447fa682ea2070bc78d832248250f1456ba5d2a8edbf8d44d82`  
		Last Modified: Fri, 08 Sep 2017 15:11:30 GMT  
		Size: 110.2 MB (110150581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mono:5.2.0.215-slim`

```console
$ docker pull mono@sha256:8c655859efe282ec68105c644dbd0f0f17721a964726de3bfe2556d4973bf0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2.0.215-slim` - linux; amd64

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

### `mono:5.2.0.215-slim` - linux; arm variant v7

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

### `mono:5.2.0.215-slim` - linux; arm64 variant v8

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

### `mono:5.2.0.215-slim` - linux; 386

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

## `mono:5.2.0-slim`

```console
$ docker pull mono@sha256:8c655859efe282ec68105c644dbd0f0f17721a964726de3bfe2556d4973bf0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2.0-slim` - linux; amd64

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

### `mono:5.2.0-slim` - linux; arm variant v7

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

### `mono:5.2.0-slim` - linux; arm64 variant v8

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

### `mono:5.2.0-slim` - linux; 386

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

## `mono:5.2-slim`

```console
$ docker pull mono@sha256:8c655859efe282ec68105c644dbd0f0f17721a964726de3bfe2556d4973bf0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5.2-slim` - linux; amd64

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

### `mono:5.2-slim` - linux; arm variant v7

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

### `mono:5.2-slim` - linux; arm64 variant v8

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

### `mono:5.2-slim` - linux; 386

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

## `mono:5-slim`

```console
$ docker pull mono@sha256:8c655859efe282ec68105c644dbd0f0f17721a964726de3bfe2556d4973bf0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:5-slim` - linux; amd64

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

### `mono:5-slim` - linux; arm variant v7

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

### `mono:5-slim` - linux; arm64 variant v8

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

### `mono:5-slim` - linux; 386

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

## `mono:latest`

```console
$ docker pull mono@sha256:13403222956c6f7cc82ea4a40107991bd6e72175042bd3cef9a199d7be2397cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `mono:latest` - linux; amd64

```console
$ docker pull mono@sha256:32bb515e885d5e5cca67490aee0678b727a4541b802ffe9ecf4f0c8f38734e79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167042114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3186c16432ee5d9705f2447d7aade2109ccb5e6baa4b80fc20a9770d31310922`
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
# Wed, 13 Sep 2017 00:39:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:1f8e8d8a329df8f777594db64fabb3945cb84118d658241e2f8df5a590ed0267`  
		Last Modified: Wed, 13 Sep 2017 00:39:41 GMT  
		Size: 109.7 MB (109686237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm variant v7

```console
$ docker pull mono@sha256:fe4d50c35b36ef711fa45aeec10b6b3f3f8cb023c29a42b604f80f68052d92d6
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d468a641fcd7ef69da276026315607dbafa0025e94d07bcce91c1902ebb824`
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
# Tue, 22 Aug 2017 20:37:40 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:ab730f6bac4ef1c0f0d10be43eafa9c70e028a5ed32960f3ba1509fd3a71b7a7`  
		Last Modified: Tue, 22 Aug 2017 20:39:16 GMT  
		Size: 98.5 MB (98536076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; arm64 variant v8

```console
$ docker pull mono@sha256:c66cb460bd80ea896ce2033717aaa2637af44bc024ecc5ca99535c6181c02c0e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160488661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803f978922ec733b276b827e01ac1b968dc50e61255fc1aa675f6de4498a435c`
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
# Fri, 08 Sep 2017 21:57:07 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:e709a0d3e3ce778bad5004c45914becc348bad7a2248ccc033f364881b338302`  
		Last Modified: Fri, 08 Sep 2017 21:58:25 GMT  
		Size: 107.8 MB (107785976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mono:latest` - linux; 386

```console
$ docker pull mono@sha256:7600f29450588abc55360c785bf9192b7e361e37d6656652e1e8996f9eedc002
```

-	Docker Version: 17.03.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169437931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21562c286248adf684456ac1309a6589aa887e7c45884daf126a01b97fa46d`
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
# Fri, 08 Sep 2017 15:10:00 GMT
RUN apt-get update   && apt-get install -y binutils curl mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
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
	-	`sha256:856fcfadb75d8447fa682ea2070bc78d832248250f1456ba5d2a8edbf8d44d82`  
		Last Modified: Fri, 08 Sep 2017 15:11:30 GMT  
		Size: 110.2 MB (110150581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
