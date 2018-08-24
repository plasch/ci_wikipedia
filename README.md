## Jenkins Configuration

Shell-commands for run test-suite on Android:

```
sh /Users/user_name/IdeaProjects/java-appium/ci-scripts/runemulator.sh

cd /Users/user_name/IdeaProjects/java-appium;
export PLATFORM=android;
mvn -Dtest=TestSuite test
```
on iOS:

```
sh /usr/local/lib/node_modules/appium/build/lib/main.js &
#!/bin/bash --login -x
appium &

cd /Users/user_name/IdeaProjects/java-appium;
export PLATFORM=ios;
mvn -Dtest=TestSuite test
```

And need to add environment variables

```
${PATH}:/$ANDROID_HOME/emulator:/$ANDROID_HOME/tools:/$ANDROID_HOME/platform-tools:/$ANDROID_HOME/tools/bin:/$HOME/maven/bin:/$JAVA_HOME/bin
```
