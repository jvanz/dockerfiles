FROM ruby:2.3-jessie

RUN apt-get update -y
RUN apt-get install -y firefox-esr

RUN useradd -m user
USER user
WORKDIR /home/user

RUN gem install opencode_theme

USER user
ENTRYPOINT bash
