## Jenkins Freestyle Job for Checking Linux Disk Usage

1. **Create a new Freestyle Project:**

   - Open Jenkins and click on "New Item" in the dashboard.
   - Enter a name for your project and select "Freestyle project," then click "OK."

2. **Configure Source Code Management (Optional):**

   - If your job requires checking disk usage on a specific code repository, configure the appropriate source code management system.

3. **Build Configuration:**

   - In the project configuration, scroll down to the "Build" section.
   - Click on the "Add build step" dropdown and choose "Execute shell" (for Linux) or "Execute Windows batch command" (for Windows).

4. **Add Shell Commands:**

   - For Linux, in the "Command" textarea, add the following shell commands to check disk usage:

     ```bash
     df -h
     ```

     This command displays disk space usage on all mounted file systems in a human-readable format.

   - You may also want to redirect the output to a file for better analysis:

     ```bash
     df -h > disk_usage.txt
     ```

5. **Save and Build:**

   - Save your Jenkins job configuration.
   - Trigger a build to see the disk usage information in the Jenkins console output.

You can customize the shell commands based on your specific requirements. Ensure that the Jenkins user has the necessary permissions to execute the disk-related commands.

