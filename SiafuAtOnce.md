# Installing Siafu Simulator at once #

Tested on: 
Ubuntu 20.04.2.0-desktop-amd64 Linux Image
Java 16.0.2
Apache Maven 3.8.2

In case Java is not installed:

sudo add-apt-repository ppa:linuxuprising/java
sudo apt-get update
sudo apt install oracle-java16-installer
sudo dpkg --configure -a

In case Maven is not installed:

Download Maven Binary tar.gz archive from https://maven.apache.org/download.cgi and extract it.
sudo mv /FOLDER_WHERE_THE_ARCHIVE_IS_LOCATED/apache-maven-*-bin.tar.gz /tmp/
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
sudo ln -s /opt/apache-maven-3.6.3 /opt/maven
mvn -version

sudo nano /etc/profile.d/maven.sh
export JAVA_HOME=/usr/lib/jvm/java-16-oracle
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}

sudo chmod +x /etc/profile.d/maven.sh
source /etc/profile.d/maven.sh

Pick a folder to download Siafu Simulator: git clone https://github.com/miquelmartin/Siafu.git
sudo apt-get update
sudo apt-get upgrade

Enter /Siafu/MavenParent folder and open pom.xml with your favorite text editor

Replace the pom.xml with this one

In case you still get error, 



