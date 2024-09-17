# kvwmap manuell installieren
## Voraussetzungen
 * Packete die im Standard installiert werden
   ```
sudo apt update && sudo apt install -y \
apt-utils \
lshw \
git \
jq \
sendmail \
tree \
unzip \
wget \
nano \
htop \
openssl \
gosu \
curl \
fish \
ca-certificates \
gnupg \
zstd \
docker.io \
docker-compose \
apparmor \
python3 \
python3-dev \
python3-jinja2 \
python3-psutil \
python3-setuptools \
python3-pip \
lm-sensors \
libpam-pwquality \
zabbix-agent \
borgbackup
    ```
 * Uid: (17000/gisadmin)   Gid: ( 1700/gisadmin)
 * ```git clone https://github.com/pkorduan/kvwmap-server.git```
 * ```kvwmap-server/bin/dcm``` ist im $PATH  ```ln -s /home/gisadmin/kvwmap-server/bin/dcm /usr/bin/dcm```
 * ```kvwmap-server/bin/setup-basis-kvwmap.sh``` wird mit Konfigurationsdatei ```setup.conf``` aufgerufen, diese anpassen
   ```
   OS_USER=gisadmin
   TEST_CERT=n
   DOMAIN=kvwmapDomain.de
   DEFAULTMAIL=myMail@kvwmapDomain.de
   SUBNET_KVWMAP_PROD=172.0.10.0/24
    ```
 * Script starten ```./setup-basis-kvwmap.sh -c setup.conf```
