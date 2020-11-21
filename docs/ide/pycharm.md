## JetBrains PyCharm
### Install JDK
```
$ sudo apt update
$ sudo apt install default-jdk
```
Check installed version
```
$ java -version
```
### Install PyCharm
* Download [PyCharm for Linux](https://www.jetbrains.com/pycharm/download/#section=linux)
* Copy the `pycharm-<VERSION>.tar.gz` to the desired installation location
```
$ sudo mkdir -p /opt/jetbrains; cd /opt/jetbrains
```
* Unpack the pycharm-<VERSION>.tar.gz file to an empty directory using the following command
```
$ sudo tar -xzf pycharm-<VERSION>.tar.gz -C /opt/jetbrains
```
Note: A new instance MUST NOT be extracted over an existing one. The target folder must be empty
```
sudo rm -rf /opt/jetbrains/pycharm-<VERSION>
```
* Run `pycharm.sh` from the bin subdirectory
```
$ cd /opt/jetbrains/pycharm-<VERSION>/bin
$ ./pycharm.sh
```
* Right mouse click on the PyCharm in launcher panel and hit "Lock to Launcher" or "Iconify", or create a desktop shortcut
  - Open new file for editing
  ```
  vi ~/Desktop/pycharm.desktop
  ```
  - Copy/paste following content to it (change PyCharm version to one, installed above)
  ```
  [Desktop Entry]
  Name=PyCharm
  GenericName=Text Editor
  Exec=/opt/jetbrains/pycharm-<VERSION>/bin/pycharm.sh
  Icon=/opt/jetbrains/pycharm-<VERSION>/bin/pycharm.png
  Type=Application
  StartupNotify=false
  Categories=Utility;TextEditor;Development;IDE;
  MimeType=text/plain;inode/directory;
  Actions=new-empty-window;
  Keywords=pycharm;

  X-Desktop-File-Install-Version=0.23

  [Desktop Action new-empty-window]
  Name=New PyCharm
  Exec=/opt/jetbrains/pycharm-<VERSION>/pycharm.sh --no-sandbox --new-window %F
  Icon=/opt/jetbrains/pycharm-<VERSION>/bin/pycharm.png
  ```
  - Hit `Esc`, then `:x` to save and exit
