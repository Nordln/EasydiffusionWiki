On a server, VPS/Instance: EASIEST SETUP COPY PASTE AND GO!



sudo apt-get update && apt-get upgrade

Then reboot the vps or instance or your pc or whatever you are using.

Log back in ssh then run commands:



mkdir stable-diffusion-ui

cd stable-diffusion-ui

wget https://github.com/cmdr2/stable-diffusion-ui/releases/download/v2.05/stable-diffusion-ui-linux.tar.xz

tar -xf [stable-diffusion-ui-linux.tar.xz](https://github.com/cmdr2/stable-diffusion-ui/releases/download/v2.05/stable-diffusion-ui-linux.tar.xz)

./start.sh



Then go to http://localhost:9000/ for example you can go to domain.com:9000 or whatever.domain.com:9000



(For more info on how to unzip.xz files,any errors etc then you need to install something, go here: https://www.cyberciti.biz/faq/how-to-extract-tar-xz-files-in-linux-and-unzip-all-files/)



Now do these commands below to keep stable-diffusion-ui running when you exit the server/ssh window/terminal:



 cd stable-diffusion-ui

 tmux new -s stable-diddusion-ui

./start.sh



Close the Terminal/ssh windows and your domain will still be online, have fun!



This is a basic setup, firewall and SSL should be added and more.





\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\






Run the Stable Diffusion Web UI with Tmux
When you run your Stable Diffusion Web UI on a normal SSH session, the Web UI's process closes when you exit the SSH session. To continuously run your Web UI even when you leave the SSH session, use tmux, a terminal multiplexer.

I just did this:

 cd stable-diffusion-ui

 tmux new -s stable-diddusion-ui

./start.sh



but officially you should do:

To create a Tmux session, run:
$ tmux new -s StableDiffusion
You may change StableDiffusion with any session name you prefer. Please see [How to Install and Use Tmux](https://www.vultr.com/docs/how-to-install-and-use-tmux) for more information about Tmux.
Change the directory to stable-diffusion-webui.
$ cd ~/stable-diffusion-webui
Launch the Stable Diffusion Web UI by running launch.py using python.
$ python3 launch.py --listen
The --listen argument makes your Web UI listen to network connections, not just on localhost. Please see [Command Line Arguments and Settings](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Command-Line-Arguments-and-Settings) for more information.
Wait until your server launches.
Detach from the Tmux session by pressing CTRL + B then D.


If you get errors:



apt install opencv-python
apt update && apt install -y libsm6 libxext6
apt-get install -y libxrender-dev
sudo apt-get install libsm6 libxrender1 libfontconfig1
apt-get install libsm6 libxrender1 libfontconfig1

Also, remember errors are usually because you need to install something that is missing.



INSTALL SSL EASY:



Run the commands below to install NGINX if it is not installed already:

sudo apt-get update
sudo apt-get install nginx
Check the available configurations for your firewall with this command:

sudo ufw app list
The output will be as follows:

Output
Available applications:
  Nginx Full
  Nginx HTTP
  Nginx HTTPS
  OpenSSH
Next, enable NGINX with the following command:

sudo ufw allow 'Nginx HTTP'

Now copy paste these commands:

sudo ufw allow 22
sudo ufw enable﻿﻿


Then, confirm the setting by running the command below:

sudo ufw status
With it installed, we'll need to also create a config file for our Botpress server. To do this, run the command below:

cd /etc/nginx/sites-available
Create a new file by running the following command.

sudo nano kodeec.website
Copy the following in the file and save it.

server {
    # listen on port 80 (http)
    listen 80;
    server_name kodeec.website 47.254.153.30 www.kodeec.website;

    location / {
        include proxy_params;
        proxy_pass http://127.0.0.1:9000;
    }
}
Enable the configuration with the following command.

sudo ln -s /etc/nginx/sites-available/kodeec.website /etc/nginx/sites-enabled/
Now you should be able to access 'kodeec.website' on your browser but it is still unsecure.

To install SSL encryption for your website, we can use Let's Encrypt.

To get started with this, install the dependencies with the following commands:

sudo apt-get install software-properties-common
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get install certbot python-certbot-nginx
or
sudo apt-get install certbot python3-certbot-nginx
Once everything's installed and running, run the command below:

sudo certbot --nginx
Follow the prompt to generate a certificate for your domain.



Finally, run the commands below to enable HTTPS encryption and reload NGINX.

sudo ufw allow https
sudo systemctl reload nginx
After doing that, you should be able to access '[https://kodeec.website'](https://kodeec.website%27/) on your browser. We have successfully installed and secured stable diffusion ui.