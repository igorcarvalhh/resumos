## How to install JAVA

Download the binary file at: 

https://www.oracle.com/java/technologies/javase-jdk16-downloads.html

Inside the folder that contains the downloaded file, move it to `/usr/lib/jvm` and extract

```sh
$ sudo mv jdk-16.0.1_linux-x64_bin.tar.gz /usr/lib/jvm
$ sudo tar zxvf /usr/lib/jvm/jdk-16.0.1_linux-x64_bin.tar.gz
```
Add the binaries to `PATH`
```bash
$ export JAVA_HOME="/usr/lib/jvm/jdk-16.0.1"
$ export PATH=JAVA_HOME/bin:$PATH
```
To test the intallation
```bash
java -version
```

## Intalling Gradle manually

### Prerequisites

* Java JDK version 8 or higher to be intalled

### Installing Gradle

Download the binary file in: https://gradle.org/install/

![](/home/igor/Pictures/Screenshot from 2021-05-12 12-04-39.png)

click in *binary-only*

```bash
$ sudo mkdir /opt/gradle
$ sudo unzip -d /opt/gradle gradle-7.0.1-bin.zip
$ export PATH=$PATH:/opt/gradle/gradle-7.0.1/bin
$ gradle -v 
```

If you have an old version of gradle run

```bash
sudo apt purge gradle
```

## Maven

https://maven.apache.org/download.cgi

```bash
$ sudo mkdir /opt/maven
$ sudo unzip -d /opt/maven apache-maven-3.8.1-bin.zip
$ export PATH=$PATH:/opt/maven/apache-maven-3.8.1/bin
$ mvn -v
```

If you have an old version of maven run

```bash
$ sudo apt purge maven
```

## Wrappers

>  ensures the same version for all developers

### Gradle

Inside you project folder

first create a file named `settings.gradle` 

```bash
$ touch settings.gradle
$ gradle wrapper
$ ./gradlew -v
```

### Maven

```bash
$ mvn -N io.takari:maven:wrapper
$./mvnw -v
```

## Installing IntelliJ

Download in: https://www.jetbrains.com/idea/download/#section=linux

```bash
$ sudo tar -xzf ideaIC-2021.1.1.tar.gz
$ cd idea-IC-211.7142.45/bin
$ ./idea.sh
```

