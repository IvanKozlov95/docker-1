from debian

RUN apt-get -y update && apt-get -y upgrade &&\
	apt-get install -y curl sudo build-essential git

RUN curl -sL https://deb.nodesource.com/setup_6.x -o nodesource_setup.sh && sudo bash nodesource_setup.sh
RUN apt-get install -y nodejs libpng-dev
RUN npm install -g bower

RUN git clone --depth 1 https://github.com/meanjs/mean.git

WORKDIR /mean

RUN npm install gulp
RUN bower install --allow-root
RUN npm install

CMD ["npm", "start"]