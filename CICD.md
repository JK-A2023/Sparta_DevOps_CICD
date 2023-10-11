# CICD

### What is it?

A set of practices and automation techniques to ensure code changes are integrated, tested, and delivered to production quickly and reliably.

1. Continuous Integration
   1. Code is frequently merged into code shared repository.
   2. This code is tested automatically.
   3. If the merge is unsuccessful, you are alerted within minutes.
   4. This is done continously throughout a project, as to avoid everyone trying to merge just before completion.
2. Continuos Delivery / Deployment
   1. Delivery:
      1. Post release, you can continue to deliver new changes to your customers quickly in a sustainable way.
      2. Release process is automated, and project can be deployed with one button.
   2. Deployment:
      1. All changes that pass all production tests are released to customers.
      2. No human intervention.
      3. Only changes that fail tests will not be deployed.

Also recieves feedback continously, as to work these changes into production to better the product.

### Why use it?

All of the above practices help to speed up the workflow, leading to more efficient production workflows, faster product iterations.
This means being quicker to market, with less down time.
These practices cut costs, saving money.

### How to use it?

Continuous Integration:
   -  
   


1. Start with code on a local machine.
2. Use SSH to connect to shared repo i.e., GitHub.
3. Upload to shared repo.
4. Webhook Trigger
5. SSh to Jenkins
6. Sends to testing server.
   1. Has Master Node (big Ec2)
   2. Sends automated tests to detached Agent Node.
   3. If tests pass, they will be available on the Master Node.
   4. Then pushes to development.
