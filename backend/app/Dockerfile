FROM ruby:3.2

# System Settings
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

# Application Settings
WORKDIR /app

COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock
RUN bundle install
COPY ./backend/app /app
