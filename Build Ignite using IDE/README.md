# Build Apache Ignite using IDE

To run and use Apache Ignite on Ubuntu, you must first install java and an appropriate IDE.

#### Step 1: Install Oracle Java JDK 8

The easiest way to install Oracle Java JDK 8 on Ubuntu is via a third party PPA… To add that PPA, run the commands below
```   
sudo add-apt-repository ppa:webupd8team/java
```
After running the commands above, you should see a prompt to accept the PPA key onto Ubuntu… accept and continue

run the commands below to download Oracle Java 9 installer:
```
sudo apt update
sudo apt install oracle-java8-installer
```
When you run the commands above you’ll be prompted to access the license terms of the software… accept and continue..
Set Oracle JDK8 as default, to do that, install the oracle-java8-set-default package. This will automatically set the JAVA env variable.
``` 
sudo apt install oracle-java8-set-default
```
you can check you java version by running following command:
``` 
javac -version
```
#### Step 2: Install maven
```
sudo apt-get purge maven maven2 maven3
sudo add-apt-repository ppa:natecarlson/maven3
sudo apt-get update
sudo apt-get install maven build-essential libgomp1 git
```
#### Step 3: Downloading NetBeans
After installing Java JDK to your system, run the commands below to download NetBeans 8.2
```
cd /tmp
wget -c http://download.netbeans.org/netbeans/8.2/final/bundles/netbeans-8.2-linux.sh
```
Wait until the complete package is downloaded to your machine… it should download to the /tmp directory.

#### Step 4: Install NetBeans
After downloading the installer package, while still in the /tmp directory, run the commands below to install.
```
chmod +x netbeans-8.2-linux.sh 
sudo ./netbeans-8.2-linux.sh
```
Then, installation wizard start. click next...
Then NetBeans installation should continue. If the installer can’t find where Java JDK is installed, you will have to browse to find it. The default location on Ubuntu is stored at:
_/usr/lib/jvm/java-8-oracle_


After installing, launch the application and begin building Apache Ignite.

#### Step 5: Build Apache Ignite
