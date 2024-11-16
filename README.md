

To activate SSH on Ubuntu and connect to it using PuTTY from another machine, follow these steps:

Step 1: Install and Enable SSH on Ubuntu
Install the SSH server (if not already installed):

```
sudo apt update
sudo apt install openssh-server
```

Enable and start the SSH service:

```
sudo systemctl enable ssh
sudo systemctl start ssh
```

Check the SSH status to confirm it’s running:

```
sudo systemctl status ssh
```

Find the IP address of your Ubuntu machine: Run the following command to get the IP address:

```
ip a
```

or 

```
ifconfig
```

Look for the IP address associated with your network interface (it often appears under inet).

Step 2: Configure the Firewall (if applicable)
Allow SSH through the firewall:

```
sudo ufw allow ssh
```

Enable the firewall (if it isn’t already enabled):

```
sudo ufw enable
```

Check the firewall status to confirm SSH is allowed:

```
sudo ufw status
```

Step 3: Connect to Ubuntu Using PuTTY
1. Download and install PuTTY on your Windows machine from the official PuTTY site, if you haven't already.

2. Open PuTTY and enter the IP address of your Ubuntu machine in the Host Name (or IP address) field.

3. Set the Port to 22 (default SSH port) and ensure the Connection type is set to SSH.

4. Click Open to start the SSH connection.

5. Log in with your Ubuntu username and password when prompted.