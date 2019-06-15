# WordPress in RPi

## 安装

### 安装docker

```bash
sudo apt-get purge docker-ce
sudo apt-get install docker-ce=18.06.2~ce~3-0~raspbian
sudo systemctl enable docker && sudo systemctl start docke

sudo apt remove -y python-pip
sudo apt install -y python-pip
sudo pip install docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

sudo groupadd docker
sudo gpasswd -a ${USER} docker
sudo service docker restart
sudo chmod a+rw /var/run/docker.sock
```

### 启动容器

```bash
docker-compose up -d
```

## 参考