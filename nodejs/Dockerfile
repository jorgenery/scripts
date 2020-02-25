FROM debian

# Set one or more individual labels
LABEL com.example.version="0.0.1-beta"
LABEL vendor1="Jorge Nery"
LABEL com.example.release-date="2020-02-25"
LABEL com.example.version.is-production="1.0"

VOLUME /apps:/home/docker/apps
VOLUME /basededados:/home/docker/basededados
WORKDIR /work-dir
COPY deploit-docker.sh .
COPY /webserver/ /webserver/
RUN apt-get update && apt-get install -y nodejs npm && apt-get clean && npm install
CMD [ "node", "server.js" ]
ENTRYPOINT ["/usr/bin/apache2ctl","-D" "FOREGROUD"]
EXPOSE 80
EXPOSE 3000
USER ottrans