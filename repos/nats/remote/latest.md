## `nats:latest`

```console
$ docker pull nats@sha256:4b0edace2daf8dfd6d7b93addff9eabd4a89a398c51a9930263fb9e0ad938d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:62eeee7a6b391d60ed4c8a808733867b6c7024a4eedf01cf3688ed4f30e2609d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5d0988d1236bfeb5680ea6c3bc2b5c61b8fc94539dd228b3dc9ce867c4f730`
-	Entrypoint: `["\/gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Wed, 13 Sep 2017 10:22:17 GMT
COPY file:8328e71a6e7f74003ba186b6557bdeff4587b91b09e1617cb5aa65dac4682108 in /gnatsd 
# Wed, 13 Sep 2017 10:22:17 GMT
COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Wed, 13 Sep 2017 10:22:17 GMT
EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Wed, 13 Sep 2017 10:22:17 GMT
ENTRYPOINT ["/gnatsd"]
# Wed, 13 Sep 2017 10:22:18 GMT
CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:700f0111179bbb06d1b4437274a22231315203a64b216aee19bbc5323f50f730`  
		Last Modified: Wed, 13 Sep 2017 10:22:24 GMT  
		Size: 2.1 MB (2125981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f18ebfeb0687d398f682bd15c5e8abfa2c27fafcf9d52c2bdbea1a36a61f05e`  
		Last Modified: Wed, 13 Sep 2017 10:22:23 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
