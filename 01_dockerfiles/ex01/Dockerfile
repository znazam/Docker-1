FROM debian

RUN apt update \
&& apt upgrade -y \
&& cd /tmp \
&& wget https://files.teamspeak-services.com/releases/server/3.6.1/teamspeak3-server_linux_amd64-3.6.1.tar.bz2 \
&& tar -xf teamspeak3-server_linux_amd64-3.6.1.tar.bz2 \
&& mkdir /opt/teamspeak-server \
&& mv teamspeak3-server_linux_amd64/* /opt/teamspeak-server \
&& cd /opt/teamspeak-server \
&& useradd -d /opt/teamspeak-server teamspeak-user \
&& chown -R teamspeak-user:teamspeak-user /opt/teamspeak-server \
&& su teamspeak-user \
&& touch .ts3server_license_accepted \
&& ./ts3server_startscript.sh start \
