FROM debian
RUN apt-get update -qy
RUN apt-get install -qy libc6-i386

RUN useradd starwars
RUN mkdir /home/starwars
WORKDIR /home/starwars

COPY starwars starwars
RUN chmod 555 *

USER starwars

EXPOSE 1337

CMD ["/home/starwars/starwars", "1337"]
