FROM ruby:2.3.1

RUN mkdir -p /src/app
WORKDIR /src/app

COPY Gemfile /src/app/
COPY Gemfile.lock /src/app/
RUN apt-get update && apt-get -y install netcat build-essential libpq-dev nodejs
RUN bundle install

COPY . /src/app
