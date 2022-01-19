FROM frekele/ant:1.10.1-jdk8
LABEL authors="Rodolpho Guerreiro"
LABEL email="rodolpho.guerreiro@wasys.com.br"

RUN echo "deb http://packages.cloud.google.com/apt cloud-sdk-jessie main" | tee /etc/apt/sources.list.d/google-cloud-sdk.list
RUN curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y \
        google-cloud-sdk \
        git
