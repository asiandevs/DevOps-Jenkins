# Jenkins: Disable, Discard and Delete Job
-------------------------------
## Disable a Jenkins Job:
-------------------------------
1. Open your web browser and navigate to your Jenkins instance.

2. On the Jenkins dashboard, find the job you want to disable.

3. Click on the job name
   - click on "Disable Project" to disable job
     ![image](https://github.com/asiandevs/images/blob/3f02bad49a9a3abb9a77f481b8cf7849981f0bf2/Jenkins_disable_job.jpg)
   - To enable click "Enable"
     ![image](https://github.com/asiandevs/images/blob/3f02bad49a9a3abb9a77f481b8cf7849981f0bf2/Jenkins_enable_job.jpg)
   
 ### Other option
   - go to the job configuration page. Enable / disable on toggle button
     ![image](https://github.com/asiandevs/images/blob/3f02bad49a9a3abb9a77f481b8cf7849981f0bf2/Jenkins_enable_disable.jpg)

-------------------------------
## Discard a Jenkins Job:
-------------------------------
1. Navigate to the Jenkins dashboard.
2. Click on the name of the job for which you want to discard changes.
3. If you are in the process of editing the job configuration and want to discard changes without saving:
  - Click on the "Discard old builds".
  - Give number of "Days to keep builds" and "Max # of builds to keep" and click Save.
   ![image](https://github.com/asiandevs/images/blob/05626c85a965422489fa8702d6b62f779541fbea/Jenkins_discard.jpg)  

---------------------------
## Delete a Jenkins Job:
---------------------------
1. Open your web browser and navigate to your Jenkins instance.

2. On the Jenkins dashboard, find the job you want to delete.

3. Click on the job name to go to the job configuration page.

4. In the left-hand menu, click on "Delete Project" under the "Build History" section.
 ![image](https://github.com/asiandevs/images/blob/b50c4b393f05403b9d9f568318a2766157083de9/Jenkins_delete1.jpg)  
   Confirm the deletion when prompted.

   Note: Deleting a job removes all its build history and configurations. Be cautious when deleting jobs.

### Alternatively, 
you can delete a job directly from the Jenkins dashboard:

1. On the Jenkins dashboard, find the job you want to delete.

2. Hover over the job name, and a small drop-down arrow will appear to the right.
 
3. Click on the arrow, and you will see options, including "Delete Project"
   ![image](https://github.com/asiandevs/images/blob/b50c4b393f05403b9d9f568318a2766157083de9/Jenkins_delete2.jpg) 

4. Click on "Delete" and confirm the deletion when prompted.

Remember to exercise caution when deleting jobs, especially if they have valuable build history or configurations. Disabling a job is a safer option if you might need to re-enable it later.
