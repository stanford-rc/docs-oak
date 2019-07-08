---
title: Frequently Asked Questions
tags:
 - storage
 - xstream
 - archive
---

# Frequently Asked Questions

## Access

 - [Can I Access Oak from Sherlock and XStream?](#can-i-access-oak-from-sherlock-and-xstream)
 - [Can I Archive files to Oak from Sherlock?](#can-i-archive-files-to-oak-from-sherlock)
 - [Can I access Oak from my desktop/laptop?](#can-i-access-oak-from-my-desktop-laptop)
 - [Can I mount Oak on my own Linux cluster at Stanford?](#can-i-mount-oak-on-my-own-linux-cluster-at-stanford)

## Backup

 - [What about automatic backups?](#what-about-automatic-backups)


## Can I Access Oak from Sherlock and XStream?

Oak storage is available from all nodes on [Sherlock](http://www.sherlock.stanford.edu/) and [XStream](http://xstream.stanford.edu/) under /oak. Like Sherlock's /scratch, Oak is based on the Lustre parallel filesystem and is connected to Sherlock (1.0 and 2.0) and XStream through Infiniband.

{% include alert.html type="warning" title="Important!" content="You need an account on both Oak and Sherlock (or XStream) to access Oak from Sherlock (or XStream). The environment variable **$OAK** should be defined on Sherlock and XStream and contains the path to your Oak group directory. You may also use the full path starting with /oak as described above." %}

## Can I Archive files to Oak from Sherlock?

The [mpiFileUtils](https://github.com/hpc/mpifileutils) utilities are designed to copy files in parallel so you can quickly archives terabytes of data from scratch to Oak. The example below shows how to launch screen and launch a job that uses the dcp tool to copy a large directory:

```bash
[sunetid@sh-ln01 login_node ~]$ screen
[sunetid@sh-ln01 login_node ~]$ module load system mpifileutils
[sunetid@sh-ln01 login_node ~]$ srun -p dev -n 2 dcp $SCRATCH/dir $OAK/scratch_archive/
```

If you're a [Sherlock](http://www.sherlock.stanford.edu/) owner, you may want to replace `-p dev` with `-p your_partition` and increase the number of MPI tasks (`-n`) to copy even faster!


## Can I access Oak from my desktop/laptop?

Yes, please see the [Oak Gateways](https://srcc.stanford.edu/private/oak-gateways) page (Stanford only).


## Can I mount Oak on my own Linux cluster at Stanford?

Yes, the SRCC team can deploy specific Oak NFSv4 gateway(s) to mount your Oak group/project directory on your Linux-based compute cluster (or desktop for specific applications). It is mandatory to use SUNet IDs on your cluster and Kerberos is required to access Oak. Such a service will incur additional costs to the PI.

# Backups

## What about automatic backups?

While the hardware configuration is quite robust, **Oak does not provide local or remote data backup**, and should be considered as a single copy. The SRCC is currently evaluating options for adding automatic remote backups (to cloud storage). Such a service will incur additional costs to the PI.
