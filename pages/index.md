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

Oak is available for use by all Stanford University and affiliated research projects and groups. This includes healthcare researchers, as well as researchers from the SLAC National Accelerator Laboratory (SLAC). Please note that a four year commitment from the PI is required when when purchasing Oak.

{% include alert.html type="info" title="Service Description" content="For more details about Oak, please look at the official Oak Service Description available <a href='https://stanford.box.com/s/t979jbzw5ejbf2u2w0781hayke1k384y'>here</a> (Stanford only)." %}

Two flavors of the service are available for purchase with a 4-year commitment:

|  Service flavor | Service description | Service price |
|-----------------|---------------------|---------------|
| **Filespace**   | PIs/Faculty rent disk space in increments of **10 TB and 1.5 million inodes**.** | $41.67 per 10TB / month<br> <small>*or $50 per TB / year*</small> |
| **JBOD**        | PIs/Faculty purchase one or more full disk arrays (JBODs), with **550 TB usable capacity **each, that is/are supported and administered by the SRCC team as part of the overall Oak service. A JBOD comes with a maximum of 82.5 million inodes**. | JBOD cost* + $666.67 per JBOD / month<br><small>(service only)</small> |


<small>**JBOD pricing is dependent upon hard disk market variations ([contact us for current pricing](mailto:research-computing-support@stanford.edu?subject=Oak%20JBOD%20pricing))</small>
<small>**inodes are filesystem objects like files and directories *</small>

Oak storage is readily available from both the [Sherlock](http://www.sherlock.stanford.edu/) and [XStream](http://xstream.stanford.edu/) HPC clusters, but also from multi-protocol gateways (Globus, SFTP, NFSv4, Samba/CIFS...). *Restrictions may apply and personalized gateway service will incur additional costs to the PI.*

{% include alert.html type="warning" title="Important!" content="Oak is NOT <a href='https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act'>HIPAA</a> compliant and is not a storage choice for any data that include <a href='https://en.wikipedia.org/wiki/Protected_health_information'>PHI</a> or <a href='https://en.wikipedia.org/wiki/Personally_identifiable_information'>PII</a>. The system is approved for storing Low and Moderate Risk data only and is not suitable for data classified as <a href='https://dataclass.stanford.edu'>high-risk</a>. For more information about data risk classifications, see the <a href='https://uit.stanford.edu/guide/riskclassifications'>Information Security Risk Classification page</a>" %}

## Oak group space

 *  There are only group/project spaces on Oak (similar to how /share/PI or /scratch/PI work on Sherlock).
 *  When a group directory is created on Oak, we use the PI/faculty SUNet ID as the group name (eg. /oak/stanford/groups/SUNetID/).
 *  Or, alternatively, a project directory can be created under /oak/stanford/projects/.
 *  File system group quotas are used to limit the amount of file system space group/project can use.
 *  Each group is provided with a personal dashboard that provides information about available disk space (quota) and usage.


## Managing users

 *  The PI provides an initial list of SUNet IDs having access to the new group or project shared directory on Oak.
 *  The PI gets access to a [Stanford Workgroup](https://workgroup.stanford.edu) to manage authorized users (please be aware that changes made in Workgroup Manager may take up to 24 hours to be propagated to Oak).
 *  Members of the workgroup can then organize files as they desire in the group/project directory (POSIX ACLs are supported).



If you would like to contribute to the site or ask a question, please [open an issue]({{ site.repo }}/issues)
