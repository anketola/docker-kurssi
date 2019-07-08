FROM node:alpine

EXPOSE 8000

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apk del git && \    
    adduser -D app

WORKDIR /backend-example-docker

RUN npm install && \
    chown -R app /backend-example-docker

USER app

ENV FRONT_URL="http://localhost:5000"

CMD ["npm", "start"]

