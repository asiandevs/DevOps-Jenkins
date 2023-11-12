# Set up a Jenkins Scripted Pipeline

1. First, log on to your Jenkins server and select “New Item” from the left panel:

2. Next, enter a name for your pipeline and select “Pipeline” from the options. Click “Ok” to proceed to the next step:

3. You can now start working on your Pipeline script:

```groovy
node {
    stage('build') {
        echo 'hello this is build phase'
    }
        stage('test') {
        echo 'hi this one is test phase'
    }
        stage('verify') {
        echo 'ok, verify has been completed'
    }
}
```
4. click Save
5. Build now
