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
#### 1.1. Install a Windows Linux Subsystem
1. Open PowerShell or Windows Command Prompt in administrator mode by right-clicking and selecting "Run as administrator"
2. Run `wsl --install --distribution Debian` command.  
   We choose Debian distribution for this tutorial.
3. Restart your machine
4. You can access your WSL files by navigating to `wsl` in File Explorer.

**One could encounter **`WslRegisterDistribution failed with error: 0x80370102`** error**  
This [tutorial](https://www.partitionwizard.com/partitionmagic/wslregisterdistribution-failed-with-error-0x80370102.html) could help you to solve the issue.

#### 1.2. Install `make` with `apt`
```
sudo apt update
sudo apt install -y make
```

#### 1.3. Run `wsl` from `tp-corba-java/EXO1/`
1. Open File Explorer
2. Navigate to `tp-corba-java/EXO1/`
3. Run `wsl` in the address/path bar of File Explorer

#### 1.3. Go back to 0. step and follow instructions for a linux OS

## 2. Make
The current working directory being `EXO1/` folder.  
1. Run `source .env` **(It should only work for linux)**
2. Run `make` from command line interface

## 3. Start server
Run `java tpcorba.exo1.Serveur`.  
If it worked, one would see `Le serveur est pret`.
