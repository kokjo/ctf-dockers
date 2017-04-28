FROM 32bit/debian:jessie

RUN apt-get update -qy
RUN apt-get install -qy socat

ENV USER treehugger
ENV PORT 1337

RUN useradd $USER
RUN mkdir /home/$USER
WORKDIR /home/$USER

COPY treehugger .
COPY run .
RUN chmod 555 *

EXPOSE $PORT

ENTRYPOINT ["./run", "./treehugger"]
