## Как это запустить?

### При помощи docker-compose.yml:

При первом запуске сначала создается docker network с названием msa командой:
docker network create -d bridge msa

Затем поочередно запускаются docker-compose, причем:
1. СНАЧАЛА ЗАПУСКАЮТСЯ docker-compose СОДЕРЖАЩИЕ BACKEND ПРИЛОЖЕНИЕ (каждый docker-compose.yml внутри директорий auth и map)
2. ПОТОМ ЗАПУСКАЕТСЯ docker-compose, СОДЕРЖАЩИЙ NGINX (лежит в корне)

Команда: docker-compose up --build
