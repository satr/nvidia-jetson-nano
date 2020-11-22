# Troubleshooting

### Change desktop manager with terminal command
If after selecting desktop manager system is not loaded:
  - Hit Ctrl+Alt+F1 to open another terminal session, login with user and password
  - Run command to edit user configuration `sudo vi /var/lib/AccountService/users/<USERNAME>`
  - Change property `XSession` to another desktop manager `XSession=ux-unity`
  - Hit Esc, then `:x` to save and exit
  - Reboot with command `sudo reboot now`
### Change auto-login with teminal command
To change autologin setting with terminal command
  - edit `sudo vi /etc/gdm3/`
  - set `true` or `false` to the property `AutomaticLoginEnable` in the section `daemon`. Ex.:
  ```
  [daemon]
  AutomaticLoginEnable=false
  ```
  - hit Esc, then `:x` to save and exit

### Docker fails on `run` command
If there is an error _docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock_ on `docker run` command
* Execute commands
```
sudo groupadd docker; sudo usermod -aG docker ${USER}
```
* Logout and login again
