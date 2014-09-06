1. Install maven.
  ```sh
  wget http://mirror.metrocast.net/apache/maven/maven-3/3.2.3/binaries/apache-maven-3.2.3-bin.tar.gz
  tar zxcf apache-maven-3.2.3-bin.tar.gz
  cd apache-maven-3.2.3
  export M2_HOME=~/apache-maven-3.2.3/
  export M2=$M2_HOME/bin
  export PATH=$M2:$PATH
  mvn --version
  ```

2. Install git
  ```sh
  sudo yum install git
  ```

3. Install Java
  - Download java from [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html) from my local laptop.
  - scp the file to my ec2 instance
  ```sh
  scp -i my-key-pair.pem jdk-7u67-linux-x64.rpm ec2-user@elastic-ip:~/
  ```
  - ssh into my ec2 instance.
  ```sh
  ssh -i my-key-pair.pem ec2-user@elastic-ip
  ```
  - install java
  ```sh
    java -version # Check java version. Probably OpenJDK at the moment.

    sudo rpm -i jdk-7u67-linux-x64.rpm # install java

    # set paths
    export JAVA_HOME=/usr/local/jdk1.7.0_67
    export PATH=$PATH:$JAVA_HOME/bin

    # Check if java version is now Oracle
    java -version

    # If not, set Oracle java as default
    sudo /usr/sbin/alternatives --install /usr/bin/java java /usr/java/jdk1.7.0_01/bin/java 20000
    sudo /usr/sbin/alternatives --config java

    # Now default java should be Oracle java
    java -version
  ```
