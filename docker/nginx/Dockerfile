FROM nginx:latest

RUN apt update -y && \
	apt install -y iproute2 iputils-ping

CMD [ "nginx", "-g", "daemon off;" ]
