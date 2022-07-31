FROM golang:1.18

RUN apt update -y && \
	apt install -y tcpdump iproute2 iputils-ping systemd iperf git make

RUN git clone https://github.com/terassyi/grp.git && \
	cd grp && \
	make && \
	mv ./grpd /usr/local/bin && \
	mv ./grp /usr/local/bin

COPY config.yml config.yml
CMD [ "bash" ]

