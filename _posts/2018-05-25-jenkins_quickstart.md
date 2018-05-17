---
layout: post
title:  "Jenkins Quickstart Guide for Java Developers"
date:   2018-05-17
excerpt: "Intended to get you quickly up and running with Jenkins, while using some of its continuous integration capabilities"
tag:
- jekyll
- halve
- blog
- vangeltzo
- theme
- vangelis
---
# Jenkins Quickstart Guide for Java Developers  

Jenkins is an open source continuous integration server written in Java. This guide is intended to get you quickly up and running with Jenkins, while using some of its continuous integration (CI) capabilities.

Before you begin, you need the following system requirements:

**Storage**

- 512MB available
- 20 GB of free drive space

**Applications**

- [Java 8, JRE or JDK](https://java.com/en/download/)
- [Docker](https://store.docker.com)

## Install Jenkins

1.  Start by downloading Jenkins at: https://jenkins.io/download/ and choose the installation package that works with your environment.
2.  Double click the installer to launch the Jenkins Install Wizard
3.  When the installation is complete, a local instance of Jenkins is launched. Your browser window will open to this locally running Jenkins instance, where you are prompted to log in to complete the installation.
4. Before you log in, retrieve the password set by Jenkins during the install. To get your password, open a terminal and type:

````cl
sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword
````

5. Return to the Jenkins browser window, enter the password and log in.

You have now installed Jenkins.

## Creating a CI Pipeline

1. Open a browser, go to http://localhost:8080/ and log in with your password.
2. Create a new file, name it Jenkinsfile and insert the following:

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
10. Then select Multibranch Pipeline
11. Next select *Add source,* and choose the repository that has the new Jenkinsfile you just created.
12. Click save

You have now created a CI pipeline in Jenkins.

 Now that you are familiar with some of the basic CI functionality using in Jenkins, You can start creating more complex pipelines by building [Java applications with Maven.](https://java.com/en/download/)
