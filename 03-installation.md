# ![CF](http://i.imgur.com/7v5ASc8.png) 401 Java: Computer Setup & Installation


### Operating Systems
This course supports Mac, Ubuntu and Windows users. All users must use the standard
setup for their system, as described in 201 & 301 prework. In particuluar, if you
use Windows, make sure you have the Windows Subsystem for Linux installed & set up
as described in [this guide](https://github.com/michaeltreat/Windows-Subsystem-For-Linux-Setup-Guide).

### Command Line Setup

**For WSL users**, please ensure that you've set up the WSL as described in the above guide. Also, please run `sudo dpkg-reconfigure tzdata` to pick your current timezone in Ubuntu.

### Editors and IDEs
We'll use a variety of text editors and IDEs to build our projects throughout this course. We use **Visual Studio Code** for light text editing, **IntelliJ IDEA** for pure-Java programs and **Android Studio** when we're building Android applications. Additionally, you'll need to make sure **Java** itself is installed, as well as **Gradle**, a build system for Java applications.

Download and install the following on your base OS:

* [Visual Studio Code](https://code.visualstudio.com/)
* [IntelliJ IDEA (Community Edition)](https://www.jetbrains.com/idea/)
* [Android Studio](https://developer.android.com/studio/)
* [Java](https://java.com/en/download/manual.jsp), version 8 if you get a choice
* [Gradle](https://gradle.org/install/) should be automatically installed by Android Studio, but that version won't necessarily be on your PATH.
    * WSL users: install Gradle following the [manual installation instructions](https://gradle.org/install/#manually) for Windows. This will AUTOMATICALLY set Gradle up for use in your Ubuntu system as well.
    * Mac users: run `brew install gradle`.
    * Linux users: probably use the [manual installation instructions](https://gradle.org/install/#manually).


**For WSL users**, also install Java, so you can use the `java` and `javac` commands from the terminal, using `sudo apt-get install default-jdk`.

**For WSL users**, you should also set up shortcuts for opening IntelliJ and Android Studio from the command line using these commands:
```bash
# WSL USERS ONLY
# IF YOU HAVE A MAC OR A LINUX MACHINE, DO NOT RUN THESE COMMANDS
echo 'alias ij="/mnt/c/Program\ Files/JetBrains/IntelliJ\ IDEA\ Community\ Edition\ 2018.2.4/bin/idea64.exe ."' >> ~/.profile
echo 'alias android="/mnt/c/Program\ Files/Android/Android\ Studio/bin/studio64.exe ."' >> ~/.profile
source ~/.profile
# now you can run `ij` or `android` to open each program.
```

**For Mac and Linux users**, you should open IntelliJ and Android Studio and go through `Tools > Create Command-Line Launcher` in the menu of each to set up the ability to launch them from the command line.

## Submission
For this assignment, turn in a screenshot of your terminal, where you've run the following commands in order. (You can copy-paste this entire chunk into your terminal.) If any of the output is different from the comment at the end of the line, then something has gone wrong in your installation, and you should reach out to your instructor for help.

```bash
mkdir setup-verification
cd setup-verification
gradle init --type java-library # should run some stuff and eventually give a success message
ls src/main/java # should say Library.java
./gradlew test # should say that all tests pass
ij # for WSL users: should open intellij
# or, if you went through the Mac/Linux "create command line launcher" process, run the command that you created there to open IntelliJ.
```
