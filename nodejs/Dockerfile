FROM debian
MAINTAINER Jorge Nery jorge.nery@ottrans.com.br

LABEL NodeJS WebServer
VOLUME /apps:/home/docker/apps
VOLUME /basededados:/home/docker/basededados
WORKDIR /work-dir
ADD deploit-docker.sh deploit-docker.sh
COPY /webserver/ /webserver/
RUN /apps/deploit-docker.sh && apt-get clean
CMD ["sh","-c","echo","$HOME"]
ENTRYPOINT ["/usr/bin/apache2ctl","-D" "FOREGROUD"]
EXPOSE 80
EXPOSE 3000
USER ottrans
