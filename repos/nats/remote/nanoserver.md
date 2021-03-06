## `nats:nanoserver`

```console
$ docker pull nats@sha256:921a5869a6f2b36585a9fbbc45a596a4650ac1f0b949c2c041550be366d5f092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `nats:nanoserver` - windows version 10.0.14393.1593; amd64

```console
$ docker pull nats@sha256:0aa54a432df0f10fd28ce93183a7591ec645225fad8a879911d7b024a2e08d5e
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 MB (392180611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb37aa1e28247863434b7c945d799d4696ae3b8acee78583bd6dd069c033256`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:54:45 GMT
RUN Install update 10.0.14393.1593
# Sun, 20 Aug 2017 23:38:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sun, 20 Aug 2017 23:38:30 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Sun, 20 Aug 2017 23:38:33 GMT
RUN cmd /S /C #(nop) COPY file:af5c8dcfdefca52dc8554bf8d71fa681363602b0e9ce7082275f43a8a56aab5a in gnatsd.exe 
# Sun, 20 Aug 2017 23:38:36 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Sun, 20 Aug 2017 23:38:37 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Sun, 20 Aug 2017 23:38:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Sun, 20 Aug 2017 23:38:41 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:38cc73423ca1d089e2e2374a8baf65d25d3792b22a22263c702f22f85bea6d4c`  
		Size: 137.4 MB (137351829 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:747f020d7a435c8107b7ffefecfb40fec54b97754ec15bd428d8b4b262bf7a5e`  
		Last Modified: Sun, 20 Aug 2017 23:39:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248fda769c0bf949f537bf7c7b7deb4c81cf84e2f076b68eba7f779cc6150e30`  
		Last Modified: Sun, 20 Aug 2017 23:39:12 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a1666000e2b5c1bc5b9329c8fb70635b33b498c29a65f0eb772f80e1f010ba`  
		Last Modified: Sun, 20 Aug 2017 23:39:10 GMT  
		Size: 2.1 MB (2131054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89af6ecae7e5411f4a90f53db311189e68d0fe3871b57057ffb7a90226dab2a3`  
		Last Modified: Sun, 20 Aug 2017 23:39:10 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fd50bb97c56370126a24efadacd0d3d3b38687d4c5b5f2519a850f674e67c4`  
		Last Modified: Sun, 20 Aug 2017 23:39:10 GMT  
		Size: 969.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da1ec556ef79b330f22c7a3a64155cefb9af8087c2e11be34660ea7db26db28`  
		Last Modified: Sun, 20 Aug 2017 23:39:10 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3341ff5958290b6b9c8d6a270be583bdee9d98766c87e85b7b1bf803abe8fc75`  
		Last Modified: Sun, 20 Aug 2017 23:39:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
