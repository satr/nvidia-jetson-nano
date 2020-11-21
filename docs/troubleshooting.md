#Troubleshooting

* If after selecting desktop manager system is not loaded:
  - Hit Ctrl+Alt+F1 to open another terminal session, login with user and password
  - Run command to edit user configuration `sudo vi /var/lib/AccountService/users/<USERNAME>`
  - Change property `XSession` to another desktop manager `XSession=ux-unity`
  - Hit Esc, then `:x` to save and exit
  - Reboot with command `sudo reboot now`
* To change autologin setting with command line
  - edit `sudo vi /etc/gdm3/`
  - set `true` or `false` to the property `AutomaticLoginEnable` in the section `daemon`. Ex.:
  ```
  [daemon]
  AutomaticLoginEnable=false
  ```
  - hit Esc, then `:x` to save and exit
