# 1. node 설치
# 우분투라는 이미지를 쓸 것임
FROM    ubuntu:22.04 
RUN     apt-get update 
# Node.js와 npm 설치 
RUN     DEBIAN_FRONTEND=noninteractive apt-get install -y curl 
RUN     curl -sL https://deb.nodesource.com/setup_16.x | bash -
RUN     DEBIAN_FRONTEND=noninteractive apt-get install -y nodejs
# 위 명령어 들은 FROM node:12로 축약이 가능함
# node:12 는 이미 누군가 빈 리눅스에 node.js를 설치하여 배포한 것 



# 2. 소스 복사
COPY    . /usr/src/app

# 3. Nodejs 패키지 설치
WORKDIR /usr/src/app
RUN     npm install

# 4. WEB 서버 실행 (Listen 포트 정의)
EXPOSE 3000
CMD    node app.js