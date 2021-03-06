## `ros:kinetic-robot`

```console
$ docker pull ros@sha256:90912c181076c8fa2fc3d598a594d5349b019958603e29fe8153cd4e9d7370d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:13b82b21e92413870627b6d3205c43c7227123d8b9c26ab2548c0e7d65a6dcd5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.4 MB (446379433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce7ce489d5194d1f998922ce21a6e28d1a43eacc709659e487a3a094073c86b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Sep 2017 03:58:47 GMT
ADD file:39d3593ea220e686d5450244ef9dd6c934e3b288a29212d332ec33942b7bf218 in / 
# Wed, 13 Sep 2017 03:58:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 13 Sep 2017 03:58:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 13 Sep 2017 03:58:49 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 13 Sep 2017 03:58:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 13 Sep 2017 03:58:50 GMT
CMD ["/bin/bash"]
# Thu, 14 Sep 2017 00:41:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:41:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Thu, 14 Sep 2017 00:41:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Thu, 14 Sep 2017 00:42:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:42:03 GMT
ENV LANG=C.UTF-8
# Thu, 14 Sep 2017 00:42:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 14 Sep 2017 00:42:14 GMT
RUN rosdep init     && rosdep update
# Thu, 14 Sep 2017 00:42:14 GMT
ENV ROS_DISTRO=kinetic
# Thu, 14 Sep 2017 00:43:46 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:43:47 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Thu, 14 Sep 2017 00:43:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 14 Sep 2017 00:43:47 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 00:44:01 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2017 00:45:46 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5c6f90da05dc7e77d2e5fef63c341ab05ba2a03396ab5ae8f18814a7bbf5265`  
		Last Modified: Thu, 03 Aug 2017 11:51:31 GMT  
		Size: 47.3 MB (47258703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbe761fcb565a007b458e09e08ecb88947f647f57be819a492a6b23694cefd8`  
		Last Modified: Wed, 13 Sep 2017 03:59:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afa5ede606fb1845e42f0d4816d2a7593a2b666ff9ca4722dcd2cff8a541acf`  
		Last Modified: Wed, 13 Sep 2017 03:59:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7253b56f434d6e4d97d259cb1007481cf670df2e04229e83cf37db33d96eb`  
		Last Modified: Wed, 13 Sep 2017 03:59:35 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8db33536d447786cf57cca870fdd7d50d55fd67060c06252edc1c8db456a8f`  
		Last Modified: Wed, 13 Sep 2017 03:59:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93f9e1b344df5866d63798d95ee359c2090492fce14257bdd202dd89319e460`  
		Last Modified: Thu, 14 Sep 2017 01:24:29 GMT  
		Size: 5.4 MB (5362231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356bfc397f044f1ff6e56461f93c0bdf554515183068188102aafcdd866a5ad3`  
		Last Modified: Thu, 14 Sep 2017 01:24:27 GMT  
		Size: 13.1 KB (13080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448d214eef354e0c39d37fc345720720084a3676a556040d2fac4403e13801ab`  
		Last Modified: Thu, 14 Sep 2017 01:24:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85067b5b90b192ff2b7aa756271e7c9cc07a62845ae19d6c9366d712ae3756c2`  
		Last Modified: Thu, 14 Sep 2017 01:24:49 GMT  
		Size: 55.5 MB (55543619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e755fbada78a8c917aaddf71968a7da9af9f042fe0c8260ad45b0decf68f3`  
		Last Modified: Thu, 14 Sep 2017 01:24:25 GMT  
		Size: 754.0 KB (753963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bacf0fdc0ad14a48c5dca191d4ebd1c012500f99237ee7653aaab6efa8195e`  
		Last Modified: Thu, 14 Sep 2017 01:25:24 GMT  
		Size: 193.3 MB (193267434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b6396885c750c317461a7c6458ea7e9dbaa37b68f83a271c1dbf9100bef94d`  
		Last Modified: Thu, 14 Sep 2017 01:24:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7de9be4503fbbe6a3946906e2528f82d31c47be1cc8ce3cfc0bf5c538a01f0`  
		Last Modified: Thu, 14 Sep 2017 01:26:55 GMT  
		Size: 4.9 MB (4915173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a9880c742d4ea0a3a972df6b0fc1a8baeed1b7857f9b097714da70cc1d16d0`  
		Last Modified: Thu, 14 Sep 2017 01:27:48 GMT  
		Size: 139.3 MB (139262322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9ae5582a09a6c75f85e7c52766b13d9f4ca1e785dd7488fdb19425bc57fbb344
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 MB (389040476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b137741f813079d787519cf10cb955d7fccf73930bf26e3ef99c8afbb943c00`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 Sep 2017 01:29:45 GMT
ADD file:7ef9db764c81cb900a3f4e1fa08f7f9bbd5bd2b738534380d4b96612d2d94fe3 in / 
# Sat, 09 Sep 2017 01:29:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 09 Sep 2017 01:29:50 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 09 Sep 2017 01:29:52 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 09 Sep 2017 01:29:54 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 09 Sep 2017 01:29:55 GMT
CMD ["/bin/bash"]
# Mon, 11 Sep 2017 23:30:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Sep 2017 23:30:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Mon, 11 Sep 2017 23:30:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Mon, 11 Sep 2017 23:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Sep 2017 23:34:09 GMT
ENV LANG=C.UTF-8
# Mon, 11 Sep 2017 23:34:16 GMT
ENV LC_ALL=C.UTF-8
# Tue, 12 Sep 2017 20:26:39 GMT
RUN rosdep init     && rosdep update
# Tue, 12 Sep 2017 20:26:40 GMT
ENV ROS_DISTRO=kinetic
# Tue, 12 Sep 2017 20:35:11 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Sep 2017 20:35:16 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Tue, 12 Sep 2017 20:35:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 12 Sep 2017 20:35:20 GMT
CMD ["bash"]
# Tue, 12 Sep 2017 20:36:26 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Sep 2017 20:44:02 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93170abd0836466ba561e86bf19d8596fdfaf4e3c826c99036aabfa64f337af6`  
		Last Modified: Thu, 17 Aug 2017 23:35:59 GMT  
		Size: 42.2 MB (42173096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4479f35d4daad1fcea526f012ed9e376c37b11ac5f0b19eae196c9e6198d7962`  
		Last Modified: Sat, 09 Sep 2017 01:31:24 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96313b9474adb2b1810740169253ce78f85adef20457754529bdfc18556e7f4`  
		Last Modified: Sat, 09 Sep 2017 01:31:24 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c7e8b5fdbd37a83bfea18b6f612e665c8ac92fc65319039cc6cb017a55901c`  
		Last Modified: Sat, 09 Sep 2017 01:31:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bafc350c2d83248cdbb3a95658150514c8b14c17df0b7755531ed1f992296ff`  
		Last Modified: Sat, 09 Sep 2017 01:31:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab2f5bbfa17536010e0daf2605aa88df897cf962bc243adb5200a4ae67117fe`  
		Last Modified: Tue, 12 Sep 2017 21:33:26 GMT  
		Size: 4.6 MB (4613461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1e7b3e0e63089e43711354c5e90b9c0509aff08ec65a8d542486060f5607b0`  
		Last Modified: Tue, 12 Sep 2017 21:33:14 GMT  
		Size: 13.1 KB (13079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f941e17a4b6e49558564e4457f89a1f68d4b0a4d8b69c57e4d0fa78b962f90d`  
		Last Modified: Tue, 12 Sep 2017 21:33:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8809b322f182d7c0c5f97e75f1881ec3a3a4ce75884399e91bc5c57aee2bd19c`  
		Last Modified: Tue, 12 Sep 2017 21:34:35 GMT  
		Size: 50.7 MB (50703769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093644b1b1a7eace4035b6d31d108434bd74e1f0f0880be4666cd9d2e4c58a7c`  
		Last Modified: Tue, 12 Sep 2017 21:33:07 GMT  
		Size: 754.0 KB (754032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35ed4590cf5422852938d070c7dd9c44aa6cf09389b063b89dcb220d37fe1ba`  
		Last Modified: Tue, 12 Sep 2017 21:36:04 GMT  
		Size: 164.7 MB (164666566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39adcf0bad2f69f202b435cbd5a395054a0a8a6f09d493be2f7262605a94e9b5`  
		Last Modified: Tue, 12 Sep 2017 21:33:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e19ed6ee30aea78431695136576639ac8eb2f53d7d601926a23f1dc6c709c0`  
		Last Modified: Tue, 12 Sep 2017 21:36:30 GMT  
		Size: 4.5 MB (4472059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9ec958c95316cab7543f664235a08f7074123da387e38e65e6f8dcd8e70637`  
		Last Modified: Tue, 12 Sep 2017 21:38:19 GMT  
		Size: 121.6 MB (121641505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e61b415c49ff81d313848a9ba012ccd88e6bd089b25d5bf189bb36978de94c22
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.6 MB (405558139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4e823cad8e5e2f6d0a8395c0a9643b07d64ad33cc6de02154f36b981653160`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Aug 2017 14:01:23 GMT
ADD file:09391963d2be8fbd3d1fa1ec76749357eebb062e3750ef9cdc1af1ee5b946f26 in / 
# Fri, 11 Aug 2017 14:01:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 11 Aug 2017 14:01:26 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 11 Aug 2017 14:01:27 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 11 Aug 2017 14:01:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 11 Aug 2017 14:01:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2017 14:17:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2017 14:17:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Wed, 16 Aug 2017 14:17:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Wed, 16 Aug 2017 14:19:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2017 14:19:48 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2017 14:19:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2017 14:20:26 GMT
RUN rosdep init     && rosdep update
# Thu, 17 Aug 2017 14:17:07 GMT
ENV ROS_DISTRO=kinetic
# Thu, 17 Aug 2017 14:22:13 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2017 14:22:15 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Thu, 17 Aug 2017 14:22:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2017 14:22:16 GMT
CMD ["bash"]
# Thu, 17 Aug 2017 14:23:05 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2017 14:30:55 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:97439f7dbdf1c01245623f97141afe52402dd6430ffa14f0bba51c3f97b1477c`  
		Last Modified: Fri, 04 Aug 2017 22:13:13 GMT  
		Size: 43.2 MB (43174322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e53a6f7623035342dd76dfd0e2e0ec35a3730ea26b9ebfdb11d6be19142706`  
		Last Modified: Fri, 11 Aug 2017 14:03:02 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792600934860e87147b88b22c2f7e5207a1991bf211afc8550ed7e94ae59d924`  
		Last Modified: Fri, 11 Aug 2017 14:03:02 GMT  
		Size: 538.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7792a57af45eeb418423a4a50b243db8a19bd5df9fe00a5a0f70ea4b1416b57e`  
		Last Modified: Fri, 11 Aug 2017 14:03:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f7b5f2a37b1082e3fa4d27dd9078d0c627fca8de3aa6ba5aa9587aac8be8dd`  
		Last Modified: Fri, 11 Aug 2017 14:03:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527f0a2a084c04b0cf96d359dcccaf72255e0476419296f0dfcfe9915dc5ac9`  
		Last Modified: Wed, 16 Aug 2017 15:29:47 GMT  
		Size: 4.8 MB (4819010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ec49cbba1731f8f8b3b1f54afa91352dc56093927543356785949306d11480`  
		Last Modified: Wed, 16 Aug 2017 15:29:42 GMT  
		Size: 13.1 KB (13081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12fd03049af8dedf5a2e822814cd269b8c9cfb70b6882111ab2c8e53d71d46e`  
		Last Modified: Wed, 16 Aug 2017 15:29:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea636f5920ba434da460d90a7764e45a0afac7fcf0dc7ddd3947a68c22242b0`  
		Last Modified: Wed, 16 Aug 2017 15:30:15 GMT  
		Size: 52.4 MB (52400817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18efa9c94988a5b52dd5863324ff24a5078cc919eb13a5b21eb9dd513fa738ba`  
		Last Modified: Wed, 16 Aug 2017 15:29:39 GMT  
		Size: 754.7 KB (754711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141b84014bac13610185aa66cccf0fb21635cc51fc21af65f64b2779fe3ac251`  
		Last Modified: Thu, 17 Aug 2017 15:14:23 GMT  
		Size: 173.9 MB (173919030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f597297cad477e53a198bb4c90d0928b70ebcfbfa2f909865b5d20ff25b7eb`  
		Last Modified: Thu, 17 Aug 2017 15:13:17 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c3904a51b4227d752087a7ac14b8f4723d4cf86e486f9c8c8e52685f7728d0`  
		Last Modified: Thu, 17 Aug 2017 15:14:41 GMT  
		Size: 4.8 MB (4767716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a174cf9bbdcfbdf380930daf839ba5137f8470b25cdfcc1619c3e301b0a178`  
		Last Modified: Thu, 17 Aug 2017 15:15:51 GMT  
		Size: 125.7 MB (125706617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
