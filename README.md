# compose-dokuwiki
Fichier docker compose décrivant le TP Dokuwiki

```
docker network create -d bridge Dokuwiki
wget https://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz
tar xzf dokuwiki-stable.tgz
sudo chown -R 82:82 dokuwiki-2020-07-29
git clone https://github.com/0xd6cb6d73/compose-dokuwiki.git
cd compose-dokuwiki
docker compose up -d
```
