# Enable HDP/IBM BigSQL for Active Directory
This repository contains a number of practical steps to enable HDP services for Active Directory security. It is a follow-up after basic Kerberization.<br>
https://docs.hortonworks.com/HDPDocuments/HDP2/HDP-2.6.5/bk_security/content/configuring_amb_hdp_for_kerberos.html<br>
<br>

**Wiki** : https://github.com/stanislawbartkowski/hdpactivedirectory/wiki
# Test environment description
* Windows 2016 Active Directory
* HDP 2.6.5, HDP 3.1
* CentOS 7.6
# Prerequisities
HDP Kerberizarion is conducted already.
https://github.com/stanislawbartkowski/wikis/wiki/HDP-2.6.5-3.1-and-Active-Directory
# AD users and groups used for testing

In AD prepare *datascience* and *dataadmin* and create *user2* in *dataadmin* and *user3* in *datascience*. Malicious *user1* should not belong to any group.

* *User2* belongs to *dataadmin* group and has granted all privileges in *datalake*
* *User3* is a member of *datascience* group and can access and read data in *datalake* but cannot modify anything. 
* *User1* does not belong to any groups, thus should be denied any access try, malicious user




