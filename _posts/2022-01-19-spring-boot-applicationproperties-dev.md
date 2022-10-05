---
title: "[spring-boot] application.properties-dev로 실행하기"
---

**application.properties란?**  
스프링부트가 자동으로 로딩되기 위한 규약들  
mysql 서버 정보, jpa 설정 등 작성함.

기본 설정 파일 application.properties을 개발 환경 용 설정파일 application-dev.properties 로 바꾸는 방법

### application.properties 에 active 설정

`spring.profiles.active=dev`

그리고 gradle에서 설치해야한다.  
`bootRun { String activeProfile = System.properties\['spring.profiles.active'\] systemProperty "spring.profiles.active", activeProfile }`  
제일 하단에 넣는게 오류가 안난다고한다.

### IntelliJ 실행 시 작동되는 configuration에 파일 설정하기

`-Dspring.profiles.active=dev`
