## `jenkins:latest`

```console
$ docker pull jenkins@sha256:84b6c9615a4b4275bc1a0a90de2907c8cd484117daff8c811544ac71a8fa21f4
```

-	Platforms:
	-	linux; amd64

### `jenkins:latest` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366053448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f118a7695f9955159c08a63c35db6fb818ab0ce74cf6fe3a454e608efea7c72`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/jenkins.sh"]`

```dockerfile
# Thu, 07 Sep 2017 23:07:26 GMT
ADD file:a7405474b639b2239b96a93d02803224c052a390fe42b3f9080f2ad07de94640 in / 
# Thu, 07 Sep 2017 23:07:26 GMT
CMD ["bash"]
# Thu, 07 Sep 2017 23:30:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2017 23:30:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg2 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 07 Sep 2017 23:30:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 08:55:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 08 Sep 2017 08:55:13 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2017 08:55:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 08 Sep 2017 08:55:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 08 Sep 2017 08:55:15 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 08 Sep 2017 08:55:16 GMT
ENV JAVA_VERSION=8u141
# Fri, 08 Sep 2017 08:55:16 GMT
ENV JAVA_DEBIAN_VERSION=8u141-b15-1~deb9u1
# Fri, 08 Sep 2017 08:55:16 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 08 Sep 2017 08:56:26 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 08 Sep 2017 08:56:28 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Mon, 11 Sep 2017 05:08:38 GMT
RUN apt-get update && apt-get install -y git curl && rm -rf /var/lib/apt/lists/*
# Mon, 11 Sep 2017 05:08:38 GMT
ARG user=jenkins
# Mon, 11 Sep 2017 05:08:38 GMT
ARG group=jenkins
# Mon, 11 Sep 2017 05:08:39 GMT
ARG uid=1000
# Mon, 11 Sep 2017 05:08:39 GMT
ARG gid=1000
# Mon, 11 Sep 2017 05:08:39 GMT
ARG http_port=8080
# Mon, 11 Sep 2017 05:08:40 GMT
ARG agent_port=50000
# Mon, 11 Sep 2017 05:08:40 GMT
ENV JENKINS_HOME=/var/jenkins_home
# Mon, 11 Sep 2017 05:08:40 GMT
ENV JENKINS_SLAVE_AGENT_PORT=50000
# Mon, 11 Sep 2017 05:08:41 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN groupadd -g ${gid} ${group}     && useradd -d "$JENKINS_HOME" -u ${uid} -g ${gid} -m -s /bin/bash ${user}
# Mon, 11 Sep 2017 05:08:41 GMT
VOLUME [/var/jenkins_home]
# Mon, 11 Sep 2017 05:08:42 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN mkdir -p /usr/share/jenkins/ref/init.groovy.d
# Mon, 11 Sep 2017 05:08:43 GMT
ENV TINI_VERSION=0.14.0
# Mon, 11 Sep 2017 05:08:43 GMT
ENV TINI_SHA=6c41ec7d33e857d4779f14d9c74924cab0c7973485d2972419a3b7c7620ff5fd
# Mon, 11 Sep 2017 05:08:46 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN curl -fsSL https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-static-amd64 -o /bin/tini && chmod +x /bin/tini   && echo "$TINI_SHA  /bin/tini" | sha256sum -c -
# Mon, 11 Sep 2017 05:08:47 GMT
COPY file:c629bc0b9ecb5b7233000c973f65721df4ce1307a5d5b33ac3871ff61a9172ff in /usr/share/jenkins/ref/init.groovy.d/tcp-slave-agent-port.groovy 
# Mon, 11 Sep 2017 05:08:47 GMT
ARG JENKINS_VERSION
# Mon, 11 Sep 2017 15:36:51 GMT
ENV JENKINS_VERSION=2.60.3
# Mon, 11 Sep 2017 15:36:51 GMT
ARG JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a
# Mon, 11 Sep 2017 15:36:52 GMT
ARG JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war
# Mon, 11 Sep 2017 15:36:57 GMT
# ARGS: JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN curl -fsSL ${JENKINS_URL} -o /usr/share/jenkins/jenkins.war   && echo "${JENKINS_SHA}  /usr/share/jenkins/jenkins.war" | sha256sum -c -
# Mon, 11 Sep 2017 15:37:00 GMT
ENV JENKINS_UC=https://updates.jenkins.io
# Mon, 11 Sep 2017 15:37:00 GMT
ENV JENKINS_UC_EXPERIMENTAL=https://updates.jenkins.io/experimental
# Mon, 11 Sep 2017 15:37:01 GMT
# ARGS: JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN chown -R ${user} "$JENKINS_HOME" /usr/share/jenkins/ref
# Mon, 11 Sep 2017 15:37:02 GMT
EXPOSE 8080/tcp
# Mon, 11 Sep 2017 15:37:02 GMT
EXPOSE 50000/tcp
# Mon, 11 Sep 2017 15:37:02 GMT
ENV COPY_REFERENCE_FILE_LOG=/var/jenkins_home/copy_reference_file.log
# Mon, 11 Sep 2017 15:37:08 GMT
USER [jenkins]
# Mon, 11 Sep 2017 15:37:09 GMT
COPY file:26c3c5818bc87662d1f4905a3ed73bd55a0a75f731c7dc52d0599c00f51408e9 in /usr/local/bin/jenkins-support 
# Mon, 11 Sep 2017 15:37:10 GMT
COPY file:1a774b24a2bbd880e2ce47b3d642b8c04bbdbede0f2256dbdb11f62b65f696ba in /usr/local/bin/jenkins.sh 
# Mon, 11 Sep 2017 15:37:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/jenkins.sh"]
# Mon, 11 Sep 2017 15:37:11 GMT
COPY file:9f0a7faf8951842e0f42c1a3f3bb54ff4ec5263064508077347c57376da68b46 in /usr/local/bin/plugins.sh 
# Mon, 11 Sep 2017 15:37:12 GMT
COPY file:a4f750618f51f00d2f8268ac43fdd8d8ef5ce16e1d412afa5a9bc7492a5d975f in /usr/local/bin/install-plugins.sh 
```

