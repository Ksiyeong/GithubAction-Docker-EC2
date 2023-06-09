# GithubAction-Docker-EC2

**깃허브 액션 + 도커 + EC2(혹은 이외의 컴퓨팅서비스) + 스프링부트 CI/CD 구축 프로젝트입니다.**

***환경***
- Java 17 
- Spring Boot 3.1.0 
- gradle 
- 로컬 PC : M2 Mac os 
- EC2 : Ubuntu 22.04 프리티어

***사전 준비***
- 깃허브 계정 및 레포지토리
- 도커허브 계정
- ec2(또는 그 외의 컴퓨팅 서비스)
- 깃허브 시크릿 등록
  - DOCKERHUB_USERNAME
  - DOCKERHUB_PASSWORD

***동작 흐름***
1. 깃허브 main 브랜치에 push & pull_request 발생
2. 깃허브 액션 감지 및 동작 수행
3. Spring Boot 프로젝트 빌드 -> app.jar
4. app.jar 도커 이미지로 빌드
5. 도커 허브에 이미지 푸시
6. ec2 도커 이미지 풀
7. 도커 이미지 실행

참조 블로그<br>
https://e-room.tistory.com/170 <br>
https://e-room.tistory.com/171
