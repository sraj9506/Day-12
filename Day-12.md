### Project 01

#### Project Overview

Your organization is implementing continuous integration (CI) practices
to streamline the software development lifecycle. As part of this
initiative, you will create a Jenkins declarative pipeline for building
a simple Maven project hosted on GitHub. This project aims to automate
the build process, ensure code quality, and facilitate continuous
delivery (CD).

Instructions

1.  Setup Jenkins Job

    -   Create a new Jenkins pipeline job. Here we choose pipeline
         option.

 ![](.//media/image1.png)
-   Configure the job to pull the Jenkinsfile from the GitHub
     repository.Tjough it is private repository we provide credentials.

 ![](.//media/image2.png)
2.  Create Jenkinsfile

    -   Write a declarative pipeline script (Jenkinsfile) that includes
         the following stages:

 1.Checkout

 2.Build

 3.Archieve Artifact

 1 Checkout : for the checkout we have to provide credentials id
 because we are fetching java code from private repository.

 2.Build: for the build we have to execute maven clean install command
 and therefore we have to provide path of maven and that's why we use
 environment variable at the starting of file.

 3.Archieve Artifact : Then after building the pipeline we archieve it
 on another location because by default it is stored in workspace which
 is volatile which means it remove previous build when we rebuild the
 pipeline.

![](.//media/image3.png)

3.  Configure Pipeline Parameters

    -   Allow the pipeline to accept parameters such as Maven goals and
         options for flexibility.

    -   Ensure the pipeline can be easily modified for different build
         configurations.

4.  Run the Pipeline

 ![](.//media/image4.png)

 We can see in the output console that build is successfully finished.
