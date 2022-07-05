# Terraform-on-MultiCloud

## 테라폼(Terraform) 이란?

<img src="https://user-images.githubusercontent.com/73388615/177294573-01fb37d0-cc33-41ec-a4a5-713b4057c34c.png" width="200" height="200"/>

테라폼(Terraform)은 프로그램 코드를 통해 인프라 서버를 구축/운영 할 수 있게 해주는 오픈 소스 Infrastructure as Code, IaC 도구(소프트웨어)이다. 
오픈소스로 개발 중인 클라우드 인프라스트럭처 자동화를 지향하는 코드로서의 Infrastructure as Code, IaC 도구이다.
테라폼은 프로그램 코드를 통해 인프라 서버를 구축/운영 할 수 있게 해주는 오픈 소스 소프트웨어 입니다.



테라폼을 사용하면 AWS든, GCP든, NCP든 테라폼이 지원하는 클라우드 플랫폼이라면, 클라우드 인프라 환경을 코드로서 정의해 사용함으로써 동일한 인프라를 재현할 수 있다.



## 📘 수행한 내용

**Infra Provisioning on MultiCloud using Terraform**   
- 테라폼으로 인프라(서버(인스턴스), 네트워크 등)을 생성하고 생성된 서버 IP를 사용자에게 출력되도록 하여 원격으로 서버 접속이 가능하도록 해보았다.



## 활용했던 구성 요소 및 명령어

### 1) Terraform 구성 요소
- provider
  - 테라폼과 외부 서비스를 연결해주는 기능으로, 이를 통해 생성할 인프라의 종류를 정할 수 있다.
- resource 
  - 테라폼으로 실제 생성할 인프라 자원을 의미한다.
- state 
  - 테라폼을 통해 생성한 자원의 상태를 의미한다. 현재 인프라의 상태를 의미하는 것은 아니다.
- data
  -프로바이더에서 제공하는 리소스 정보를 가져와서 테라폼에서 사용할 수 있는 형태로 매핑시킬 수 있다. 즉, 이미 클라우드에 존재하는 리소스를 가져오는 것이다. 


### 2) Terraform 명령어
- init
  - Terraform 구성 파일이 포함된 작업 디렉토리를 초기화하는 데 사용됨.
- plan
  - 정의한 코드가 어떤 인프라를 만들게 되는지 미리 예측 결과를 보여줌. 단, plan을 한 내용에 에러가 없다고 하더라도, 실제 적용되었을 때는 에러가 발생할 수 있다.
- apply
  - 실제로 인프라를 배포하기 위한 명령어. apply를 완료하면, 클라우드에 실제로 해당 인프라가 생성되고 작업 결과가 backend의 .tfstate 파일과 local의 .terraform에 저장된다.
- destory 
  - 생성된 리소드들을 state 파일 기준으로 모두 삭제. 
