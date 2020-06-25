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