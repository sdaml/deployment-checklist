#### Step 4 - Configure the Server Block file
- Remove `default_server` from the `listen` lines
- If you have a domain name you'd like to associate with the server block, change the `server_name` from `YOUR_IP_ADDRESS` to your domain.

```
server {
        listen 80;
        listen [::]:80;

        root /var/www/<your-proj-name>;
        index index.html;

        server_name YOUR_IP_HERE;

        location / {
                try_files $uri $uri/ =404;
        }
        
        location /static/ {
            alias /var/www/<your-proj-name>;
            autoindex off;
        }
}
```

#### Step 5 - Enable your Server Blocks
```sh
sudo ln -s /etc/nginx/sites-available/<your-repo-name> /etc/nginx/sites-enabled/ # Copy your server block from sites available to sites enabled
sudo nginx -t # test to make sure there are no syntax errors in your configuration
sudo systemctl restart nginx # restart the nginx process
```

