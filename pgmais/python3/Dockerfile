FROM python:alpine3.6

MAINTAINER Rodolpho Guerreiro

COPY . /opt/radar-email

WORKDIR /opt/radar-email

RUN apk add --no-cache mariadb-dev mysql-client gcc libffi libffi-dev build-base python3 git openssh && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade pip setuptools && \
    if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    if [[ ! -e /usr/bin/python ]]; then ln -sf /usr/bin/python3 /usr/bin/python; fi && \
    rm -r /root/.cache

#ARG SSH_PRIVATE_KEY
#RUN mkdir /root/.ssh/
#RUN echo "${SSH_PRIVATE_KEY}" > /root/.ssh/id_rsa
#RUN touch /root/.ssh/known_hosts
#RUN ssh-keyscan git.pgd.to >> /root/.ssh/known_hosts

#RUN git clone https://Guerreiro:96347009@git.pgd.to/pg/pg_miscellaneous.git \
    #cd pg_miscellaneous \
    #&& pip install mysqlclient \
    #&& python3 setup.py install

CMD python3 radar.py
