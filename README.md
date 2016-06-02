# Jelastic MariaDB Database Replication Installation Package 

This repository provides [MariaDB Database Replication](http://docs.jelastic.com/mariadb-master-slave-replication/) JPS-based installation package for Jelastic Platform.

**MariaDB Database Replication** is used to solve performance problems, to support the db backups, and to alleviate system failures. It enables data from one database server (master) to be replicated to another (slave).

**Engine**: java

**Environment topology**:

1. 
   - node type: mariadb
   - count: 2
   - cloudlets: 16
   

### What it can be used for?
Master-slave replication is used to solve a number of different problems with performance, supporting the backup of different databases, and as a part of a larger solution to alleviate system failures. It enables data from one database server (the master) to be replicated to one or more database servers (the slaves).
<br />
The master logs the updates, which then ripple through to the slaves. The slave outputs a message stating that it has received the update successfully, thus allowing to send the subsequent updates. Master-slave replication can be either synchronous or asynchronous. The difference is simply the timing of propagation of changes. If the changes are made to the master and slave at the same time, it is synchronous. If changes are queued up and written later, it is asynchronous.


### What Jelastic JPS package is?

Jelastic JPS package represents an one-click installation solution, that allows to get the desired project hosted at Jelastic Cloud in a matter of minutes. Being based on [Jelastic Packaging Standard](https://docs.jelastic.com/jps), it automates creation of the necessary environment and subsequent application deployment to it. Herewith, all of the required properties and behaviors are predefined within the package JSON manifest, so you instantly get the ready-to-go solution.
The full list of the available at a platform one-click packages can be seen at the corresponding same-named section of [Jelastic Marketplace](https://docs.jelastic.com/marketplace#apps].

### How to deploy a package?
###### For Developers

In case you can’t find the desired solution within the list of available ones at your dashboard, just copy and save the content of its manifest as a *.json* file and [import](https://docs.jelastic.com/environment-export-import#import) it to the dashboard. Herewith, you can apply any necessary adjustments to template settings through this file (if such are required) and install its customized version in the similar way.

###### For Cluster Admins

In order to add the desired JPS package to your platform and make it available for users, perform the following:
- copy content of its manifest 
- switch to the [Marketplace](http://ops-docs.jelastic.com/marketplace-46) section of your JCA panel and choose **Add > New Installation** menu option
- paste the copied strings into the appeared frame and **Save** the template
- choose your newly added package within the list and click on **Publish** above

Also, you are able to adjust the given package template according to your needs and provide its customized version.