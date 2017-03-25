# Configure your Digital Ocean Droplet

#### Step 1 - Login as Root
```bash
ssh root@SERVER_IP_ADDRESS
```

- If this is your first time logging in, you will be prompted to change the root password

#### Step 2 - Create a New User
- Root is a very powerful and dangerous user to do routine tasks with, so we'll create a new user for most activities
- This user will also have admin access by prepending `sudo` to any admin commands
```bash
adduser <username> # Create the user
usermod -aG sudo <username> # Add the user to the sudoers group
```
