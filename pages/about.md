---
title: About
permalink: /about/
---

# About

Oak is a High Performance Computing (HPC) storage system available to research groups and projects at Stanford. Hosted by the Stanford Research Computing Center (SRCC) and sometimes referred as "cheap and deep storage", *Oak* provides the research community with inexpensive storage for research projects, storage that can grow in order to accommodate the projects’ increasing storage requirements.

## The System

Oak is a capacity-oriented HPC storage system designed for long term storage that doesn't rely on a single vendor implementation. It was designed by the SRCC team using COTS (commercial off-the-shelf) components and open source software to provide up to billions of inodes and tens of petabytes of storage space to answer Stanford researchers' big data storage needs.

The software of Oak is based on the [Lustre filesystem](http://lustre.org) and the [Robinhood Policy Engine](https://github.com/cea-hpc/robinhood/wiki). Personalized usage dashboards are provided thanks to the [Grafana](https://grafana.com/) and [Docker](https://www.docker.com/) projects.

Oak's scalable and highly available architecture is based on MD cells (metadata) and I/O cells (data) each with external SAS-3 switches and high-density JBOD chassis designed for the cloud market. The Lustre servers are interconnected through a high-bandwidth and low-latency Infiniband fabric (56 Gb/s links). Oak storage components are redundant, from servers to disk array controllers and data paths between servers and disks. It also provides disk mirroring for the metadata and double-parity RAID in a 8+2 configuration for the data (file content). The use of additional parity allows the storage system to continue to function even if two disks in a volume of ten disks fail simultaneously.

SRCC's Oak project was first presented at the Lustre Administrators and Developers workshop in September 2016 in Paris. The slides are available [here](https://www.eofs.eu/_media/events/lad16/07_thiell_cheap_n_deep.pdf).


## Support

If you need help, please don't hesitate to [open an issue](https://www.github.com/{{ site.github_repo }}/{{ site.github_user }}).

