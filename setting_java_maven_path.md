# setup Java Path and Maven Path  in Jenkins
-------------------------------------
## Setting up Java Path:
-------------------------------------
1. Navigate to Jenkins and log in.
2. Click on **Manage Jenkins** in the left menu.
3. Click on **Global Tool Configuration**.
4. Scroll down to the **JDK** section.
5. Click on **JDK installations...** to add a new JDK installation.
6. Click on **Add JDK**.
7. Provide a name for the JDK installation (e.g., `JDK3`).
8. Specify the path to the JDK installation directory. You can either install a JDK on the Jenkins machine, and then specify its path, or you can use a tool installer.
9. Click **Save**.
---------------------------
## Setting up Maven Path:
---------------------------
1. In the same **Global Tool Configuration** page, scroll down to the **Maven** section.
2. Click on **Maven installations...** to add a new Maven installation.
3. Click on **Add Maven**.
4. Provide a name for the Maven installation (e.g., `mvn7`).
5. Specify the path to the Maven installation directory. Similar to Java, you can install Maven on the Jenkins machine and provide its path, or use a tool installer.
6. Click **Save**.
