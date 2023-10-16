# Setting up CI with Jenkins:

This CI job will clone code onto a Jenkins Virtual Machine every time code is pushed to the Dev branch of the specified repo and test it.

## General:

![img.png](images/jenkins_ci/image.png)

## Source Code Management:

![img.png](images/jenkins_ci/image-1.png)

## Build Triggers and Build Environment:

![img.png](images/jenkins_ci/image-2.png)

## Build Steps:

Execute shell:

```
cd app

npm install

npm test
```