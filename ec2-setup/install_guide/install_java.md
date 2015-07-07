# How to install Java on Amazon linux

1. Download java from Oracle. Note that a hack is required to bypass 'Accepting terms of Agreement' Oracle enforces you. Replace wget url with the java version you want to download, which can be found from [Oracle download site](http://www.oracle.com/technetwork/java/javase/downloads/index.html).

  ```sh

  sudo wget -c --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u45-b14/jdk-8u45-linux-x64.rpm" --output-document="jdk-8u45-linux.rpm"
  ```


2. Install it

  ```sh
    sudo rpm -i jdk-8u45-linux.rpm
  ```

3. Add the below to your profile (ex> .zshrc )

  ```sh
    # set paths
    export JAVA_HOME=/usr/java/jdk1.8.0_45/
    export PATH=$PATH:$JAVA_HOME/bin
  ```
