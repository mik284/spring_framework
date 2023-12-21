## [Click me to Learn about Maven](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)
> The src/main/java directory contains the project source code, the src/test/java directory contains the test source, and the pom.xml file is the project's Project Object Model, or POM.
### The POM xml file
* The pom.xml file is the core of a project's configuration in Maven.
* It is a single configuration file that contains the majority of information required to build a project in just the way you want.
* The POM is huge and can be daunting in its complexity, but it is not necessary to understand all of the intricacies just yet to use it effectively.


### Maven Phases
Although hardly a comprehensive list, these are the most common default lifecycle phases executed.

* validate: validate the project is correct and all necessary information is available
compile: compile the source code of the project
* test: test the compiled source code using a suitable unit testing framework. These tests should not require the code be packaged or deployed
* package: take the compiled code and package it in its distributable format, such as a JAR.
* integration-test: process and deploy the package if necessary into an environment where integration tests can be run
* verify: run any checks to verify the package is valid and meets quality criteria
* install: install the package into the local repository, for use as a dependency in other projects locally
* deploy: done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.
 
>There are two other Maven lifecycles of note beyond the default list above. They are

* clean: cleans up artifacts created by prior builds
* site: generates site documentation for this project
> Phases are actually mapped to underlying goals. The specific goals executed per phase is dependant upon the packaging type of the project. For example, package executes jar:jar if the project type is a JAR, and war:war if the project type is - you guessed it - a WAR.
