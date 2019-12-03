---
layout: page
title: Oak Storage
permalink: /
---

# Oak Storage

<div style="float: left; width:20%; margin-right:20px">
     <img src="{{ site.baseurl }}/assets/img/logo/oak.png">
</div><br><span>
Oak is a High Performance Computing (HPC) storage system available to research groups and projects at Stanford. 
Learn <a href="{{ site.baseurl }}/about">more about Oak</a> or contact us at [srcc-support@stanford.edu](mailto:srcc-support@stanford.edu?subject=Oak%20storage) for further questions.
   </span>
<br><br>

## Oak Service Overview

Oak is a storage system provided by the Stanford Research Computing Center
([SRCC](https://srcc.stanford.edu/)) and available to all researchers at Stanford University.
It is based on [Lustre](http://lustre.org), a distributed parallel file system with wide scalability,
both in performance and storage capacity.

Oak is particularly well suited to store large group-shared datasets, curated output of HPC job campaigns and archives at a
very affordable price. Oak is available from multi-protocol gateways (like Globus, SFTP and SMB) and is
mounted on the Sherlock HPC cluster. Based on off-the-shelf components and open source software, it can easily
grow in order to accommodate the research projects’ increasing storage requirements, up to tens of petabytes.

Two flavors of the storage service are available (charged monthly):

|  Service flavor     | Service description | Service price |
|---------------------|---------------------|---------------|
| **10TB FILESPACE**  | Disk space in increments of **10 TB and 1.5 million inodes**[^1]. | $42.95 per 10TB / month<br> <small>*or $0.004295/GB/month*</small> |
| **250TB FILESPACE** | Disk space in increments of **250 TB and 37.5 million inodes**[^1]. | $550 per 250TB / month<br> <small>*or $0.0022/GB/month*</small> |

[^1]: inodes are filesystem objects like files and directories

Oak storage is readily available from [Sherlock](http://www.sherlock.stanford.edu/), [SCG](https://login.scg.stanford.edu/) and [XStream](http://xstream.stanford.edu/) HPC clusters,
but also from multi-protocol gateways (Globus, SFTP, NFSv4, SMB/CIFS...). Shared Globus and SFTP gateways are available for all, but personalized gateway service, like SMB or NFS,
will incur additional costs to the PI:

|  Service flavor | Service description | Service price |
|-----------------|---------------------|---------------|
| **Gateway**     | Access to and management of gateway to Oak Storage | $71 / month per gateway<br> |

{% include alert.html type="warning" title="Important!" content="Oak is NOT <a href='https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act'>HIPAA</a> compliant and is not a storage choice for any data that include <a href='https://en.wikipedia.org/wiki/Protected_health_information'>PHI</a> or <a href='https://en.wikipedia.org/wiki/Personally_identifiable_information'>PII</a>. The system is approved for storing Low and Moderate Risk data only and is not suitable for data classified as <a href='https://dataclass.stanford.edu'>high-risk</a>. For more information about data risk classifications, see the <a href='https://uit.stanford.edu/guide/riskclassifications'>Information Security Risk Classification page</a>" %}

{% include alert.html type="info" title="Service Description" content="For more details about Oak, please look at the official Oak Service Description available <a href='https://stanford.box.com/s/t979jbzw5ejbf2u2w0781hayke1k384y'>here</a> (Stanford only)." %}


## Oak group space

 *  There are only group/project spaces on Oak (similar to how /home/groups or /scratch/groups work on Sherlock).
 *  When a group directory is created on Oak, we use the PI/faculty SUNet ID as the group name (eg. /oak/stanford/groups/SUNetID/).
 *  Or, alternatively, a project directory can be created under /oak/stanford/projects/.
 *  File system group quotas are used to limit the amount of file system space group/project can use.
 *  Each group is provided with a personal dashboard that provides information about available disk space (quota) and usage.


## Managing users

 *  The PI provides an initial list of SUNet IDs having access to the new group or project shared directory on Oak.
 *  The PI gets access to a [Stanford Workgroup](https://workgroup.stanford.edu) to manage authorized users (please be aware that changes made in Workgroup Manager may take up to 4 hours to be propagated to Oak).
 *  Members of the workgroup can then organize files as they desire in the group/project directory (POSIX ACLs are supported).


If you would like to contribute to the site or ask a question, please [open an issue]({{ site.repo }}/issues)
