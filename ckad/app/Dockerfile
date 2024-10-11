FROM node:lts-alpine3.18

COPY . /src
WORKDIR /src

RUN npm install
EXPOSE 8080

ENTRYPOINT ["node", "./app.js"]
