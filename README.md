
### Pre-requisites
* Vagrant
* VirtualBox

### To configure (only do this once):

Place this in your `~/.ssh/config` file

```
Host 192.168.33.* *.myapp.dev
  StrictHostKeyChecking no
  UserKnownHostsFile=/dev/null
  User root
  LogLevel ERROR
```

Ensure the Hosts Updater plugin is installed inside Vagrant

```
vagrant plugin install vagrant-hostsupdater
```
### To run the environment:
Stand up the Vagrant environment & SSH into the fresh VM
```
vagrant up app1
ssh app1.myapp.dev
```
