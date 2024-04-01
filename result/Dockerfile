FROM node:20-alpine

RUN mkdir /result_app

WORKDIR /result_app

COPY . /result_app

RUN npm install

EXPOSE 80

CMD [ "node", "server.js"]
