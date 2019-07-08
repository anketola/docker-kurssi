FROM ubuntu:16.04

EXPOSE 8000

RUN apt-get update && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt install -y nodejs && \
    apt install -y git && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app


WORKDIR /backend-example-docker

RUN npm install && \
    chown -R app /backend-example-docker

USER app

ENV FRONT_URL="http://localhost:5000"

CMD ["npm", "start"]

