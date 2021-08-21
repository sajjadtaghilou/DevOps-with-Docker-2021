FROM ubuntu:20.10

EXPOSE 5000
WORKDIR /nodejs

RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v

COPY example-frontend .
RUN npm install

RUN npm run build
RUN npm install -g serve

ENTRYPOINT serve -s -n -l 5000 build
