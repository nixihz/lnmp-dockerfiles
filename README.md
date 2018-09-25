## build image 
```
cd ./config/redis
sudo docker build -t btbtop/redis3.2:0.0.1 .

cd ../../
cd ./config/mysql
sudo docker build -t btbtop/mysql5.7:0.0.1 .


cd ../../
cd ./config/php7
sudo docker build -t btbtop/php7.0-fpm:0.0.1 .

cd ../../
cd ./config/nginx
sudo docker build -t btbtop/nginx1.14:0.0.1 .

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

### deploy docker-composer.yml file
docker stack deploy -c docker-compose.yml btbtop

### rm stack
docker stack rm btbtop

### list containers
docker container ls -a   

### rm exited containers
docker container rm $(sudo docker container ls -a -q)   

```
