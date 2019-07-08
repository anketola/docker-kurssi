FROM ubuntu:16.04

EXPOSE 5000

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    apt install -y git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app

WORKDIR /frontend-example-docker

RUN npm install && \ 
    chown -R app /frontend-example-docker

USER app

ENV API_URL=http://localhost:8000

CMD ["npm", "start"]

