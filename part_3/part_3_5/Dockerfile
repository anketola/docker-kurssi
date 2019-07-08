FROM node:alpine as build-stage

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apk del git

WORKDIR /frontend-example-docker

RUN npm install && \
     npm run build

FROM node:slim

EXPOSE 5000

COPY --from=build-stage /frontend-example-docker/dist/ /app/dist

WORKDIR /app/dist

RUN npm install -g serve

ENV API_URL=http://localhost:8000

CMD serve -s -l 5000
