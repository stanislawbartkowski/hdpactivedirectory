# HDP/CDP and Kerberos
This repository contains a number of practical steps to enable HDP services for Active Directory security. It is a follow-up after basic Kerberization.<br>
https://docs.hortonworks.com/HDPDocuments/HDP2/HDP-2.6.5/bk_security/content/configuring_amb_hdp_for_kerberos.html<br>
<br>

All specific descriptions are included in Wiki.<br>

**Wiki** : https://github.com/stanislawbartkowski/hdpactivedirectory/wiki

| System | Info | URL
| --- | --- | --- |
| HDP |How to integrate Ambari Console with AD/LDAP | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/Ambari-console-and-AD-LDAP
| HDP |  Atlas - AD/LDAP integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/Atlas
| HDP CDP | BigSQL AD authentication | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/BigSQL
| HDP | BigSQL/Ranger integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/BigSQL-and-Ranger
| CDP | Ranger AD/LDAP integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/Cloudera,-Ranger,-Active-Directory,-usersync
| HDP | Ranger - HBase integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/HBase,-Ranger
| HDP CDP | Ranger HDFS integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/Ranger-HDFS-plugin
| HDP CDP | Ranger and HBase integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/HBase-Ranger
| HDP | Ranger and Hive integration | https://github.com/stanislawbartkowski/hdpactivedirectory/wiki/Hive-Ranger


# Test environment description
After Kerberization, good practice is running simple tests to make sure that security takes effect. To run tests, make additional settings in AD or KDC/LDAP environment.

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
* *User1* does not belong to any groups, thus should be denied any access try.
<br>

| User | Group | Description |
| -- | -- | -- |
| user1 | (no group) | malicious user
| user2 | dataadmin | full access
| user3 | datascience | read-only access



