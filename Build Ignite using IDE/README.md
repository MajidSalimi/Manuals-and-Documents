Build Apache Ignite using IDE

To run and use Apache Ignite on Ubuntu, you must first install java and an appropriate IDE.


Step 1: Install Oracle Java JDK 8

The easiest way to install Oracle Java JDK 8 on Ubuntu is via a third party PPA… To add that PPA, run the commands below
   
      sudo add-apt-repository ppa:webupd8team/java

After running the commands above, you should see a prompt to accept the PPA key onto Ubuntu… accept and continue

run the commands below to download Oracle Java 9 installer:

      sudo apt update
      sudo apt install oracle-java8-installer

When you run the commands above you’ll be prompted to access the license terms of the software… accept and continue..
Set Oracle JDK8 as default, to do that, install the oracle-java8-set-default package. This will automatically set the JAVA env variable.
 
      sudo apt install oracle-java8-set-default

you can check you java version by running following command:
 
      javac -version


Step 2: Downloading NetBeans
After installing Java JDK to your system, run the commands below to download NetBeans 8.2
