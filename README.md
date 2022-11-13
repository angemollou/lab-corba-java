# EXO1

## 0. Install Java 8
From https://www.oracle.com/java/technologies/downloads/#java8,
install Java 8 according to your system

## 1. Set environment variables
### On linux, create a new file named ".env"

1. Change current working directory to `tp-corba-java/EXO1/` and add in `.env` file
```
#!/bin/sh

export MY_HOME=/home/path/to/project/folder/
export CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
export JAVA_HOME="/absolute/path/to/jdk/folder"
export PATH="$JAVA_HOME/bin:$PATH"

```
According to how he installed Java 8, one should remove `export JAVA_HOME="/absolute/path/to/jdk/folder"` from .env

### On Windows
#### 1.1. register all those variables
```
MY_HOME=/home/path/to/project/folder/
CLASSPATH="$MY_HOME/org.jboss.openjdk-orb.zip:$MY_HOME/idlj.jar:$MY_HOME/rmic.jar:classes"
JAVA_HOME="/absolute/path/to/jdk/folder"
PATH="$JAVA_HOME/bin:$PATH"
```
According to how he installed Java 8, one shouldn't set `JAVA_HOME="/absolute/path/to/jdk/folder"` variable.

#### 1.2. Install a Windows Linux Subsystem
1. Open PowerShell or Windows Command Prompt in administrator mode by right-clicking and selecting "Run as administrator"
2. Run `wsl --install --distribution Debian` command.  
   We choose Debian distribution for this tutorial.
3. Restart your machine

**One could encounter **`WslRegisterDistribution failed with error: 0x80370102`** error**  
This (tutorial)[https://www.partitionwizard.com/partitionmagic/wslregisterdistribution-failed-with-error-0x80370102.html] could help you to solve the issue.


## 2. Make
The current working directory being `EXO1/` folder.  
1. Run `source .env` **(It should only work for linux)**
2. Run `make` from command line interface

## 3. Start server
Run `java tpcorba.exo1.Serveur`.  
If it worked, one would see `Le serveur est pret`.
