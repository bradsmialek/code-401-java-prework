# ![CF](http://i.imgur.com/7v5ASc8.png) 401 Java: Computer Setup & Installation

For this assignment, turn in a screenshot of your terminal, where you've run the following commands in order. (You can copy-paste this entire chunk into your terminal.) If any of the output is different from the comment at the end of the line, then something has gone wrong in your installation, and you should reach out to your instructor for help.

```bash
mkdir setup-verification
cd setup-verification
gradle init --type java-library # should run some stuff and eventually give a success message
ls src/main/java # should say Library.java
./gradlew test # should say that all tests pass
```
