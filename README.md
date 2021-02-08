<img src = "https://img.shields.io/badge/version-1.1.1-brightgreen" />

Hadoop-MasterNode
=========

* This Ansible Role is used to configure the Hadoop v2 MasterNode!
* This role will be using the most stable version of Hadoop 2 i.e. Hadoop-2.10.1
* This role is used to configure Hadoop on **CentOS** based Linux Only.

Requirements
------------

* Hotspot Java Version 8 is required. In this role, specifically java version jdk-8u271-linux-x64.rpm is used. It might be possible that, this version is not available now online.
* Download any version of oracle/hotspot java version 8, place the file in the "files" folder in the role. In this role, the folder is not present because it was empty, so it was not uploaded. Therefore, first of all create that folder & then place that jdk downloaded in this folder.
* Remember to download that jdk that ends with **linux-x64.rpm**.
* The group name of the systems that has to be configured for Master Node should be **"MasterNode"** in the Inventory File (not required, if running this role on the localhost, in the case of running this role on the localhost, "localhost" keyword must be used while mentioning the hosts in the ansible-playbook).

**Very Important Changes in the code that needs to be done by the user!**
* Whichever java you download, make sure to replace the name mentioned in the line number 42 of this code by the java package name you have downloaded.
* Also, replace the exact version of the java version mentioned on line number 103 in the code by the exact version you have downloaded. For example, in the code, in line number 103, it is been written as "jdk1.8.0_271", now, if you have downloaded the package "jdk1.8.0_281-linux-x64.rpm", then replace the java version on line number 103 by "jdk1.8.0_281".  

Role Variables
--------------

**NameNode_Format** => This should be assigned to "no" when the NameNode is already been formatted for the first time. But as & when re-formatting is required, it can be again set to "yes". By default, it is set to "yes".
<br />

**softwares** => This is the directory where the JDK will be copied.
<br />

**NameNode_Port** => Port on which the NameNode will be running.
<br />

**hadoop_dir** => Directory where the Hadoop package will be extracted. 
<br />

**NameNode_Dir** => This is the Directory where the NameNode Metadata will be kept!
<br />

**Replication_Factor** => Replication Factor for the data in the Hadoop Cluster. By default, it is set to "1".

Dependencies
------------

* Linux DVD Image should be attached to the VirtualBox(specifically in case of using this role to configure in VirtualBox)!
* If not using this role in Virtual Machine, then make sure that the Linux dvd Image is available at the location **"/dev/cdrom** or **"/dev/sr0""**, if not, then update the path in the line number 11 of the main tasks file.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: MasterNode
      roles:
         - Hadoop-MasterNode

License
-------

[MIT](https://github.com/HarshitDawar55/Hadoop-v2-MasterNode/blob/main/LICENSE)

Author Information
------------------

Developed by Harshit Dawar, also known as Technologist, a public speaker, extrovert, & optimist.

**LinkedIn:** https://www.linkedin.com/in/harshitdawar

**PortFolio:** https://harshitdawar55.github.io

**Twitter:** https://www.twitter.com/harshitdawar55

**Medium:** https://harshitdawar.medium.com

**GitHub:** https://www.github.com/harshitdawar55
