### WORK IN PROGRESS
# jenkins-secured-rancherOS
Installation script for jenkins secured via ngninx and certbot (letsentcrypt).

The docker-compose.yml includes the services jenkins/jenkins, ngninx:latest and certbot/certbot.
The init-letsencrypt script starts the automated initial config. After that you could start, stop and restart the system via docker-compose up/down/restart.

### COPYRIGHT
Special thanks to [Juriy](https://github.com/Juriy/) and [wmnnd](https://github.com/wmnnd/).
I used the [jenkins.conf](https://github.com/Juriy/easyio/blob/master/conf/nginx/jenkins.conf) to configure nginx for jenkins 
and the docker-compose and init-letsencrypt file from [wmnnds repo](https://github.com/wmnnd/nginx-certbot) for the docker installation of nginx with encryption.
Basically 90% of the work contributes to them. I combined those two repos to creat an easy jenkins installation on Container Operating Systems like rancherOS.

### Additional Information
If you are using this you may update the paths in docker-compose and your domain information as well as the e-mail address in the app.conf file. I will comment out the important stuff.
Also you may switch consoles in RancherOS to get some additional command line tools since RancherOS is very minimalistic.
