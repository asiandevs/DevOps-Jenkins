-----------------------------------
# Integrating Jenkins with Git
-----------------------------------
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

3. **Set Up Build Triggers:**
   - In the same job configuration, find the "Build Triggers" section.
   - Select the option that triggers the build based on changes in the Git repository. For example, you can choose "Poll SCM" to check for changes at regular intervals or "Build when a change is pushed to GitLab" for webhook-based triggering.

![image](https://github.com/asiandevs/images/blob/6f0ac931a4ee21dbcdcafd0c0e0ab164014f635b/gitrepo_buildtrigger.jpg)

4. **Configure Additional Build Steps:**
   - Set up the build steps according to your project requirements.
   - This may include executing shell commands, running Maven or Gradle builds, or any other build tool specific to your project.

5. **Save and Run the Job:**
   - Save the Jenkins job configuration.
   - Manually trigger a build to test the integration.

------------------------------------------------------------------
## Webhooks (Real-time Triggers - Jenkins job from Git):
-----------------------------------------------------------------
To enable real-time triggering of Jenkins builds upon Git commits, it's recommended to set up webhooks. Webhooks allow Git repositories to notify Jenkins whenever a change occurs.

1. **Create or Configure a Jenkins Job:**
2. **Configure Source Code Management (SCM):**
3. **Set Up Build Triggers:**
Enable GitHub hook trigger for GITScm polling under Build Triggers.
   ![image](https://github.com/asiandevs/images/blob/6d8fb3fdc4aea5660b394fb0661e0f3f2bbd20e7/BuildTrigger_webhook.jpg)
5. **Configure Additional Build Steps:**
• Select “Execute shell” under “Build” section.
• Enter the commands
  javac JenkinsWorld.java
6. **Save the Job:**
7. **Enable webhook in GitHub:**
   **Generate a Jenkins URL:**
   - Ensure your Jenkins server is accessible from the internet.
   - Obtain the external URL for your Jenkins server (e.g., `http://your-jenkins-server:8080`).

   **Configure Webhooks in Git Repository:**
   - In your Git repository settings, find the webhook or integrations section.
   - Add a new webhook and provide the Jenkins URL with the path `/github-webhook/` (for GitHub) or `/gitlab-webhook/` (for GitLab).
   - Ensure that the webhook is triggered on push events.
       ![image](https://github.com/asiandevs/images/blob/6d8fb3fdc4aea5660b394fb0661e0f3f2bbd20e7/github_webhook.jpg)

   **validate  settings on Jenkins side:**
    Manage Jenkins -> Configure System -> GitHub ->Advanced -> Override Hook URL
    ![image](https://github.com/asiandevs/images/blob/e7bebbe88f0415337a2e29363f4cbc46beba498d/validatewebhookJenkins.jpg)
   
   **Test Webhook:**
   - After setting up the webhook, make a small change in your Git repository and check if Jenkins is triggered automatically.

By following these steps, you'll have successfully integrated Jenkins with your Git repository, allowing for continuous integration and automated builds triggered by changes in your Git codebase.

