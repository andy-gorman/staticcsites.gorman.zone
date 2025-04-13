# Configuration For My Static Sites, stored on my DO droplets
Right now this is just instructions in this README and a todo list ## Setup This is how I setup my Digital Ocean Instance
* Using the DO web terminal, I created a user `agorman`
  * `adduser agorman`
* Briefly allowed password based ssh login
  * Update /etc/ssh/sshd_config.d/50-cloud-init.conf 
      * /etc/ssh/sshd_config.d/50-cloud-init.conf
        `PasswordAuthentication yes`
* On local machine
    * ssh copy id my public ssh key over to new instance
* Disable password based ssh login

* Install NGINX (`apt-get install nginx`)
* Delete default nginx config `rm /etc/nginx/sites-enabled/default`
* Copy gorman.zone.conf to /etc/nginx/sites-enabled/gorman.zone
* Install certbot `apt-get install cerbot python3-certbot-nginx`
* 


* Utility
    * Install Mosh `apt-get install mosh`
        *  `locale-gen en_US.UTF-8` Needed to run mosh-server
    * Install ufw `apt-get install ufw`
        * ufw default deny incoming
        * ufw default allow outgoing
        * ufw allow OpenSSH
        * ufw allow mosh
        * ufw allow 'Nginx Full'
