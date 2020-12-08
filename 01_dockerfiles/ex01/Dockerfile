FROM debian

FROM debian
ENV TS3SERVER_LICENSE=accept
RUN apt update && apt upgrade -y
RUN apt-get install wget -y && apt-get install bzip2
RUN apt install nano
RUN wget http://dl.4players.de/ts/releases/3.13.2/teamspeak3-server_linux_amd64-3.13.2.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.13.2.tar.bz2
RUN rm teamspeak3-server_linux_amd64-3.13.2.tar.bz2
ENTRYPOINT cd teamspeak3-server_linux_amd64 && sh ts3server_minimal_runscript.sh
EXPOSE 9987/UDP 30033 10011

# docker build -t "ex01" .
# docker run -d  -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
