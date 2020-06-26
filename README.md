## Ansible documentation commnads

### Get a module specific documentation (shorten version)
```
ansible-doc -s <module-name>
```

### Get a module specific documentation (full version)
```
ansible-doc <module-name>
```

### "Help" list for ansible-doc
```
man ansible-doc
```

### List of all ansible modules
```
ansible-doc -l
``` 
you can also search on it using
```
/<keyword>
```

## Linux user management

### How to give root access to a user
```
sudo usermod -aG sudo <user>
```

### How to remove root password prompt for commands
````
sudo visudo
```
Write at the bottom of the file
```
<user> ALL=(ALL) NOPASSWD: ALL
```
Run the following to clear cache
```
sudo -k
```
to test run the following
```
sudo ls
```
it should not ask for a prompt password

### Network machine configuration
first get the needed information
You will need
* Your ip and mask (ex 192.254.254.199/24) in this case your local network would be 192.254.254
* Your gate-way (Can be found here https://osxdaily.com/2011/09/15/find-default-gateway-ip-address-mac-os-x/)
```
route get default |grep gateway
```

etc/netplan/<tab>

sudo netplan apply