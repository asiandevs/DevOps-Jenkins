# Downloading and installing Jenkins [ Here in AWS Linux]
## Connect to your instance
Perform a software packages update
```
yum update –y
```
## Get the OS version
```
 cat /etc/os-release
```
## Select the OS from the download and install Jenkins packages
Go to the page 
[Jenkins Packages Download](https://www.jenkins.io/download/)

In my case OS is Amazon Linux baesd on centos rhel fedora
```
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
Import a key file from Jenkins-CI to enable installation from the package:

```
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
## Install Jenkins
### Install java [ This case community one]
```
yum install fontconfig java-11-openjdk
```
```
sudo amazon-linux-extras install java-openjdk11
```
```
alternatives --config java
```
```
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.20.0.8-1.amzn2.0.1.x86_64
export PATH=$JAVA_HOME/bin$PATH
echo $JAVA_HOME
```
```
yum install jenkins
```

### Enable the Jenkins service to start at boot

```
systemctl enable jenkins
```
## Start Jenkins as a service and validate the status

```
$ sudo systemctl start jenkins
$ sudo systemctl status jenkins
```
NOTE: For other version of Java 
---------------------
## Install java
---------------------
Jenkins is Java based application. I am using AWS EC2 instance:
- First get the jdk package list
```
yum search jdk
```
installed from the available one
```
yum install java-1.8.0-openjdk-devel
```
### set JAVA HOME in Linux System
set / get  default Java version in Linux and select the version option
```
alternatives --config java
```
vi /etc/profile
```
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.382.b05-1.amzn2.0.2.x86_64
export PATH=$JAVA_HOME/bin$PATH
```
- enable from the current session or reconnect the session to reflect the change
```
source /etc/profile
```
```
echo $JAVA_HOME
java -version
```
