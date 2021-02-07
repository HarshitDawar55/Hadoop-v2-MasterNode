Hadoop-MasterNode
=========

* This Ansible Role is used to configure the Hadoop v2 MasterNode!
* This role will be using the most stable version of Hadoop 2 i.e. Hadoop-2.10.1

Requirements
------------

Hotspot Java Version 8 is required.

Role Variables
--------------

**NameNode_Format** => This should be assigned to "no" when the NameNode is formatted for the first time. But as & when re-formatting is required, it can be again set to "yes". By default, it is set to "yes".
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

RedHat Enterprise Linux 8 DVD should be attached to the VirtualBox(specifically in case of using this role to configure in VirtualBox)! 

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: MasterNode
      roles:
         - Hadoop-MasterNode

License
-------

MIT

Author Information
------------------

Developed by Harshit Dawar, also known as Technologist, a public speaker, extrovert, & optimist.

**LinkedIn:** https://www.linkedin.com/in/harshitdawar

**PortFolio:** https://harshitdawar55.github.io

**Twitter:** https://www.twitter.com/harshitdawar55

**Medium:** https://www.medium.com/@harshitdawar

**GitHub:** https://www.github.com/harshitdawar55
