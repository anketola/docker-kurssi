FROM node:alpine

EXPOSE 5000

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apk del git && \
    adduser -D app

WORKDIR /frontend-example-docker

RUN npm install && \
    chown -R app /frontend-example-docker

USER app

ENV API_URL=http://localhost:8000

CMD ["npm", "start"]

