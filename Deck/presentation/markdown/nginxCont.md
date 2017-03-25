## Set up Nginx Server Blocks

#### Step 1 - Set up new Document Root Directories
```sh
sudo mkdir -p /var/www/<your-repo-name> 
sudo chown -R $USER:$USER /var/www/<your-repo-name>
```

#### Step 2 - Clone your github repo
```sh
cd /var/www/
git clone https://<github-username>@github.com/<github-username>/<repository-name>.git
npm install
npm run build
# NOTE: modify your index.html file so that the bundle.js file is the one located in the dist directory 
```

#### Step 3 - Create a Server Block File
```sh
sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/<your-repo-name>
sudo vim /etc/nginx/sites-available/<your-repo-name>
```

