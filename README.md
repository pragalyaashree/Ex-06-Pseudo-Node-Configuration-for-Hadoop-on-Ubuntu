# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/fb683f28-5d7f-480d-ac20-21ac33476be4)

2.	Install java1.8 in folder /usr/local
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/c6af9ea5-b084-45ac-a045-ffdbf08dd99b)

3.	Install Hadoop
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/0bd1b98e-7c65-46ca-9e82-af2177f041d6)

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/d4af64bf-1087-47d8-bb32-051c2fa17729)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/0ff1d9f0-1f12-4ec0-b874-8ed9ee44632b)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes

![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/42ce982e-e39d-4b1e-a417-85ad4981bf0e)
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/8dfe194e-9baf-42d2-af7e-181691342e8a)

$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh

Include the following lines in hadoop-env.sh file
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/e07d941b-e554-47e5-8218-80e57c547a3f)


b)	core-site.xml

Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/bbcb5e77-608c-4791-9d83-15a4cdb4f7d1)

Include the following lines in core-site.xml file between <configuration> and
</configuration> tags
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/fffe1c7a-d19c-466d-b0d1-278dea2f2e38)




c)	mapred-site.xml
```
 $sudo cp mapred-site.xml.template mapred-site.xml
```
Include the following lines in mapred-site.xml file
```
 <property>
<name>mapreduce.framework.name</name>
<value>yarn</value>
</property>
```

d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/0d9b9fd9-2879-49ff-80bc-c1b04cadbe49)


e)	yarn-site.xml
Include the following lines in yarn-site.xml file
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/8b1c2dcc-678d-44a0-a331-beb4961143ce)

8.	Format the Hadoop File system implemented on top of the local file system using
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/6f4bb7e1-6bfd-4a7e-9f44-18fa548c34e3)

9.	Start Hadoop using
```
$sbin/start-all.sh
```


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/88b7a855-2094-4c2e-9388-2302f1e46318)


11.	Create a directory ‘/input’ in HDFS
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/9f3aacc4-df82-4be1-b11e-24a204db392d)


12.	Copy the input files into the distributed file system
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/0a1e3a5b-9287-488c-ad8a-7025040ac998)

13.	Run some of the examples provided
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/818166a7-a25f-4858-a725-6cb51bee12df)


14.	Examine the output files
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/6779a22c-f372-4c3a-9076-fb1e05892f54)


Copy the output files from the distributed file system to the local file system and examine them:
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/32fba8e3-6764-4673-aefd-7bdd2acab4e0) 
or
View the output files on the distributed file system
![image](https://github.com/AfzaraThagsin/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127172501/9747286b-ff99-48e2-9076-a8d8ae4cdefe)


## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
