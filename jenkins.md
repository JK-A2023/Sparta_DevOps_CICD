# Jenkins

### What is it?

- An open-source server automation server used for implementing CICD pipelines. 
- It helps to automate and streamline the building, testing, and deployment of software applications
- Makes the software development process more efficient and reliable.

### Why use it?

1. Start Jenkins
2. Run the following where you have jenkins.war file:
   1. `java -jar jenkins.war`
3. Open browser, type the following:
   1. `www.localhost:8080`
   2. If port 8080 is already in use, use the following:
      1. `java -jar jenkins.war –-httpPort=7070`
4. Log into your account.
5. Click New Item
6. Enter name as Job1 (you can choose any name you wish)
7. Select freestyle proejct, then click OK.
8. Repeat these steps to create 2 more jobs, i.e., Job2, Job3.
9. Click on Dashboard.
10. Click on Job1.
11. Click on Configure on the left menu.
12. Click on add build step.
13. From the drop down menu, select `Execute Shell`
14. Enter the command: `date`
15. 