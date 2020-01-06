# Docker Week2
## Docker Image File 만들기
### 1. Dockerfile을 만들 폴더에 이동
```bash
$ cd /path/to/work
```  

### 2. Dockerfile 생성 및 편집
```bash
$ vi Dockerfile
```
혹은
```bash
$ touch Dockerfile // 파일 생성 후
$ vi Dockerfile // Dockerfile 편집
```

## Docker Image에 들어가는 Option들 (추후 수정 예정)

### FROM
  - [원문번역]: 새로운 Build stage를 초기화하고 차후 단계를 위한 Base Image를 설정하는 것이다.
  - 새로운 Image를 만들기 위한 Base Image를 설정하는 단계이다.
  - FROM은 한 Dockerfile에서 여러 번 실행 가능하며 FROM이 실행되는 시점에는 \
  이전 단계의 명령들은 사라지게 된다. (? 이건 번역 다시 해야할듯)
  - Format 
    - FROM \<image> [AS \<name>]
    - FROM \<image> [:\<tag>] [AS \<name>]
    - FROM \<image> [@\<digest>] [AS \<name>]

### MAINTAINER
  - 추가 예정

### RUN
  - 현재 Image의 맨 위의 새로운 layer에 입력되어있는 명령어를 실행 후 결과를 저장한다.
  - 결과가 저장된 Image는 Dockerfile에서의 다음 명령어를 실행할 때 사용된다. 
  - Format 
    - RUN \<command> 
      - ex) RUN apt-get install npm
    - RUN ["executable", "param1", "param2"]
      - ex) RUN ["apt-get", "install", "npm"]

### CMD
  - Build된 Image가 Container로 올려질 (run 될) 시 실행되는 기본(default) 명령어. [ENTRYPOINT와 동일]
  - CMD는 docker run 실행 시 명령어를 주지 않았을 때 사용할 default 명령을 설정한다.
  - CMD 명령어는 한 Dockerfile에 여러번 정의 될 수 있으나, \
    맨 마지막에 정의된 CMD 명령어만 실행된다.
  - Format 
    - CMD command param1 param2
    - CMD ["executable","param1","param2"] 
    - CMD ["param1","param2"] (ENTRYPOINT를 실행하고 그 명령의 인자값들)
### ENTRYPOINT
  - Build된 Image가 Container로 올려질 시 실행되는 명령어.
  - Format (RUN 명령어와 동일)
    - ENTRYPOINT command param1 param2
    - ENTRYPOINT ["executable", "param1", "param2"]
      - ENTRYPOINT 명령어에 executable만 있고 CMD에서 Parameter만 넘길 수 있다.

### ENTRYPOINT와 CMD를 어떤 차이가 있는가는 다음 사이트를 참고하자.
  - (나중에 정리 예정)
  - https://bluese05.tistory.com/77
  - https://blog.leocat.kr/notes/2017/01/08/docker-run-vs-cmd-vs-entrypoint

### VOLUME
  - VOLUME은 디렉터리의 내용을 컨테이너에 저장하지 않고 호스트에 저장하도록 설정하는 것.
  - 단, VOLUME으로는 호스트의 특정 디렉터리와 연결할 수는 없음.
  - Format
    - VOLUME \<directory>
    - VOLUME ["directory 1", "directory 2"]

### ADD
  - Image에 Host에 있는 파일을 올리는 것.
  - The ADD instruction copies new files, directories or remote file URLs from \<src> and adds them to the filesystem of the image at the path \<dest>.
### COPY
  - Image에 Host에 있는 파일을 올리는 것.
  - The COPY instruction copies new files or directories from \<src> and adds them to the filesystem of the container at the path
### EXPOSE
### USER
### WORKDIR
### ARG
### ONBUILD
### STOPSIGNAL
### HEALTHCHECK
### SHELL