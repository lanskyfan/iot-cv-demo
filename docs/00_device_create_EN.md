---
title: "Preparation: Installing and Configuring Cloud9"

---

## Installing and Configuring Cloud9

### The purpose of using Cloud9

AWS Cloud9 is a cloud-based integrated development environment (IDE) for cloud programming [1]. It allows developers to write, run, and debug the codes with the browser. Cloud9 provides sufficient pre-installed packages and essential tools for popular programming languages, including JavaScript, Python, PHP, etc. Moreover, developers can easily share the development environment with the teammates, which enables pair programming in real time.

In our project, we adopted Cloud9 for its great benefits of pair programming, serverless applications, and high integration with other services in AWS.

Our team cooperated to code and implement our project. Because everyone was interested in all the detail of the project, we implemented the project together: one teammate coded at a time and other teamamtes using Cloud9 to monitor and give ideas.

Our project included a serverless application for IoT devices and Cloud9 greatly helped us ease our coding and debuging with serverless application. Cloud9 provides preconfigurations of the development environment capable with all AWS services and also the environment ot locally testing and debugging AWS Lambda functions. We saved a lot of time and had fewer troubles when using Cloud9 for programming serverless applications, 

Another great advantage using Cloud9 is that Cloud9 can have direct terminal access to AWS. The traditional way to connect to a remote machine is using SSH connection. However, it is a bit tired to switching between editor and shell. When using Cloud9, we had the sudo privileges to our managed EC2 instances and a preauthenticated AWS Command Line Interface, which eased our access to our EC2 instances as well as improved our programming experience.

### Implementation

(A step by step implementation with screenshots.)

1. Install Cloud9 with EC2 Instances.

Before we started, we read the instructions of AWS Cloud9 carefully. Then, we logged in to the AWS Console and selected Cloud9. As shown in Figure(?), we created the environment with name IoT Project. We created a new EC2 instance with Amazon Linux system to host our Cloud9 IDE as shown in Figure(?). Finally, we reviewed our configuration (in Figure(?)).

2. Connect to Cloud9 with browser.

In this step, we tested our connection to our Cloud9 IDE using browser as shown in Figure(?). We tested the connection speed of Cloud9 as well as the smooth experience of the integrated remote terminal.

3. Share our Cloud9 with all teammates.

In order to collaborate with our teammates, we shared our Cloud9 Platform. Since all our teammates were in the same AWS Account with different IAM, we shared our Cloud9 as shonw in Figure(?). Finally, all our teammates could access our Cloud9 and collaborated with it.


### Result

So far, we have installed and configured our Cloud9 IDE, and we were able to move to our next part of project: creating and connecting IoT devices. Moreover, we had the great experience of pair programming on the Cloud9 IDE, which significantly improved our efficiency.



### Reference

1. AWS Cloud9 https://aws.amazon.com/cloud9/?nc2=type_a