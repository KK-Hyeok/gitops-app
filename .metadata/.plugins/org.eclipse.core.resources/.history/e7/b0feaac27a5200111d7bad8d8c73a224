FROM openjdk:17-jdk-slim

# 2. 컨테이너 내부에서 작업할 폴더 경로를 /app으로 지정합니다.
WORKDIR /app

# 3. GitHub Actions가 빌드해준 실행 파일(target 폴더 안의 .jar)을 컨테이너 안으로 복사합니다.
COPY target/*.jar app.jar

# 4. 이 도커 컨테이너가 켜질 때, 자동으로 자바 앱이 실행되도록 명령어를 지정합니다.
ENTRYPOINT ["java", "-jar", "app.jar"]