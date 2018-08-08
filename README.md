# Building Java Projects with Gradle

https://spring.io/guides/gs/gradle/#scratch

This is a good beginner guide that walks through using Gradle to build a simple Java project.

## Some Learnings

1. Some gradle commands are:

```
  $ gradle -v
  $ gradle tasks
  $ gradle build
  $ gradle wrapper --gradle-version 4.7
  $ gradle run
```
And after a gradle wrapper has been created, one can use:

```
  $ ./gradlew build
  $ ./gradlew run
```

2. The Gradle Wrapper is the preferred way of starting a Gradle build. It consists of a batch script for Windows and 
   a shell script for OS X and Linux. These scripts allow you to run a Gradle build without requiring that Gradle be installed 
   on your system.

3. To run the "gradlew" (gradle wrapper) executable, on *nix systems,  prefix gradlew with "./" e.g.:

```
  $ ./gradlew build
```  

4. Use the following to peek into a "jar"file:

```
  $ jar tvf build/libs/gs-gradle-0.1.0.jar
``` 

5. Bundled "jar" files:
   - are NOT runnable; and
   - do NOT contain declared dependency libraries

6. The Gradle wrapper files are designed to be committed to source control so anyone can build the project without having
   to install and configure a specific version of Gradle.  
