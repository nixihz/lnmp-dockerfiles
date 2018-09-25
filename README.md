## image 
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


