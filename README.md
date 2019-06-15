# WordPress in RPi

请见[中文文档](./README-cn.md)

This docker-compose.yml was tested in Raspberry Zero W and Raspberry 3B+ with Raspbian Stretch 2019 installed. Micro SD card is 32GB. Other rpi were not tested. You can test it and give me feedback.

## Intall

### install docker

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

### start

```bash
docker-compose up -d
```

### browser

Open browser and view: http://localhost

## Refs