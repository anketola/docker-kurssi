FROM ubuntu:16.04

WORKDIR /curler

RUN apt-get update && apt-get install -y curl
COPY script.sh /curler/script.sh

RUN chmod +x /curler/script.sh

CMD ["/curler/script.sh"]
