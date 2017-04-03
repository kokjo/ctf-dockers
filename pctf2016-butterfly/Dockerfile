FROM debian
RUN apt-get update -qy
RUN apt-get install -qy socat

RUN useradd butterfly
RUN mkdir /home/butterfly
WORKDIR /home/butterfly

COPY butterfly_33e86bcc2f0a21d57970dc6907867bed butterfly
COPY run .
RUN chmod 555 *

EXPOSE 1337

CMD ["/home/butterfly/run", "1337", "butterfly", "/home/butterfly/butterfly"]
