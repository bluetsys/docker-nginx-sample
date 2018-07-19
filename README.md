# docker-nginx-sample
docker-nginx-sample

# node
```
sudo git clone https://github.com/bluetsys/docker-nginx-sample.git
sudo npm insatll
node index.js
```
# docker
```
$ sudo docker build --tag node-nginx:test docker-nginx-sample/
```

```
sudo docker build --tag node-nginx-lb:test docker-nginx-sample/nginx/
```

```
sudo docker run -d --name node-nginx-instance-01 -p 3001:3000 node-nginx:test
sudo docker run -d --name node-nginx-instance-02 -p 3002:3000 node-nginx:test
sudo docker run -d --name node-nginx-instance-03 -p 3003:3000 node-nginx:test
sudo docker run -d --name node-nginx-instance-lb -p 3000:80 node-nginx-lb:test
```