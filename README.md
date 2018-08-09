# Building Java Projects with Gradle (a spring.io guide)

This is a good beginner guide that walks through using Gradle to build a simple Java project:
<https://spring.io/guides/gs/gradle/#scratch>

## Some Learnings From The Experience

01 Some gradle commands are:

  ``` bash
    gradle -v
    gradle tasks
    gradle build
    gradle wrapper --gradle-version 4.7
    gradle run
  ```

  And after a gradle wrapper has been created, one can use:

  ``` bash
    ./gradlew build
    ./gradlew run
  ```

02 The Gradle Wrapper is the preferred way of starting a Gradle build. It consists of a batch script for Windows and 
   a shell script for OS X and Linux. These scripts allow you to run a Gradle build without requiring that Gradle be installed 
   on your system.

03 To run the "gradlew" (gradle wrapper) script/executable, on *nix systems,  prefix gradlew with "./" e.g.:

  ``` bash
    ./gradlew build
  ```  

04 Use the following to peek into a "jar"file:

  ``` bash
    jar tvf build/libs/gs-gradle-0.1.0.jar
  ```

05 Bundled "jar" files:

- are NOT runnable; and
- do NOT contain declared dependency libraries

06 The Gradle wrapper files are designed to be committed to source control so anyone can build the project without having to install and configure a specific version of Gradle.

07 Add a `.gitignore` with most file ignore patterns before adding source files to the repo. This will prevent untracked files from being added to the git tracked files index.

08 To get git to stop tracking an erroneously previously tracked file, it must be removed from the git index. To do that:

  ``` bash
    git rm --cached <filename-of-erroneously-tracked-file>
  ```

  Then update the `.gitignore` file with the file/folder pattern so that it is will not be tracked in future, then commit.

09 Ensure binary files, like JAR files, are not tracked i.e. added to the `.gitignore` file.

10 Try to selectively add folders and files i.e. `git add <file>`, rather than adding all files at once i.e. `git add .` .

11 If needed, to remove blobs from the repo, use `git filter-branch` <https://git-scm.com/docs/git-filter-branch> to rewrite branches, or, alternatively, use another tool like *BFG Repo-Cleaner <https://rtyley.github.io/bfg-repo-cleaner/>* which appearently does the same thing but faster. :)

❇️🍰❇️

## Future Things

Redo this but use Docker
