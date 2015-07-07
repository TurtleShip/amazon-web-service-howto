# How to install maven on Amazon linux

You can find maven download link [here](https://maven.apache.org/download.cgi). For simplicity, I am using ```http://apache.spinellicreations.com/maven/maven-3/3.3.3/binaries/apache-maven-3.3.3-bin.tar.gz``` as my download link.


```sh
# download maven
sudo wget http://apache.spinellicreations.com/maven/maven-3/3.3.3/binaries/apache-maven-3.3.3-bin.tar.gz

# Unzip it
sudo tar -xzvf apache-maven-3.3.3-bin.tar.gz

cd apache-maven-3.2.3
pwd
export M2_HOME'the path outputed by pwd command'
export M2=$M2_HOME/bin
export PATH=$PATH:$M2
mvn --version # this should output maven version
```
