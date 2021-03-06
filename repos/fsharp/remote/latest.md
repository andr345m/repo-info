## `fsharp:latest`

```console
$ docker pull fsharp@sha256:bec6346a74c39bb95ee3ce5a873021e41d745e4d08c8621be987d5cce21b39e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:latest` - linux; amd64

```console
$ docker pull fsharp@sha256:6adfb5c141b2af7ee39cfe8920f73538fa2ecd44cdabd2709cb9c28c6aa9ab2f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178869730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ed31a75f9b1be6a20037d6b1858e20321b8b70217ba493f245e0ec3f3eb4ac`
-	Default Command: `["fsharpi"]`

```dockerfile
# Wed, 13 Sep 2017 08:40:50 GMT
ADD file:bdab114a5717b42a5e02e6f602d5eeb48fc998a60d200704b4da1a7ce8552775 in / 
# Wed, 13 Sep 2017 08:40:50 GMT
CMD ["bash"]
# Thu, 14 Sep 2017 00:43:20 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 14 Sep 2017 00:43:20 GMT
ENV MONO_THREADS_PER_CPU=50
# Thu, 14 Sep 2017 00:59:25 GMT
RUN MONO_VERSION=5.0.1.1 &&     FSHARP_VERSION=4.1.25 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Thu, 14 Sep 2017 00:59:25 GMT
WORKDIR /root
# Thu, 14 Sep 2017 00:59:26 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:065132d9f7059b525640520932c776949f4d0d744b65429f1026f3d4d9b3615a`  
		Last Modified: Thu, 07 Sep 2017 23:11:57 GMT  
		Size: 30.1 MB (30113134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844ec28d02855be6f737f1449be027908361e1d59463c6b26b4dfaec8eb2f7c0`  
		Last Modified: Thu, 14 Sep 2017 01:34:10 GMT  
		Size: 148.8 MB (148756596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
