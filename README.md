# 🎬 무종이의 영화 리뷰 Project

## 📛 프로젝트의 명칭 및 로고

## 📝 프로젝트의 간단한 설명
  영화 리뷰 웹 사이트입니다.

## 💻 필요한 소프트웨어 및 하드웨어 요구 사항
- Java 17
- MySQL 8 이상
- Git
- IntelliJ (또는 자바 IDE)
- 터미널 (Windows CMD, Mac Terminal 등)

### 🛠 설치 및 설정 방법

1. 아래의 두 저장소를 각각 클론합니다.

   ```bash
   git clone https://github.com/openSourceTeam-8/front-end.git
   git clone https://github.com/openSourceTeam-8/backend.git
   ```
2. Java 17 버전을 설치하고 기본(Java default) 버전으로 설정합니다.

3. MySQL을 설치하고 실행합니다.

## ▶ 사용 방법 및 예시


1. **백엔드 프로젝트 열기**  
   백엔드 코드를 자바 개발 환경(예: IntelliJ)에서 엽니다.

2. **프론트엔드 코드 삽입**  
   `src/main/resources/templates` 경로에 앞서 클론한 프론트엔드 코드를 복사해 넣습니다.

3. **application.yml 파일 생성**  
   `src/main/resources` 경로에 `application.yml` 파일을 생성하고 아래 내용을 작성합니다.

   ```yaml
   spring:
     datasource:
       driver-class-name: com.mysql.cj.jdbc.Driver
       url: jdbc:mysql://localhost:3306/opensource?allowPublicKeyRetrieval=true&useSSL=false&serverTimezone=Asia/Seoul
       username: root  # 본인의 DB 계정명으로 수정
       password: 0000  # 본인의 DB 비밀번호로 수정

     jpa:
       database: mysql
       database-platform: org.hibernate.dialect.MySQL8Dialect
       show-sql: true
       hibernate:
         ddl-auto: update
       properties:
         hibernate:
           format_sql: true

     servlet:
       multipart:
         max-file-size: 50MB
         max-request-size: 50MB

   logging:
     level:
       your:
         database:
           package: debug
       org.hibernate.SQL: debug
       org.hibernate.type: trace

   springdoc:
     api-docs:
       enabled: true
     swagger-ui:
       enabled: true
       tagsSorter: alpha
       operations-sorter: alpha
       display-request-duration: true

   jwt:
     secret: cb65f1793aa189bd0d0b682634dba6ad7365946a05cac5150b3671c3a761c505
   ```

4. **빌드 및 실행 (IntelliJ 기준)**  
   `bootJar`를 실행하여 `.jar` 파일을 생성합니다.

5. **jar 실행**  
   `build/libs` 디렉토리로 이동 후 아래 명령어를 실행합니다:

   ```bash
   java -jar opensource-server-0.0.1-SNAPSHOT.jar
   ```

   > 💡 파일명을 직접 변경했다면, 해당 변경한 파일명으로 실행해주세요.

## 🧪 테스트 방법

## 🤝 기여 방법

## 📄 라이선스 정보
  이 프로젝트는 AGPL 라이선스 하에 제공됩니다.

## 👨‍💻  저자 및 연락처 정보
  김동혁
  
  김현아
  
  이채원
  
  황재희

## 📚 참고 문헌
