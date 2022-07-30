FROM rust:latest

RUN apt update -y && \
	apt install -y build-essential git

RUN git clone https://github.com/terassyi/rushttp.git && \
	cd rushttp && \
	cargo build --release && \
	mkdir -p /etc/rushttp/static/assets/html && \
	cp src/static/assets/html/* /etc/rushttp/static/assets/html/ && \
	mv target/release/rushttp /usr/local/bin


CMD [ "rushttp", "9999" ]
