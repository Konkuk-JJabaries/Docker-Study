# Docker Command

## 1. docker images
  - docker에 저장되어 있는 image들을 출력하는 명령어
  - ### Format
``` bash
    $ docker images [OPTIONS] [REPOSITORY[:TAG]]
```
  - ### Options
    | Name , shorthand | Default | Description |
    |---|:---:|:---|
    | `-all , -a` || Show all images </br> (default hides intermediate images)|
    | `--digests` || Show digests |
    | `--filter , -f` | | Filter output based on conditions provided |
    | `--format` || Pretty-print images using a Go template |
    | `--no-trunc` ||Don’t truncate output|
    | `--quiet , -q` ||Only show numeric IDs|


## 2. docker build
  - Dockerfile을 이용하여 image를 build 하는 명령어
  - ### 주로 사용하는 명령
``` bash
    $ docker build --tag <imagename>:<tag>
```

## 3. docker run
  - docker에 저장된 image를 실행하는 것(container화 하는 것)
  - ### 주로 사용하는 명령
``` bash
    $ docker run -it -d -p 80:80 <image>:<tag>
```
## 4. docker ps
  - 실행 중인 container들 출력
  - ### 주로 사용하는 명령
``` bash
    $ docker ps -al
    $ docker ps -ef
```
## 5. docker exec
  - 실행 중인 container에 명령을 전송
  - ### 주로 사용하는 명령
``` bash
    $ docker exec -it <containerID> /bin/bash
```
## 6. docker inspect
  - 추후 작성
## 7. docker stop
  - 실행 중인 container를 멈춤
  - ### 주로 사용하는 명령
``` bash
    $ docker stop <containerID>
```

## 8. docker rm
  - 정지 된 container의 자원을 해제
  - ### 주로 사용하는 명령
``` bash
    $ docker rm <stoppedContainerID>
    $ docker rm -f <stoppedContainerID> # Container 강제 종료
```

## 9. docker rmi
  - 저장되어져 있는 image를 삭제
  - ### 주로 사용하는 명령
``` bash
    $ docker rmi <imageID>
    $ docker rmi -f <imageID> # Image 강제 삭제
```
