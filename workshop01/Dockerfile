FROM node:latest

LABEL name="myapp"

ENV DB_HOST=mydb DB_PORT=3306
ENV APP_PORT=3000 APP_DIR=/app

RUN mkdir $APP_DIR

WORKDIR $APP_DIR

ADD main.js .
ADD package-lock.json .
ADD package.json . 
ADD config config
ADD public public
ADD views views

RUN npm install

EXPOSE $APP_PORT

ENTRYPOINT [ "node", "main.js" ]