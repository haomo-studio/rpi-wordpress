# WordPress in RPi

本项目在Raspberry Zero W 及 Raspberry 3B+中测试通过，操作系统为Raspbian Stretch 2019中测试通过。其他版本的rpi未测试（理论上应该都可以）。

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