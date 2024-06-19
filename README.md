# Learning_Singularity
A repository where I put the work I am doing with singularity containers.

## CNAF_Download
In this folder I put the code written to transfer the files from tape at CNAF to the Vega HCP. 

- **Build the container**: singularity build --sandbox --fakeroot download_gws.sif Singularity.def
- **Enter the container shell**: singularity shell download_gws.sif
- **Create a Virgo proxy**: voms-proxy-init --voms virgo:/virgo/virgo --vomses /root/virgo.voms
- **Download a .gwf file**: gfal-copy srm://storm-fe-archive.cr.cnaf.infn.it:8444/virgod0t1/Run/O3/raw/1238/V-raw-1238443600-100.gwf .
