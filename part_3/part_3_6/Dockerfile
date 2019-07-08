FROM python:3.7.3-alpine3.10

EXPOSE 5000

RUN apk add --no-cache git && \
    git clone https://github.com/anketola/flask-docker.git && \
    apk del git && \
    adduser -D app

WORKDIR /flask-docker

RUN pip install --upgrade pip && \
    pip install virtualenv && \
    virtualenv /venv && \
    pip3 install -r requirements.txt && \
    chown -R app /flask-docker

USER app

CMD python3 run.py

