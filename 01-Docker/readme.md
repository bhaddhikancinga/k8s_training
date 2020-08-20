docker run -p 3002:80  nginx

docker build -t demo .

docker run -it demo  /bin/sh

docker run -it -p 8010:8000 demo  /bin/sh

docker run  -p 8010:8000 demo

docker run  -p 8011:8000 -e type=development demo

docker container ls

docker container rm --force 4a0e80c868ce 4df36a76723b

docker system prune --all

docker run  -p 8010:8000 -e type=development -it -v $(pwd):/app demo /bin/sh

docker exec -it b792819e8869 /bin/sh

docker-compose up -d

docker-compose down