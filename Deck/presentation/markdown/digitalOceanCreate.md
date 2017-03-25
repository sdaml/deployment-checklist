# Create a Digital Ocean Droplet

- Create an account on [Digital Ocean](https://www.digitalocean.com/)
- Create an Ubuntu 16.04 droplet with 512MB of memory, in a datacenter of your choice
- Add your **public** ssh key to the droplet
    + The ssh key is likely `~/.ssh/id_rsa.pub`
    + You can also create a new ssh key by typing `ssh-keygen -t rsa -C "your_email@example.com"`
- Give your droplet a hostname (this isn't visible to the public, so call it something you will remember it by)
