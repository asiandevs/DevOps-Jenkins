# Downloading and installing Jenkins [ Here in AWS Linux]
## Connect to your instance
Perform a software packages update
```
sudo yum update –y
```
## Get the OS version
```
 cat /etc/os-release
```
## Install java
Jenkins is Java based application. I am using AWS EC2 instance:

```
yum search jdk
yum install java-1.8.0-openjdk-devel
```
### set JAVA HOME in Linux System
set / get default Java version in Linux
```
alternatives --config java
```
```
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.382.b05-1.amzn2.0.2.x86_64
export PATH=$JAVA_HOME/bin$PATH
echo $JAVA_HOME
java -version
```
## Select the OS from the download and install Jenkins packages
```
https://www.jenkins.io/download/
```
In my case OS is Amazon Linux baesd on centos rhel fedora
```
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
Import a key file from Jenkins-CI to enable installation from the package:

```
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```
```
  yum install jenkins
```

## Install Jenkins

```
$ sudo yum install jenkins -y
```

## Enable the Jenkins service to start at boot

```
$ sudo systemctl enable jenkins
```
## Start Jenkins as a service and validate the status

```
$ sudo systemctl start jenkins
$ sudo systemctl status jenkins
```
