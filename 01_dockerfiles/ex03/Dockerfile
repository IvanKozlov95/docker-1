FROM debian

RUN apt-get -y update && apt-get -y upgrade && \
	apt-get install -y git && \
	apt-get install -y golang-go sqlite
	
RUN export GOPATH=$HOME/go && \
	mkdir -p $GOPATH/src/github.com/gogits && \
	cd $GOPATH/src/github.com/gogits && \
	git clone -b develop --depth=1 https://github.com/gogits/gogs && \
	cd gogs && \
	go build -tags "sqlite"

WORKDIR /root/go/src/github.com/gogits/gogs

ENV USER=root

EXPOSE 3000

CMD ["./gogs", "web"]