FROM node:latest
ENV DB_HOST=mydb DB_USER=root DB_PASSWORD=changeit DB_PORT=3306
ENV APP_DIR=/app APP_PORT=3000

WORKDIR ${APP_DIR}

WORKDIR ${APP_DIR}


ADD config config
ADD public public
ADD views views

ADD main.js .
ADD package.json .
RUN npm install


EXPOSE ${APP_PORT}

ENTRYPOINT [ “node”, “main.js” ]
CMD [ “{$APP_PORT}” ]
