# Devit (Python)

> 개발자 구인 구직 서비스 <br/>

 

 

<br/>



## 1. 제작 기간 & 참여 인원

* 2022.05.06 ~ 2022.05.13

* 3명 : [이다혜](https://github.com/ekgpgdi), [김지호](https://github.com/kimziaco?tab=repositories), [김대희](https://github.com/eet43)

<br/>

 

## 2. 사용 기술 

<b>```Back-end```<b/>
* Python 3.8 

* Flask

* boto3 <br/>

* requests <br/>

* pymongo <br/>

 

<b>```Front-end```<b/>

 

- HTML

- Bootstrap

- JavaScript

 
<br/>


## 3. Data Model Design - Embedded Data Models

![스크린샷 2022-08-23 오전 11 39 35](https://user-images.githubusercontent.com/84092014/186057233-0f5aa9be-05c3-4e91-b7d1-1aa476b2a02f.png)
![스크린샷 2022-08-23 오전 11 39 46](https://user-images.githubusercontent.com/84092014/186057253-6872906e-ce64-415d-b7f4-75ddd35b8501.png)

 
<br/>
 

## 4. 아키텍처

<p align="center">

 <img width="786" alt="스크린샷 2022-08-22 오후 5 07 26" src="https://user-images.githubusercontent.com/84092014/185902896-eb7667e8-1835-4d86-a441-e09a7aff12af.png">

  </p>

 <br/>

## 5. 핵심 기능
![image (2)](https://user-images.githubusercontent.com/84092014/186078329-650da812-69b0-4d6c-a674-0b4c00d52044.png)
<br/>

## 6. 핵심 트러블 슈팅 
1. EC2 AMI ubuntu 버전 차이로 인한 python 버전 불일치 문제 
> EC2 AMI의 ubuntu 버전을 18.04 LTS 로 지정하여 python version 이 3.6으로 설치가 되었고 그로 인해 프로젝트 python 3.8 버전과 일치하지 않아 requirements.txt에 작성한 패키지 버전들과 호환 오류 발생
> 처음에는 pip 로  python 3.6에서 사용 가능한 패키지 버전들로 다운그레이드하여 설치함으로써 불필요한 작업이 발생
> 이후 ubuntu 버전 차이라는 것을 인지하고 ubuntu 버전을 20.04 LTS 로 변경하여 해결

2. 추가 작업 없는 배포를 고민 
> Local 환경에서 작업하던 프로젝트를 어떻게 추가 작업없이 CI/CD 의 장점을 이용하여 EC2에 배포할 수 있을까 라는 고민을 시작
> 환경 변수 분리를 위해 Prod 환경과 Local 환경의 환경 변수들을 config 파일로 분리
