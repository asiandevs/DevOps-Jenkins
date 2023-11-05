# Downloading and installing Jenkins [ Here in AWS Linux]
## Connect to your instance
Perform a software packages update
```
sudo yum update –y
```
## Add the Jenkins repo

```$ sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
```
Import a key file from Jenkins-CI to enable installation from the package:

```$ sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
$ sudo yum upgrade
```
## Install java
Jenkins is Java based application. I am using AWS EC2 instance, Install Java (Amazon Linux 2023):

```
$ sudo dnf install java-17-amazon-corretto -y
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
