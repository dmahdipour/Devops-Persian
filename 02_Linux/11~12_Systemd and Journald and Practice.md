### Systemd (OLD -> initd)
* First process with pid=1
* Put other process on background
* Manage all services
* SystemCTL
```shell
systemctl start SERVICE_NAME
systemctl stop SERVICE_NAME
systemctl status SERVICE_NAME    #Display the status and config files path, etc.
systemctl enable SERVICE_NAME    #Run a service automatically after reboot -> config by config.d files
systemctl disable SERVICE_NAME
systemctl mask SERVICE_NAME      #Stop a service in the manner that give a message to them who want to enable. It makes a symlink to /dev/null
systemctl unmask SERVICE_NAME
systemctl edit SERVICE_NAME      #Config a service actions

systemctl is-enabled SERVICE_NAME
systemctl is-active SERVICE_NAME
systemctl is-failed SERVICE_NAME

sytemctl edit SERVICE_NAME       # Create a file to override main config file of the service in /etc/systemd/system/SERVICE_NAME.service.d/override.conf
vim /etc/systemd/system/SERVICE_NAME.service.d/override.conf  #Ater which service should be run, what's the TYPE, PID, KillMode, Timeout, etc.
```

### Journald
* Keep a service logs
* List of boots and what happen to a service after boot
* Help to debugging 
* JournalCTL
```shell
journalctl -xefu SERVICE_NAME   #Show the service log  -f follow, -u service name
```

**Note:** After each action, validate it. ex: after  <u>mkdir test</u>  run  <u>ls</u>  to make sure it acts correctly.

