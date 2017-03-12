# Alerte Blanche NGINX Front

NGINX web server fronting the traffic to the different API servers.

## Installation

```bash
sudo -s
apt-get install -y nginx
wget -O /etc/nginx/conf.d/alerte-blanche.conf https://raw.githubusercontent.com/HackQC2017-BoltTeam/alerte-blanche-front/master/conf/alerte-blanche.conf
rm /etc/nginx/sites-enabled/default
nginx start
exit
```

## Usage

This table describes where the incoming routes will redirect to.
Ti is expected that the services be listening at the given port.

| Route           | Service             | Port   |
| --------------- | ------------------- | ------ |
| `/api`          | Alerte Blanche API  | `8080` |
| `/platonix`     | Platonix            | `8081` |
| `/yeoulparking` | YeoulParking        | `8082` |
