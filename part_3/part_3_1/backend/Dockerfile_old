FROM ubuntu:16.04

EXPOSE 8000

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN apt install -y git
RUN git clone https://github.com/docker-hy/backend-example-docker.git
WORKDIR /backend-example-docker
RUN npm install

ENV FRONT_URL="http://localhost:5000"

CMD ["npm", "start"]

