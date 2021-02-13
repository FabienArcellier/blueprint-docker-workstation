FROM tsl0922/ttyd

ENV DEBIAN_FRONTEND=noninteractive

# Common utilities

RUN apt-get update && \
    apt-get install -y apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common \
    wget

# The installation of docker allow you to use docker from inside the webconsole
# it makes it easier to have an environment ready to use inside the
# docker-compose environment
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" &&\
    apt-get install -y docker-ce docker-ce-cli containerd.io

# Common utility

RUN apt-get install -y postgresql osm2pgsql
