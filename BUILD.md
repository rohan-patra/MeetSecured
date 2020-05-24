# Installation - Manual

**Prerequisites**
- OS: Ubuntu STL or Debian (Any Version)
- Ram: 16 GB
- APT
- `apt-transport-https` package installed
- `NGINX` or other server installed
- SQL/Database
- `NodeJS` and `npm` version 10 and above
- NPM addon: @babel/plugin-transform-flow-strip-types
- LivePeerJS
- Domain set up and pointed to IP



**Clone Source Using Below Command**

`git clone https://github.com/rohan-patra/MeetSecured.git`

**Ready to Install**
- `echo 'deb https://download.jitsi.org stable/' > /etc/apt/sources.list.d/jitsi-stable.list`
- `wget -qO - https://download.jitsi.org/jitsi-key.gpg.key | apt-key add -` 
- *These lines add the Jitsi SIP repo to your system source list*
- *Next, install Jitsi SIP*
- `apt-get install jitsi-meet -y`
- *Get SSL Certificate from Let's Encrypt*

   

- `wget https://dl.eff.org/certbot-auto`
- `wget -N https://dl.eff.org/certbot-auto.asc`
- `apt-get install gnupg2 -y # needed to receive and validate the certificate`
- `gpg2 --keyserver pool.sks-keyservers.net --recv-key A2CFB51FA275A7286234E7B24D17C995CD9775F2`
- `gpg2 --trusted-key 4D17C995CD9775F2 --verify certbot-auto.asc certbot-auto`
- `chmod a+x ./certbot-auto`
- `mv ./certbot-auto /usr/local/bin/certbot`
- `certbot certonly --nginx --rsa-key-size 4096 -m `youremail@example.com` -d `yourdomain.com

 - Should result in the following message: 
`gpg: Good signature from "Let's Encrypt Client Team <letsencrypt-client@eff.org>" [ultimate]`
 - Clone the repo and run `npm install` and `make` in the same directory
 - Copy build folder contents and paste inside directory `/usr/share/jitsi-meet`
 - `systemctl restart nginx.service jicofo.service jitsi-videobridge2.service`
 - Application should run on both http and https as long as there are no firewall restrictions
