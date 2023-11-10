# Integrating Jenkins with Git

## Prerequisites:

1. **Install Jenkins:**
   Ensure that Jenkins is installed and running on your server. You can download Jenkins from the [official website](https://www.jenkins.io/) and follow the installation instructions for your operating system.

2. **Install Git Plugin:**
   Jenkins relies on plugins to extend its functionality. Install the Git plugin in Jenkins to enable Git integration.
   - Go to "Manage Jenkins" > "Manage Plugins."
   - Navigate to the "Available" tab and search for "Git."
   - Check the box next to "Git Plugin" and click "Install without restart."

## Configure Jenkins with Git:

1. **Create or Configure a Jenkins Job:**
   - Create a new freestyle Jenkins job (e.g., JenkinsWorld) or configure an existing one.

2. **Configure Source Code Management (SCM):**
   - In the job configuration, find the "Source Code Management" section.
   - Select "Git" as the SCM option.
   - Provide the Git repository URL.
   - Configure credentials if your repository requires authentication.
 ![image](https://github.com/asiandevs/images/blob/6f0ac931a4ee21dbcdcafd0c0e0ab164014f635b/gitrepodefined.jpg)

4. **Set Up Build Triggers:**
   - In the same job configuration, find the "Build Triggers" section.
   - Select the option that triggers the build based on changes in the Git repository. For example, you can choose "Poll SCM" to check for changes at regular intervals or "Build when a change is pushed to GitLab" for webhook-based triggering.

![image](https://github.com/asiandevs/images/blob/6f0ac931a4ee21dbcdcafd0c0e0ab164014f635b/gitrepo_buildtrigger.jpg)

5. **Configure Additional Build Steps:**
   - Set up the build steps according to your project requirements.
   - This may include executing shell commands, running Maven or Gradle builds, or any other build tool specific to your project.

6. **Save and Run the Job:**
   - Save the Jenkins job configuration.
   - Manually trigger a build to test the integration.
