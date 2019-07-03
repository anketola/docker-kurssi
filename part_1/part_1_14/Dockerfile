FROM ruby:latest

EXPOSE 3000

WORKDIR /railsproject

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

COPY ./rails-example-project .
RUN bundle install
RUN rails db:migrate

CMD rails s

