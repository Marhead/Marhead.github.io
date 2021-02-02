## 프로젝트 생성

- Java 11
- IDE: IntelliJ



- 프로젝트 선택
  - Project: Gradle Project
  - Spring Boot: 2.3.x
  - Language: Java
  - Packaging: Jar
  - Java: 11
- Project Metadata
  - groupid: hello : 그룹명, 단체명
  - artifactld: hello-spring : 빌드 결과
- Dependencies: Spring Web, Thymeleaf(템플릿 엔진, 다양하게 존재)



Maven -> Gradle : 요즘 추제, 레거시 프로젝트가 아닌 이상 그래들 많이 사용



Boot 프로젝트 빌드시 나오는 폴더

- .gradle :
- .idea : IntelliJ 설정 파일
- gradle
- src
  - main
    - java : 실제 패키지
    - resources : xml, html등의 코드를 제외한 설정파일들
  - test : 테스트 코드들(요즘 개발 트렌드에서 테스트케이스가 중요해짐)

- build.gradle
  - junit : 기본 첨가
  - mavenCentral 에서 다운, repository에서 추가 가능
- apache-tomcat : spring 구동시 자동 실행 되는 서버 구동기

## 라이브러리 살펴보기

maven-gradle 등의 빌드 툴들은 의존관계를 관리해준다.

log출력을 하는 이유 : 에러등을 모아서 압축적으로 보기 좋음

**로그(Log)란 무엇인가?**

로그(log)는 소프트웨어 혹은 하드웨어 서비스들이 지속적으로 만들어내는 시스템 이벤트(event)의 기록입니다. IT 서비스는 대표적으로 다음과 같은 서비스에서 로그가 발생합니다.

● 네트워크

● 서버

● 컨테이너

● 클라우드 인프라

● 애플리케이션

● 메시지 버스(카프카..)

● 로드밸런서

...

좀 더 구체적인 예를 찾아볼까요?

● Docker에서 발생한 로그

● 운영체제 로그

● 애플리케이션 에러 로그

● 애플리케이션 코드 추적 로그

● 솔루션 로그(아파치, 오라클, MySQL, 리눅스, VMWare...)

● AWS VPC Flow 로그

● 클러스터 성능 지표 

● 악의적 IP 혹은 사용자의 접근 기록

● 클라우드 인프라 로그

**로그의 형태**

로그는 정해진 규칙에 의거하여 Key-Value 형태 혹은 정해진 Key 순서에 맞게 Value 값으로 표현하는 것이 일반적입니다. 이런 패턴을 통해 분석과 모니터링 정보를 제공합니다.

e.g.) 로그에 찍힌 값의 순서

타임스탬프 / 호스트 이름 / 프로세스 타입 / 애플리케이션 / 실행 내용 / TCP 상태/...etc



logback - 성능 구현체

slf4j - 로그 구현 인터페이스



### test

junit 5버전. 상용



**스프링 부트 라이브러리**

- spring-boot-starter-web
  - spring-boot-starter-tomcat : 톰캣(웹서버)
  - spring-webmvc: 스프링 웹 MVC
- spring-boot-starter-thymeleaf: 타임리프 템플릿 엔진(View)
- spring-boot-starter(공통): 스프링 부트 + 스프링 코어 + 로깅
  - spring-boot
    - spring-core
  - spring-boot-starter-logging
    - logback, slf4j

**테스트 라이브러리**

- spring-boot-starter-test
  - junit: 테스트 프레임워크
  - mockito: 목 라이브러리
  - assertj: 테스트 코드를 좀 더 편하게 작성하게 도와주는 라이브러리
  - spring-test: 스프링 통합 테스트 지원

% 컨트롤러가 우선순위를 가짐

