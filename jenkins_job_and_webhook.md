# Jenkins


1. Navigate to the Jenkins homepage.
2. Select `New Item`
3. Give your project a name.
4. Select what type of project you want (in this case, a Freestyle Project)


![img.png](images/jenkins/image.png)

5. Give it a description.
   1. While optional, this is highly advised.

![img.png](images/jenkins/image-1.png)

6. Select `Discard old builds`
7. Set the `Max # of builds to keep` to `3`


![img.png](images/jenkins/image-2.png)

8. Select what step you wish it to complete.
   1. Here, we are selecting Execute Shell
   2. Jenkins will create a bash file (.sh gile)
9. To test if this build works, type the following in the command window:
   1.  `whoami`
   2.  `uname -a`

![img.png](images/jenkins/image-3.png)


![img.png](images/jenkins/image-4.png)

10. Press Save.
11. Return to the Dashboard.

![img.png](images/jenkins/image-5.png)

12. Using the dropdown menu on your job, select the build now button.

![img.png](images/jenkins/image-6.png)

13. Select the Console Output to see if it has worked.

### Possible Issues

If the server endpoint IP address is to change, then you need to change the GitHub webhook to update it.
It will no longer automatically update if it is using the wrong IP address.

# How to set up GitHub webhook with Jenkins

DISCLAIMER: Must already have credentials added.

### Create project:

1. Add a name
2. Freestyle Project
3. Ok

![img.png](images/webhook/image.png)

### General

1. Add description :

![img.png](images/webhook/image-1.png)

2. Discard old builds
   1. Max # of builds to keep: `3`

![img.png](images/webhook/image-2.png)

3. Enable Github Project.
4. Navigate to GitHub repo page.
   1. Click green code.
   2. Copy HTTPS url.

![img.png](images/webhook/image-3.png)
![img.png](images/webhook/image-4.png)

### Office 265 Connector

1. Restrict where this project can be run:
   1. specify `sparta-ubuntu-node`
   2. If using the drop down, make sure to delete the space it adds on at the end. No whitespace.

![img.png](images/webhook/image-5.png)

### Source Code Management:

1. Copy the same GitHub repo as before.
2. Use your credentials that you added previously.
3. Change branch specifier to main, NOT master.

![img.png](images/webhook/image-6.png)

### Build Triggers:

1. Select GitHub hook trigger.

![img.png](images/webhook/image-7.png)

### Build Environment:

1. Select Provide Node

![img.png](images/webhook/image-8.png)

### Build:

1. Select add Build Steps
2. Select Execute Shell

![img.png](images/webhook/image-9.png)

3. Add in your commands to ran on start:

![img.png](images/webhook/image-10.png)

4. Save.

### Test Run:

1. Click on Build Now:

![img.png](images/webhook/image-11.png)

2. Refresh page. If it is blue, it has worked. Else, you have made a mistake.

![img.png](images/webhook/image-12.png)

### GitHub Webhook.

1. Preemtively, we will copy our Jenkins address, up to the port:
   1. We will use this shortly.

![img.png](images/webhook/image-13.png)

2. Navigate to your GitHub repo.
   1. Find the repo settings.
   2. Navigate to the Webhooks section.
   3. Click Add webhook.

3. In the Payload URL, paste in the copied portion of the URL.
4. After this is pasted, type the following:
   1. `github-webhook.`
5. Change content Type to `application/json`
6. Add webhook.

![img.png](images/webhook/image-14.png)

7. Refresh the page. If it has worked, there will be a little green tick.

![img.png](images/webhook/image-15.png)

### Testing:

From here, make a small change to repo. When pushed to GitHub, it will communicate with Jenkins, starting the CI process, and automatically restart the instance with the changes made.