-	Layers:
	-	`sha256:219d2e45b4afc3d80375a2fcf76505684de01f55027fb35a691099f0e538fdd8`  
		Last Modified: Thu, 07 Sep 2017 23:20:31 GMT  
		Size: 45.1 MB (45125497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a482fbcfe4075b3bf46ba44ce501ab9fa42067dd341003b450dca9569a25857f`  
		Last Modified: Thu, 07 Sep 2017 23:56:24 GMT  
		Size: 11.1 MB (11102630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980edaaff53b44cce16a276125944851f730f29a03d970db878a0c71206460b2`  
		Last Modified: Thu, 07 Sep 2017 23:56:23 GMT  
		Size: 4.4 MB (4411946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44dc7c129fe363ccac06134040592ae57125218629e5b7913aaef7e0c63e3db`  
		Last Modified: Thu, 07 Sep 2017 23:56:57 GMT  
		Size: 50.0 MB (50015366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34a55a78629d1810896a463ad235a043bfb76771657326e7f12a5d6b5462711`  
		Last Modified: Sat, 09 Sep 2017 00:34:34 GMT  
		Size: 661.9 KB (661916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0608417860f2fbf351f5691f518ecedd1b5e0fbc6a09ff9df6fc4e9cbe1d617`  
		Last Modified: Sat, 09 Sep 2017 00:34:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ffb0683f1a94850d234bc16a57845dbbb8096706ac2f498cfa6227b5d34c88`  
		Last Modified: Sat, 09 Sep 2017 00:34:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ab86bd63bcf0ac2f592a1ea2e581af4508a5097bdfdde4a148d9c8ce57fbdf`  
		Last Modified: Sat, 09 Sep 2017 00:35:14 GMT  
		Size: 183.7 MB (183688010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e8d28e95f8e809aafb72c4c445a45bb7f3d1f388754776e7e3abc9cd144048`  
		Last Modified: Sat, 09 Sep 2017 00:34:34 GMT  
		Size: 272.0 KB (271989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6ad9f8a749ea4b8a11775a297da1d6fd4216d3f6c13e57c44ff4a8a5b8229`  
		Last Modified: Mon, 11 Sep 2017 05:09:13 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caea7ba6c3e70b666dbd6008bb62249b42f4ff0470f587840acfa2004a5a55a`  
		Last Modified: Mon, 11 Sep 2017 05:09:12 GMT  
		Size: 4.2 KB (4159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cfd5fe294ab40e348ef3deccf419b1c89bc06d481d8e6dd3db0ef6476da129`  
		Last Modified: Mon, 11 Sep 2017 05:09:12 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd1db8a084be7ebedca190039a6392cbfeb78a937a9bc3d6095af9338a46fb`  
		Last Modified: Mon, 11 Sep 2017 05:09:12 GMT  
		Size: 354.8 KB (354775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0effb33601d65cdd1a68eec7cd4f44402ce390e8ecad286d87cadd83388a20a`  
		Last Modified: Mon, 11 Sep 2017 05:09:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44ed6ff78d38cccdd091a57dd0d40ca14fb9164db99ae07639cdabc4c6b6c85`  
		Last Modified: Mon, 11 Sep 2017 15:37:58 GMT  
		Size: 70.4 MB (70409093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3faed2e710ab7bbbd610296633bcc89180dbd8b216cef8742c9142d752e501d6`  
		Last Modified: Mon, 11 Sep 2017 15:37:53 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419efd8022d3e2abe4cb9d5df171599a55677b7af49b422bcaf95dd2a153f989`  
		Last Modified: Mon, 11 Sep 2017 15:37:53 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922937d7045b03357cbd765e50ff28aeff6dda10b987fc53ccc93a9462b1cacc`  
		Last Modified: Mon, 11 Sep 2017 15:37:53 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f053067a66df13f1e44e7a35bc96a72811cdd715fee4984c2f3a40124313ae`  
		Last Modified: Mon, 11 Sep 2017 15:37:53 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a319c3ba246448874b9d4c3735fbd42e6b86a8577be75f7aff9cb968ce2ab6`  
		Last Modified: Mon, 11 Sep 2017 15:37:53 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
