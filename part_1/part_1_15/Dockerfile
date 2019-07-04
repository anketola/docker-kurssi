FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/anketola/flask-docker.git

EXPOSE 5000

WORKDIR /flask-docker
RUN apt-get install python3 -y
RUN apt-get install python3-venv -y
RUN python3 -m venv venv
RUN /bin/bash -c "source venv/bin/activate"
RUN apt install python3-pip -y
RUN apt install python3-dev -y
RUN pip3 install -r requirements.txt

CMD python3 run.py

