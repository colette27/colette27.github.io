---
layout: post
title:  "Jenkins Quickstart Guide for Java Developers"
date:   2018-05-17
excerpt: "Intended to get you quickly up and running with Jenkins, while using some of its continuous integration capabilities"
tag:
- java
- blog
- jenkins
- CI
- installation
---
[View page MD](https://github.com/colette27/colette27.github.io/blob/master/_posts/2018-05-25-jenkins_quickstart.md)

# Jenkins Quickstart Guide for Java Developers  

Jenkins is an open source continuous integration server written in Java. This guide is intended to get you quickly up and running with Jenkins, while using some of its continuous integration (CI) capabilities.

Before you begin, you need the following system requirements:

**Storage**

- 512MB available
- 20 GB of drive space

**Applications**

- [Java 8, JRE or JDK](https://java.com/en/download/)
- [Docker](https://store.docker.com)

## Install Jenkins

1.  Download [Jenkins](https://jenkins.io/download/), choose the installation package that works with your environment.
2.  Double click the installer to launch the Jenkins install wizard.
3.  When the installation is complete, a local instance of Jenkins is launched. Your browser window will open to this locally running Jenkins instance, where you are prompted to log in to complete the installation.
4. Before you log in, you need to get the password set by Jenkins during the install. To get your password, open a terminal and type:
````cl
sudo cat /Users/Shared/Jenkins/Home/secrets/initialAdminPassword
````
5. Return to the Jenkins browser window. Enter the password and log in.

You have now installed Jenkins.

## Creating a CI Pipeline

1. In the Jenkins control panel, create a new file and name it Jenkinsfile.
2. Insert the following code into the Jenkinsfile:
````cl
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
3. This will be your new CI pipleline.
4. Give your pipleline a name.
5. Select *Multibranch Pipeline*
6. Next, select *Add source,* and choose the repository with the new Jenkinsfile you just created.
7. Click *save*

You have now created new a CI pipeline in Jenkins.

 Now that you are familiar with some of the basic CI functionality using in Jenkins, You can start creating more complex pipelines by building [Java applications with Maven.](https://java.com/en/download/)
