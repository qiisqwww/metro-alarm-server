ПОРЯДОК ЗАПУСКА:

При первом запуске сначала создается docker network с названием msa командой:
docker network create -d bridge msa

Затем поочередно запускаются docker-compose, причем:
1. СНАЧАЛА ЗАПУСКАЮТСЯ docker-compose СОДЕРЖАЩИЕ FASTAPI APP (между ними порядок не важен)
2. ПОТОМ ЗАПУСКАЕТСЯ docker-compose, СОДЕРЖАЩИЙ NGINX (лежит в этом каталоге)

Команда: docker-compose up --build