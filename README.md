# EXO1

## On linux, create a new file named ".env"

1. Add in ".env"
```
#!/bin/sh

export MY_HOME=/home/path/to/project/folder/
export CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
export JAVA_HOME="$MY_HOME/jdk1.8.0_351"
export PATH="$JAVA_HOME/bin:$PATH"

```

## On Windows, register all those variables
```
MY_HOME=/home/path/to/project/folder/
CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
JAVA_HOME="$MY_HOME/jdk1.8.0_351"
PATH="$JAVA_HOME/bin:$PATH"
```
