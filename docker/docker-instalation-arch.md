# enable loop module

```bash
 sudo tee /etc/modules-load.d/loop.conf <<< "loop" && \
 modprobe loop
```

# install stable docker from community repo

```bash
sudo pacman -S docker
```

# start and enable docker

```bash
systemctl start docker.service && \
systemctl enable docker.service
```

# add user to run docker without root

```bash
groupadd docker
gpasswd -a <username> docker
```

# restart computer

```bash
shutdown -r now
```

# Check instalation

```bash
docker info
```

