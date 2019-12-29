# AWS Week1
## 세부 설치 과정
[설치과정](https://victorydntmd.tistory.com/61)  
다만 AWS의 사양과 latancy 때문에 RaspberryPi로 서버를 대체  
후에 개발과정 중 `안정적인 서비스를 제공`하기 위하여 AWS에 Docker를 올릴 예정  
`Main Server Domain`
```
ec2-13-59-234-130.us-east-2.compute.amazonaws.com
```
`Test Server Domain`
```
ec2-18-223-190-20.us-east-2.compute.amazonaws.com
```
Pem key는 Slack에 각각 저장되어 있음

`Raspberry docker -> Test`
```
222.232.17.133 -p 8827
```
계정 생성 및 추가 api&lib 설치는 [이종빈](https://github.com/EmptyPaper)에게 문의
