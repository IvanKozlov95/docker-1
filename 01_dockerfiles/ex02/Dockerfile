FROM ruby

RUN apt-get -y update && apt-get -y upgrade && \
	apt-get install -y nodejs && \
	gem install rails

ONBUILD COPY app/ /opt/

WORKDIR /opt/app

ONBUILD RUN bundle install