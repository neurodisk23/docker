# Docker Instalaltions for Jetson Nano

REF : https://www.forecr.io/blogs/installation/how-to-install-and-run-docker-on-jetson-nano

Main steps 

1. Search for the Docker version
```
sudo docker version
```
2. Prerequisites
```
sudo apt-get update
sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg \
lsb-release
```
3. Get DOCKER official DPG key
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
4.Set up repo pull
```echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
5. Install DOCKER from repo
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
6. Run Hello world
   ```
   sudo docker container run hello-world
```
