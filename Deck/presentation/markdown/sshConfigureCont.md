#### Step 3 - Add Public Key Authentication
- On your local machine, copy your **public** ssh key to your clipboard
```sh
    cat ~/.ssh/id_rsa.pub
```

- On the server, switch users from root to your new user and authorize your local ssh key
```sh
su - <username> # Switch to the new user
mkdir ~/.ssh # create an ssh directory
chmod 700 ~/.ssh # set ssh driectory permissions to owner only
vim ~/.ssh/authorized_keys # paste your public key into this file
chmod 600 ~/.ssh/authorized_keys # restrict execution permissions on the file
exit # return to the root user
```

#### Step 4 - Disable Password Authentication
- With ssh keys configured, it's best to increase the security of your server by disabling password authentication
```sh
vim /etc/ssh/sshd_config # Uncomment PasswordAuthentication and set to no
systemctl reload sshd # Reload the ssh daemon
```

#### Step 5 - Log in as the newly created user
```sh
ssh <username>@SERVER_IP_ADDRESS
```
