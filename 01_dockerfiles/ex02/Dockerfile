FROM ruby

RUN apt-get -y updare && apt-get -y upgrade && \
	get install rails

ONBUILD COPY app/ /opt/

WORKDIR /opt/app

ONBUILD RUN bundle install