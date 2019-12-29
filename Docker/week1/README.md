# Docker Week1
## Docker 설치및 설정
```bash
$ curl -fsSL https://get.docker.com/ | sudo sh
```  
혹은  
```bash
$ curl -fsSL get.docker.com -o get-docker.sh
```
```bash
$./get-docker.sh
```

## Docker Version & GROUP Setting
```bash
$ sudo usermod -aG docker $USERNAME
```
```bash
Client: Docker Engine - Community
 Version:           19.03.5
 API version:       1.40
 Go version:        go1.12.12
 Git commit:        633a0ea
 Built:             Wed Nov 13 07:37:22 2019
 OS/Arch:           linux/arm
 Experimental:      false

Server: Docker Engine - Community
 Engine:
  Version:          19.03.5
  API version:      1.40 (minimum version 1.12)
  Go version:       go1.12.12
  Git commit:       633a0ea
  Built:            Wed Nov 13 07:31:17 2019
  OS/Arch:          linux/arm
  Experimental:     false
 containerd:
  Version:          1.2.10
  GitCommit:        b34a5c8af56e510852c35414db4c1f4fa6172339
 runc:
  Version:          1.0.0-rc8+dev
  GitCommit:        3e425f80a8c931f88e6d94a8c831b9d5aa481657
 docker-init:
  Version:          0.18.0
  GitCommit:        fec3683
  ```