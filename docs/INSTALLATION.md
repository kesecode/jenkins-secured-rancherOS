# Step by step install guide
#### On a DigitalOcean RancherOS Instance
Create a rancherOS instance on digital ocean and point your domain on the instance, floating ip recommended.

Connect via SSH and follow the instructions.
Consider a private fork of the repo to add your domain and email address in the config files before you pull it on to your instance.

---

1. Switch console to centos then reconnect
```
sudo ros console switch centos
```
2. Update yum
```
sudo yum update
```
3. Install git
```
sudo yum -y install git
```
4. Install Docker-Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```
5. Clone Repo to rancher home
```
git clone https://github.com/kesecode/jenkins-secured-rancherOS/
```
6. (Edit in your domain name(s))

8. Run chmod inside the repository
```
sudo chmod +x init-letsencrypt.sh
```
8. Run init
```
sudo ./init-letsencrypt.sh
```
9. Restart Docker-Compose instance (without -d)
```
docker-compose down
docker-compose up
```
10. Note the initial admin password for jenkins. After the initialization you can run in detached mode. Have fun!
