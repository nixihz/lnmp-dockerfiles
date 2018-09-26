## build image 
```
cd ./config/redis
sudo docker build -t myapp/redis3.2:0.0.1 .

cd ../../
cd ./config/mysql
sudo docker build -t myapp/mysql5.7:0.0.1 .


cd ../../
cd ./config/php7
sudo docker build -t myapp/php7.0-fpm:0.0.1 .

cd ../../
cd ./config/nginx
sudo docker build -t myapp/nginx1.14:0.0.1 .

cd ../../
```

## mkdir dirs

```
mkdir -p data/mysql/3306/
mkdir -p data/redis/6379/
mkdir -p logs/nginx/
mkdir -p logs/php7/
```

## docker

```
### list images
docker image ls  

### swarm init
docker swarm init

### deploy docker-composer.yml file
docker stack deploy -c docker-compose.yml myapp

### rm stack
docker stack rm myapp

### list containers
docker container ls -a   

### rm exited containers
docker container rm $(sudo docker container ls -a -q)   

```
