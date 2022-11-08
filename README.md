# EXO1

## 0. Install Java 8
From https://www.oracle.com/java/technologies/downloads/#java8,
install Java 8 according to your system

## 1. Set environment variables
### On linux, create a new file named ".env"

1. Add in ".env"
```
#!/bin/sh

export MY_HOME=/home/path/to/project/folder/
export CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
export JAVA_HOME="$MY_HOME/jdk1.8.0_351"
export PATH="$JAVA_HOME/bin:$PATH"

```
According to how he installed Java 8, one should remove `export JAVA_HOME="$MY_HOME/jdk1.8.0_351"` from .env

### On Windows, register all those variables
```
MY_HOME=/home/path/to/project/folder/
CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
JAVA_HOME="$MY_HOME/jdk1.8.0_351"
PATH="$JAVA_HOME/bin:$PATH"
```
According to how he installed Java 8, one shouldn't set JAVA_HOME="$MY_HOME/jdk1.8.0_351" variable.

## 2. Make
The current working directory begin **EXO1** folder.  
1. Run `source .env` **(It should only work for linux)**
2. Run `make` from command line interface

## 3. Start server
Run `java tpcorba.exo1.Serveur`
