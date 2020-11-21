# IDE for development
## JetBrains PyCharm
[Now to](https://youtrack.jetbrains.com/issue/JBR-549)

[Files](https://bintray.com/jetbrains/intellij-jbr/jbrsdk11-linux-aarch64#files)

### Install OpenJDK
```
sudo dpkg —add-architecture armhf
sudo apt update
sudo apt install opened-11-jre:armhf
```
Check installed version
```
PATH=/usr/lib/jvm/java-11-openjdk-armhf/bin:$PATH java -version
```
openjdk version "11.0.4" 2019-07-16
OpenJDK Runtime Environment (build 11.0.4+11-post-Ubuntu-1ubuntu218.04.3)
OpenJDK Server VM (build 11.0.4+11-post-Ubuntu-1ubuntu218.04.3, mixed mode)
Now, modify startup script (in my case I use pycharm) pycharm.sh script to include 
`PATH=/usr/lib/jvm/java-11-openjdk-armhf/bin:$PATH` or just run the following command in your terminal
```
$ PATH=/usr/lib/jvm/java-11-openjdk-armhf/bin:$PATH ./pycharm.sh
```
