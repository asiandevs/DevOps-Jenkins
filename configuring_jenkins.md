# Configuring Jenkins

## To access Jenkins through its management interface

From your browser, connect to http://<your_server_public_DNS>:8080 . 

## Unlock Jenkins screen
As prompted, enter the password found in /var/lib/jenkins/secrets/initialAdminPassword.

Use the following command to display this password:
```
$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
## Install suggested plugins
The Jenkins installation script directs you to the Customize Jenkins page. Click Install suggested plugins.
Jenkins Plugin Manager showing available plugins.
Once the installation is done, select Back to Dashboard.

## Create your first admin user.
On the left-hand side, select Manage Jenkins, and then select Manage Plugins.

