---
layout: post
title: "Jenkins Quickstart Guide for Java Developers"
---
# Jenkins Quickstart Guide for Java Developers   [![Donate](https://img.shields.io/badge/paypal-donate-blue.svg)](https://www.paypal.me/taylantatli/0usd)

Jenkins is an open-source continuous integration server written in Java. This guide is intended to get you quickly up and running with Jenkins while using some of its continuous integration capabilities.

Before you begin, you need the following system requirements:

**Storage**
512MB  of storage
20 GB of drive space
iromet
 **Software**
[Java 8, JRE or JDK](https://java.com/en/download/)
[Docker](https://store.docker.com)

##Install Jenkins

1.  To download Jenkins, go to: https://jenkins.io/download/ choose the installation package that works with your enviroment.
2.  Double click the installer to launch it—this launches the Install Wizard.
3.  At installation completeion a local instance of Jenkins will be launched by the installer.
Your browser window will open to this locally running Jenkins Instance where you are prompted to log in to complete the installation.

4. In order log in you will need to retrieve the password set by Jenkins. To get your password, open a terminal and type:

````cl
sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword
````
This will return the password string to log into Jenkins

## Creating a CI Pipeline
1. Open a browser, go to http://localhost:8080/ and log in with your password.
2. create a new file, name it Jenkinsfile and insert the following:
````JavaScript
Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
````
8. Open Jenkins and choose create a new file
*This will be your new CI pipleline*
9. Name your new pipeline
10. Select Multibranch Pipeline
11. Select *Add source,* choose the repository with the new Jenkinsfile
12. Click save
Now you have created your CI pipeline.
For more informaton on creating CI pipleines To create Java applications see **Build a Java app with Maven** 
