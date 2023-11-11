### For Red Hat-based distributions (e.g., CentOS):

1. Open a terminal.

2. Install Apache Maven using the following command:

    ```bash
    sudo yum install maven
    ```

3. Verify the installation:

    ```bash
    mvn -version
    ```

4. Set up environment variables. Open your shell profile configuration file (e.g., `~/etc/profile`) and add the following lines:

`vi /etc/profile`

    ```bash
      export MAVEN_HOME=/usr/share/maven
      export PATH=$MAVEN_HOME:$PATH
    ```
Then, reload the configuration:

      ```
      source /etc/profile
      ```

**Note: For the latest versions and additional information, visit the [Apache Maven website](https://maven.apache.org/).**
