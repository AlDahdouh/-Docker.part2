FROM ubuntu:latest
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install nodejs git-core -y
RUN git clone https://github.com/docker-hy/backend-example-docker.git
WORKDIR /backend-example-docker
ENV FRONT_URL=http://localhost/
RUN npm install
EXPOSE 8000
ENTRYPOINT ["npm"]
CMD ["start"]
