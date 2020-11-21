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
* Right mouse click on the PyCharm in launcher panel and hot "Lock to Launcher"
