FROM ubuntu:latest
RUN apt-get update && apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash 
RUN apt-get install nodejs git-core -y
RUN git clone https://github.com/docker-hy/frontend-example-docker.git
WORKDIR /frontend-example-docker
ENV API_URL=http://localhost/api/
RUN npm install
EXPOSE 5000
ENTRYPOINT ["npm"]
CMD ["start"]
