# Configure Nginx
- Nginx is one of the most popular web servers in the world.

#### Step 1 - Install Nginx
```sh
sudo apt-get update
sudo apt-get install nginx
```

#### Step 2 - Adjust the Firewall
```
sudo ufw app list # List available applications
sudo ufw allow 'Nginx HTTP' # enable Nginx HTTP
sudo ufw allow 'Nginx HTTPS' # enable Nginx HTTPS
sudo ufw enable # enable firewall
sudo ufw status # Verify changes
```
- Visit your IP address in a web browser to see the nginx landing page

#### Step 3 - (Optional) Configure a Hostname for your Droplet
- Domain names can be bought from, for example, [Namecheap](https://www.namecheap.com/)
- We're going to skip this step, but a detailed tutorial can be found [here](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-host-name-with-digitalocean)
