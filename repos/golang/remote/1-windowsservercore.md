## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:d9ef443b10e244e4adfd817502d7fa821148c18d473fd2810a9d8f25b7307746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1593; amd64

### `golang:1-windowsservercore` - windows version 10.0.14393.1593; amd64

```console
$ docker pull golang@sha256:d2a0f5ac5d53be21c52e309549198e26357756268fd97e8f9614a36386fa841a
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5476375396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c78f7ab6bce330483aa08f1d3aebac88723f221ccf88a51bbc18d610b0c683`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Mon, 07 Aug 2017 23:55:17 GMT
RUN Install update 10.0.14393.1593
# Wed, 09 Aug 2017 23:02:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Aug 2017 23:02:49 GMT
ENV GIT_VERSION=2.11.1
# Wed, 09 Aug 2017 23:02:52 GMT
ENV GIT_TAG=v2.11.1.windows.1
# Wed, 09 Aug 2017 23:02:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.11.1.windows.1/MinGit-2.11.1-64-bit.zip
# Wed, 09 Aug 2017 23:02:57 GMT
ENV GIT_DOWNLOAD_SHA256=668d16a799dd721ed126cc91bed49eb2c072ba1b25b50048280a4e2c5ed56e59
# Wed, 09 Aug 2017 23:03:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  git --version'; git --version; 		Write-Host 'Complete.';
# Wed, 09 Aug 2017 23:03:49 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Aug 2017 23:04:10 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 25 Aug 2017 00:07:47 GMT
ENV GOLANG_VERSION=1.9
# Fri, 25 Aug 2017 00:11:21 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '874b144b994643cff1d3f5875369d65c01c216bb23b8edddf608facc43966c8b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Fri, 25 Aug 2017 00:11:26 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f5eeabe6154feaf01ca3bf333d9936a1e0803a4998279a74f27e5012605eff4`  
		Size: 1.3 GB (1257698307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ccc26568c531f834e36947c2392a7ef8702cad1e6ae3c8ee6f3887b588d68de3`  
		Last Modified: Wed, 09 Aug 2017 23:22:26 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2461b5d23777d595639dbcfd94b314ce68b271ae9d03d65f26aec29cc03a638`  
		Last Modified: Wed, 09 Aug 2017 23:22:26 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d716c85deb4ca39cbb12696d83f08ea8c226171b12071731f66e8a0056edade7`  
		Last Modified: Wed, 09 Aug 2017 23:22:24 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21316779ba82b63367b8828bfe39b2e1d89d8d160029f5be2c0b03674d80159f`  
		Last Modified: Wed, 09 Aug 2017 23:22:22 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9138ea572b95cbe2decbd1dc194b547925094cf33c30755fa1b2fd0427018d13`  
		Last Modified: Wed, 09 Aug 2017 23:22:22 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563393b476b86653ae40533a9392c711fcbf9e092246278d76184e799092cca6`  
		Last Modified: Wed, 09 Aug 2017 23:22:29 GMT  
		Size: 29.2 MB (29183702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080c30beacd1c8e8cd41ad1b4798474546ff75350d5951ca9fdd6be903b904ec`  
		Last Modified: Wed, 09 Aug 2017 23:22:17 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a0c6238373507e8174da22c0bd9871bd1b49abb95d81b70d44881f209bb5e`  
		Last Modified: Wed, 09 Aug 2017 23:22:20 GMT  
		Size: 4.8 MB (4758224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def4b20b5759f8e3919ec514c3cf9564dbada16eb1ad7d2ba492b32ec161436`  
		Last Modified: Fri, 25 Aug 2017 00:14:55 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680cbb81a807fe00245f856c46d4c1655e6c7fb3d42e0d430c84d7979fc42dab`  
		Last Modified: Fri, 25 Aug 2017 00:15:15 GMT  
		Size: 114.7 MB (114739334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5069e23598f016a220e7be63bfbc3e4a54336fc0c90f61a0b27185034b9d6b8`  
		Last Modified: Fri, 25 Aug 2017 00:14:55 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
