## `python:windowsservercore`

```console
$ docker pull python@sha256:6bd3cdd392f6987c4b0ad27529501004ec0bb2b94962d557e4755e60bf2da35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.1715; amd64

### `python:windowsservercore` - windows version 10.0.14393.1715; amd64

```console
$ docker pull python@sha256:e2ceee8b6224d30047a0d74d038b17617aeba7d92c7b603419bf3098d104d1ab
```

-	Docker Version: 17.03.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5391939739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e979c0a49c6ca761c1e8d61f8f41c6ab3963389c93efaef6d22e1d4913f7c528`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 12 Sep 2017 22:02:46 GMT
RUN Install update 10.0.14393.1715
# Thu, 14 Sep 2017 16:25:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Sep 2017 16:25:12 GMT
ENV PYTHON_VERSION=3.6.2
# Thu, 14 Sep 2017 16:25:15 GMT
ENV PYTHON_RELEASE=3.6.2
# Thu, 14 Sep 2017 16:26:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	(New-Object System.Net.WebClient).DownloadFile($url, 'python.exe'); 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Thu, 14 Sep 2017 16:26:31 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Thu, 14 Sep 2017 16:27:18 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	(New-Object System.Net.WebClient).DownloadFile('https://bootstrap.pypa.io/get-pip.py', 'get-pip.py'); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Thu, 14 Sep 2017 16:27:20 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da87b55a9b6358a65462540faeaa97505b0a12e1a2c14f08893589181d32d00d`  
		Size: 1.3 GB (1265822551 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d9a80234ea5aa1b3fdb0960fc47b11cc20b357170851b348ddd413a7be726094`  
		Last Modified: Thu, 14 Sep 2017 16:32:17 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551dfe8e3c6fc1dc5662f31e80304dbf76b0670114ec4ebc9351cf734632a57e`  
		Last Modified: Thu, 14 Sep 2017 16:32:18 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928238f3389b1be0a25dba6e01c042720f79ed68c28fb531c8fd98f5d4928f5`  
		Last Modified: Thu, 14 Sep 2017 16:32:13 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3749b7c2ee2e969afc4c3621987883eb41fa86646d9dca1550ca7c9c3aef3484`  
		Last Modified: Thu, 14 Sep 2017 16:32:23 GMT  
		Size: 46.9 MB (46851867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa144886a8def4c1bf4b76eb0d4207517a38709ecf5446dddd58af9498446500`  
		Last Modified: Thu, 14 Sep 2017 16:32:13 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1b3e9fa5a23aadef827127a72eb0b0bf41edbe75ce6177e3297ebd0274c0c3`  
		Last Modified: Thu, 14 Sep 2017 16:32:16 GMT  
		Size: 9.3 MB (9273316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723ed185e103d96b711980effd6b0114090701cdc60be548f1bd2158b92c046`  
		Last Modified: Thu, 14 Sep 2017 16:32:13 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
