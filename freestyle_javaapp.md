------------------------------------------------------------------------------
# Create a Freestyle project for a JAVA application (e.g., JenkinsWorldJava)
------------------------------------------------------------------------------
** Note : Make sure git software is installed before using git repository to the Jenkins server and set the correct Java path. **
## Create a New Job:
1. Click on "New Item" on the Jenkins dashboard.
2. Enter a name for your project/job (e.g., "jenkinsworldjava").
3. Select "Freestyle project" as the project type.
4. Click "OK" to create the job.

## Build Configuration:
- In the "Build" section, click on "Add build step" and choose "Execute shell" for shell scripts.
- Configure the build step with the necessary commands or settings.
  - Select “Execute shell” under “Build” section.
  - Enter the commands:
```shell
git clone https://github.com/asiandevs/jenkins-world-java.git
cd jenkins-world-java
javac JenkinsWorld.java
java JenkinsWorld
```

## Save the Configuration:
- Scroll to the bottom of the configuration page and click "Save" to save your job configuration.
- Click "Save and Build Now."

## Build the Job:
- On the Jenkins dashboard, find your newly created job and click on it.
- Click on "Build Now" to manually trigger a build.

## View Build Results:
- After the build is triggered, you can view the build progress and console output by clicking on the build number under the "Build History" section.
